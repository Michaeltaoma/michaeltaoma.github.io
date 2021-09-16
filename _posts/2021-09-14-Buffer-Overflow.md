# Buffer Overflow #

- Buffer overflow is a general method or scheme of a computer secure threat. Its main idea is: attacker puts in more content than total number of legal space in a buffer, data that exceeds the buffer limit overflow to somewhere they shouldn't be and directly affect the normal running of a program.

- How process stores

> ```
> 0xFFFFFFFF
> kernel -- denote command and env variables, run time?
> Stack -- denote arguments, local variables, run time
> ↓
> ↑
> Heap -- denote the dynamic memory alloctaed by malloc(), run time
> Uninitialized static data -- 特指的是static, compile time, static const int x;
> Initialized static data -- 特指的是static, compile time, static const int x = 10; 
> Text(code) -- denote the code segment, compile time
> 0x00000000
> ```

- Heap
	+ the heap is managed by the programmer, the ability to modify it is somewhat boundless
	+ in C, variables are allocated and freed using functions like malloc() and free()
	- 需要程序员自己去释放空间，不然的话，heap占用的空间就会被持续的占用
	+ the heap is large, and is usually limited by the physical memory available
	+ the heap requires pointers to access it

- what kind of buffer arrays are stored in stack?
	+ As mentioned, stack stored all the fixed length(stack itself is fixed-length)
	+ when declare fixed length array: `char buffer[n];`, the array will be stored in stack
	+ when declare dynamic length array: 
	```C
	char *buffer;
	buffer = new char[n];
	```
	the array will be stored in heap

- Stack Frame

> ```
> function arguments
> return address -- store the return address
> old ebp value -- stores the last location of ebp?
> local variables
> ```

when a function starts, things happen

0. ESP works as expected.
1. function arguments has been pushed(in reverse order, such that argumentN would actually being pushed prior to argument0)
2. current value in the EIP will be pushed to stack. This is the return address of the function. The address in current EIP is the adress where this particular function is being called
3. current EBP value will be pushed to the stack. This is to restore the EBP when the function ends.
4. EBP will be set to ESP. Since later when the function return, we need to point back the ESP to the start address to release storage.
5. Local variables get pushed onto the stack. ESP changes as expected.
6. Function runs. If local variables needs to be referenced, then it will be referenced using EBP
7. When function finishs running, ESP points to EBP, releasing all the space took by local variables.

### Over-write ###

#### Stack Overflow ####

##### Code #####

**Anything that tries to put more things in a *fixed* length array/buffer results in stack overflow**

```C
void func(char *arg1)
{
char buffer[4]; /* Initialize a fixed array */
strcpy(buffer, arg1); /*Put in the string*/
}

int main()
{
char *mystr = "AuthMe!"; /*Try to put in buffer more than it takes*/
func(mystr);
}
```

```C
char buffer[10]; /* Initialize a fixed array */
memcpy(buffer, "Hello, world!\n", 15); /*Try to put in buffer more than it takes*/
```

```C
#include <stdio.h>
#define MAX_IP_LENGTH 15 /*Define the holder length for ip address*/
int main(void) {
  char file_name[] = "ip.txt";
  FILE *fp;
  fp = fopen(file_name, "r");
  char ch;
  int counter = 0;
  char buf[MAX_IP_LENGTH]; /*Initialize a fixed length array*/
  while((ch = fgetc(fp)) != EOF) {
  	/*Fill the array*/
    buf[counter++] = ch;
  }
  buf[counter] = '\0';
  printf("%s\n", buf);
  fclose(fp);
  return 0;
}
```

##### How the attack works? #####

##### Stack Smashing #####
1. Construct input string (code injection)
	- "\[NOP SLED\]\[SHELLCODE(MAL CODE)\]\[PADDING\]\[OLD EBP\]\[RETURN ADDRESS\]"
		- Contains no all-zeros byte
			+ - Caused memcpy, scanf...to stop
		- NOP SLED
			- No operation, automatic skip to next line when encounter. Adding this helps with locating the desired address: as long as with land on one of NOP SLED, the actual start of the malicious code can be find
		- SHELLCODE(MAL CODE)
			- The malicious code we are trying to run. MUST BE:
				1. Machine Code
				2. Contains no all-zeros byte
					- Caused memcpy, scanf...to stop
				3. Can't used loader: must be self contained
			- Malicious code can just be Shellcode
				+ create a shell for the attacker so that the attacker is able to control the victim computer
		- PADDING
		- OLD EBP: The original address
		- RETURN ADDRESS
			- The start address of the mal code, can be one of the NOP SLED
2. Send the input string to a buffer to overflow it
3. Overwrite the return address

##### Return Oriented Programming #####
1. Find gadgets
	- Gadgets are chunks of library functions, or useful functions
	- To find useful gadgets, automate a search of the target binary for gadgets(look for `ret` instructions, work backwards)
2. Construct Input String
	- Contains addresses of different gadgets, in a way that they can be combined
	- arguments will be in between gadgets
3. Overwrite the return address
4. Stack serves as code
	- gadgets invoked via `ret`
	- gadgets get their arguments via `pop`

##### Return-to-libc #####
0. Can be viewed as a very special case of ROP since every "gadgets" used here would be a complete function from library.
1. Construct the input string
	- Contains the address of the library function that the attacker desire
	- Contains the arguments, if any
2. Sent the input string to a buffer to overflow it
3. Overwrite the return address with the address of the library function that the attacker desire
4. Executing the library function
5. Reading arguments from stack

##### Blind Return Oriented Programming #####
0. To tackle the randomization of code segment
0. Assume that when a process crash and re-run, the code would not be re-rand
1. 

##### Challenge #####
1. Loading code into memory
2. Getting injected code to run
3. Finding the return address

##### Defend Strategies #####

1. Make the bug harder to exploit

     - Examine necessary steps for exploitation, make one or more of them difficult or impossible

     - Best case: complicated exploitation by changing the libraries, compiler, and/or os

     - Detecting overflows with canaries（stop attacker putting code into the memory）
     	```
     	function arguments
		return address 
		old ebp value 
		------- canary -------
		local variables
     	```
     	+ carnary就是上面的这一小串代码，如果return address被覆盖的话，那么canary肯定也无了，只需要检查canary是否是一致的就好
     	+ what value should the canary have
     		* terminator canaries(用那些scanf看到就会停的东西，攻击者根本不会使这样的数据，因为如果一使用他们也用不了s 	
     		* random canaries：randomize each process start
     		* random xor canaries：store canary xor some control info

     - Make stack(and heap) non-executable(stop get %eip to point to attacker code)
     	+ In this case, the malicious code that we injected to the stack can't run
     	+ can be bypassed by return-to-libc

     - Address-space layout randomization-> ASLR
         - ASLR randomly arranges the address space positions of key data areas of a process(the location of the library) so an attacker does not know which addresses to inject into the call stack in order to abuse libc or other known software libraries including the system Kernel. 
         - caveats
         	+ only shifts the offset of memory areas
         	+ may not apply to program code
         	+ need sufficient randomness
         		* otherwise can be **brute force**
         - can be resolved by ROP

     - Randomization of the code segment

  2. Avoid the bug entirely

     - Secure coding practices
     - Advanced code review and testing

  3. Both are used

#### Heap Overflow ####
##### Code #####
```C
/*Define a struct(similar to an object) */
typedef struct _vulnerable_struct {
	char buff[MAX_LEN];
	int (*cmp)(char*, char*);
} vulnerable;

int foo(vulnerable* s, char* one, char* two)
{
	strcpy(s->buff, one); /*copy one in buff*/
	strcpy(s->buff, two); /*copy two in buff*/
	/*if one + two exceeds MAX_LEN, the *cmp pointer will be overwrite*/
	return s->cmp(s->buff, "file://foobar");
}
```
##### How the attack works? #####

##### Overflow into the C++ object *vtable* #####
For each object in C++, *vtable* contains pointers to the object's methods. **The attacker can overflow this vtable to modify the pointer**. Just like the most basic example, if one of the fields get overflowed, then the *vtable* can be modified.

##### Overflow into the adajecent #####
Like its name, this kind of variant overflow to the adajecent, especially those adajecent object with function pointers.

##### Overflow heap metadata #####
Heap metadata refers to a hidden header, used to keep track of heap allocated memory, just before the pointer returned by malloc. This header contain pointer linking a return object into a list of allocated data. Attacker can overflow this header to overwrite the pointer.

#### Integer Overflow ####

##### Code #####
```C
void vulnerable()
{
	char response;
	int nresp = packet_get_int();
	if (nresp > 0)
	{
		/*response is allocated as follow*/
		response = malloc(nresp*sizeof(char*)); /*The size of response can easily be corrupted since attacker can easily overflow the integer: nresp*sizeof(char*) and make it wraps to 0*/
		for (int i = 0; i < nresp; i++)
		{
			/*Then anything from packet_get_string would be overflowed*/
			response[i] = packet_get_string(NULL);
		}
	}
}
```

#### Data Corruption ####
##### How the attack works? #####
- **Modify a secret** to be known to the attacker, to be able to decrypy future intercepted messages

- **Modify state variables** to bypass authorization checks

- **Modify interpreted strings** used as part of commands. Like SQL injection.

#### Stale Memory: Dangling Pointer ####
##### Code #####
```C
struct foo {int (*cmp)(char*, char*);};
struct foo *p = malloc(...); /*Allocate memory*/
free(p); /*free the memory, but not the pointer*/

q = malloc(...); /*Locate the just-freed memory*/
*q = 0xdeadbeef; /*Overwrite the memory location that now has been pointed with p and q*/

p->cmp("hello", "hello"); //dangling pointer
```

##### How the attack works? #####
This kind of attack occurs when a pointer is freed, but the program continues to use it. An attacker can arrange for the freed memory to be reallocated and under his control, now, he can modify the data being pointed to malicious.

#### Format String Vulnerabilities ####
##### Code #####
```C
void vulnerable()
{
	char buf[80];
	if (fgets(buf, sizeof(buf), stdin)==NULL) return;
	/*the string buf might contain specifiers without arguments.*/
	printf(buf);
}
```

##### How the attack works? #####
`printf` takes variable number of arguments and pays no mind where the stack frame ends. So if there is a specifier in the first argument, it presumes that you called it with as many arguments as specified in the format string. Attacker can exploit this to make the program prints private information.

- `printf("100% dave");`: printf会直接把%和d的空格给忽略
  - `printf("%s");`: prints bytes pointed to by that stack entry，把eip右边的那个解成一个pointer，找到pointer指向的位置，把位置有的memory的东西全都print出来
  - `printf("%d %d %d %d");`: printf会直接把eip边上的四个entry（本来用来存储argument的地方）全都print出来
  - `printf("100% no way!");`: printf writes the number 3 to address pointed by stack entry
    - %n会把progress of printf load进下一个参数，例如`printf("The value of %ns : ", &s);`，那么在这里，s的值就是13，因为%n之前有13个character


### Over-read ###
#### Read Overflow ###
##### Code #####
```C
int main()
{
	char buf[100], *p;
	int i, len;
	while (1) {
		/*retrieve len*/
		p = fgets(buf, sizeof(buf), stdin);
		if (p == NULL) return 0;
		len = atoi(p);
		/*retrieve the string to print*/
		p = fgets(buf, sizeof(buf), stdin);
		if (p == NULL) return 0;
		for (int i = 0; i < len; i++)
		{
			/*if len > len(buf), then the attack happens and private information leaks*/
			if (!iscntrl(buf[i])) putchar(buf[i]);
			else putchar('.');
		}
		printf("\n");
	}
}
```
##### How the attack works? #####
During this kind of attack, attacker reads past the end of the message they are allowed and hence disclose the private information.

#### Heartbleed ####

##### How the attack works? #####
This bug takes advantage of a feature of the ssl server: heartbeat, which allows the user to send a Heartbleed request to confirm that the connection to the database is alive, and the server returns a heartbeat message. However, the user can specify a longer message length than they actually claim to need when sending the request message, so that everything in the buffer next to the heartbeat message will be read

### Learning Objectives ###

- Explain how a buffer overflow vulnerability can allow an attacker to divert the control flow from the real program code to the instructions placed by the attacker in the buffer(i.e., code injection)

- Explain how a buffer overflow vulnerability can allow an attacker to override variables in the program or to leak data.

- Explain dangling pointer and format string vulnerabilities and how they can be exploited.

- Compare and contrast countermeasures for making exploits of the above vulnerabilities in C and C++ programs harder to execute.

- Explain general idea(s) of Return-Oriented Programming (ROP) and why ROP would be used instead of other (simpler) exploit techniques.

## Math Essential ##

### Modular Arithmetic ###

- figures prominently in the field of public key cryptography

- **x mod n is the remainder of x/n**

  - possible values are through 0 to n-1

  - notation:
    $$
    x\ mod\ n = y \\
    x =  y\ mod\ n \\
    x(mod)\ n = y\\
    x=y(mod\ n)
    $$
    
  - ((a mod n) + (b mod n)) mod n = (a + b) mod n
  
  - ((a mod n)(b mod n)) mod n = ab mod n
  
- **additive inverse of x mod n**

  - denoted as -x mod n
  - what, that in the range of 0 to n-1, that you add to x to get (x + target) mod n = 0
  - -2 mod 6 = 4，4 is the addictive inverse of 2 mod 4
  - (2 + 4) mod 6 = 0

- **multiplicative inverse of x mod n**

  -  what, that in the range of 0 to n - 1, that I multiply x by to get (x * target) mod n = 1
  - $3^{-1}$ mod 7 = 5, because (3 * 5) mod 7 = 1
  - $x^{-1}$ mod y only exist when x and y are relatively prime, easy to find using Euclidean Algorithm

- **Prime**: A number *p* is said to be *prime* if it has no factors other than 1 and *p*

- ***Relatively prime***: two numbers *x* and *y* are ***relatively prime*** if they have no common factor other than 1

- **totient function**: number of integers less than n that are relatively prime to n

  - For any prime number *p*, it's easy to show that $\phi(p)=p-1$
  - If p and q are prime, then $\phi(pq) = (p-1)(q-1)$

### Permutation ###

- building block of ciphers(?)
- Then a ***permutation* of *S*** is an ordered list of the elements of *S,* where each element appears exactly once.
- There are $n!$ permutations for a set consisting n elements

### Probability ###

- For event outcomes $S = \{0, 1, 2, ..., N-1\}$, if each outcome is equally likely, then the probability of the event X, where $X \sub S$, is 
  $$
  P(X) = \frac{\text{number of elements in X}}{\text{number of elements in S}}\\\\
  P(X) = 1 - P(\text{complement of X})\\\\
  P(sum > 3) = 1-P(sum\leq3)
  $$

### Linear Algebra ###

- We write $v \in R^{n}$ to denote a vector containing n components, where each element is a real number: $v = [v_1, v_2, v_3, v_4] = [4, 7/3, 13, -\frac{3}{2}] \in R^{4}$

  - dot product of two vectors, $u, v\in R^{n}$ is $u \dotproduct v=u_1v_1 + u_2v_2 +...+u_nv_n$

- A matrix is an $n\times n$ array of numbers. For example, $A=\begin{bmatrix}3 & 4 & 2\\1 & 7 & 9\end{bmatrix}$ is a $2\times 3$ matrix. We write $A_{2 \times 3}$ to denote that.

- Say matrix A, we use $a_{2, 3}$ to denote 9.

- To **multiply matrix** by a number, we simply multiply each element of the matrix by the number

- **Addition** of matrices only defined for those with the same dimensions.

- **Matrix Multiplication**

  - For two matrices, $A_{m\times n}, B_{k\times l}$, the multiplication only works when $n = k$, and the result dimension of the matrix is $m \times n$
  - 在点乘的时候，用左边的每一行去和右边的每一列做affine
    - 因为做点乘的话至少要align，也就是，左边的每一行（一行有列数个元素）和右边的每一列（一列有行数的元素）align，然后我们在相乘的时候确定了，左边的列数和右边的行数相等

- **Identity Matrix**, $I_{n \times n}$ has 1s on the main diagonal and 0s elsewhere, always square.

  - For a square matrix A, $AI = IA = A$

- Block matrices, where the elements are themselves matrices

  - we can also multiply block matrices:
    $$
    M = \begin{bmatrix}I_{n\times n} & C_{n\times1}\\A_{m\times n}  & B_{m\times 1}\end{bmatrix} and\ V = \begin{bmatrix}U_{n\times l}\\T_{1\times l}\end{bmatrix}
    $$
    In this case, the result is $MV = \begin{bmatrix}X_{n\times l} \\ Y_{m\times l}\end{bmatrix}$, and $X = U + CT$ and $Y = AU + BT$

- Linear independent

  - For vectors $x, y \in R^{n}$, we say that $x$ and $y$ are linearly independent if, for scalar $\alpha, \beta$, that the only solution for $\alpha x+\beta y = 0$ is $\alpha = 0, \beta=0$
  - if a set of vectors are linearly independent, then none of the vectors can be written as a *linear combination* of the other vectors, that is, none of **the vectors can be written as a sum of multiples of the other vectors in the set.** 

### Learning Objectives ###

After studying this module, students should be able to:

1. Find *modular* addition, multiplication, as well as additive and multiplicative inverse of a number.
2. Determine if two numbers are *relatively prime*.
3. Count the number of permutations of a set.
4. Compute the discrete probability of an event or a set of related events (e.g., both dice show even numbers).

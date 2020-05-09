---
layout: post
updated: 2020-05-09 09:33
---

1. Java基础知识
2. 面向对象
3. 常用API
4. 集合I/O
5. 多线程、网络编程、反射、设计模式

这是准备java面试的第二天，以上的分类的思维导图，来自-><a href="https://www.cnblogs.com/java1024/p/8757952.html" target="_blank">这里</a>
- 这里是整理好的面试题，至少都过一遍:
	1. <a href="https://blog.csdn.net/qq_41701956/article/details/86686492">2019年最新java面试题及答案整理上</a>
	2. <a href="https://blog.csdn.net/qq_41701956/article/details/86699263">2019年最新java面试题及答案整理下</a>

### 面向对象(Object Oriented)
- 面向对象是一种程序设计思想之一。面向对象是一种对现实世界理解和抽象的方法，是计算机编程技术发展到一定阶段后的产物。**面向过程是一种以过程为中心的编程思维。这些都是以*什么正在发生为主要目标进行编程。*与面向底箱明显不同的是封装、继承、类**
- 在看完了网上一个很生动的例子，这里写下一些个人的理解。面向对象应该是一个大于面向过程的概念，即面向对象融合了面向过程与对象。为什么这么说呢，在网上现有的对于面向过程的定义一般都如：面向过程指的是一种以事物为中心的编程思想。主要关注的是“怎么做”，即完成任务的具体细节。但是令我非常不解的一点就是：**<u>难道面向对象思想中就不包含一丝面向过程的概念吗？这两个非得一定是互斥对立的吗？</u>**个人认为，面向对象也关注任务的具体细节，但是面向对象把任务的具体细节抽象化，并且把事物分工给了各个对象，只不过，当我们无法再细分，具体到某一个对象的某一个任务的时候，我们不也是“关注任务的具体细节”吗？当不停的出现新的需求，或者同类任务却有不同的小细节时，面向对象就展现出了其优势。
#### 类与对象
- *类与对象是不一样的东西，不过他是存在联系的。***类对某一类事物进行描述，是抽象的；而对象是类的实例，是具象的。对象拥有他这一类的共有的属性，却也有独立与对象个体的属性。**万物皆是对象，当这个对象从一个类被实例化的时候，他就成了对象。打个比方，狗是一个类，狗规定了狗的一些共有性质（脊索动物门，哺乳纲...），而柯基是狗的一个子类，因为它继承了狗的特点，却也衍生出了自己的特点，而你家的养的小柯基jimmy则是一个对象，因为他不再是抽象的了，他是具象的一条狗叫jimmy
- **成员变量（class variable/member variable）**: 
	1. 成员变量定义在类中，在整个类都可以被访问
	2. 成员变量随着对象的建立而建立，随着对象的消失而消失，存在于对象所在的堆内存中。成员变量与对象共存亡。
	3. 成员变量有默认初始化值。
- **局部变量**
	1. 局部变量只定义在局部范围，如函数内、语句内、只在所属的区域有效
	2. 局部变量存于栈内存中（因为只有function call的时候会用到这个局部变量），当方法执行完之后，变量空间会自动释放
	3. 局部变量没有默认初始化值
- 在使用变量时遵循的原则是就近原则，就是现在“局部”范围里面找，没有的话才是取到成员类的位置上找
- 小问题：父类的成员变量子类可不可以访问
- **静态变量**: 指的是使用<code>static</code>修饰符修饰的变量
	1. 静态变量随着类的加载而存在（并不需要实例化），随着类的消失而消失
	2. 静态变量可以被对象调用，还可以被类名字调用
	1. 静态变量的数据储存在方法区（共享数据区）的静态区，所以也叫对象的共享数据
- **匿名对象**: 在实例化的时候没有明确的给出名字的对象。匿名对象只用一次，而且匿名对象只在堆内存中开辟空间，而不存在栈内存的引用。
```java
public class Person {
    public String name; 
    public int age; 
    // 定义构造方法，为属性初始化
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    // 获取信息的方法
    public void tell() {
        System.out.println("姓名：" + name + "，年龄：" + age);
    }
    public static void main(String[] args) {
        new Person("张三", 30).tell(); // 匿名对象，可以看到张三这个对象是没有名字的，直接使用了person类的tell方法
    }
}
```
#### 封装（Encapsulation，这里的解释很多都是从<a href="https://www.cnblogs.com/chenssy/p/3351835.html" target="_blank">chenssy的博客</a>中引用的） 
- 封装从字面上来理解就是包装的意思，专业点就是信息隐藏，是指利用抽象数据类型将数据和基于数据的操作封装在一起，使其构成一个不可分割的独立实体，数据被保护在抽象数据类型的内部，尽可能地隐藏内部的细节，只保留一些对外接口使之与外部发生联系。系统的其他对象只能通过包裹在数据外面的已经授权的操作来与这个封装的对象进行交流和交互。也就是说用户是无需知道对象内部的细节（当然也无从知道），但可以通过该对象对外的提供的接口来访问该对象。  
- 如果用124的定义的化就很简单：Encapsulation is the process of defining a Class that has at least one customizable attribute
- 使用封装的好处：
	1. 良好的封装能够减少耦合（耦合指的是模块及模块之间信息或参数依赖程度）
	2. 类内部的结构可以自由修改
	3. 可以对成员进行更精确的控制
	4. 隐藏信息，实现细节
- 其实这个概念就是相当简单的，封装令一个对象的属性私有化，同时提供一些可以被外界访问的属性的方法，即使是方法，也可以被类封装起来


```java
import java.io.Serializable;

/**
 * A class to store Halloween information.
 * <p>
 * The year, the number of vistors, hourly temperatures in deg C and the weather condition is recorded. This class
 * has been created as a lecture example, and is not otherwise particularly useful!  
 * <p>
 * This version demonstrates the implementation of Comparable (for sorting) and Serializable (for
 * filing).  Also, the mutators for temperature and weather condition have been combined, so both
 * attributes have to be set at the same time.  In this way they cannot be set to an illegal value
 * independently.
 * 
 * @author Alan McLeod
 * @version 3.2
 */
public class Halloween5 implements Comparable<Halloween5>, Serializable {

	private static final long serialVersionUID = 4705089863030936649L;
	private int year;
    private int numMunchkins;
    private int[] temperatures;
    private String weatherCondition;

    /**
     * Full parameter constructor.
	 * 可以看到如果是和类名一样的方法的那他就是个constructor
     * @param yr The year when the data was collected.
     * @param numKids The number of Trick or Treaters!
     * @param temps The air temperatures in degrees Centigrade in an array of int of any size.
     * @param weather The weather condition: "clear", "snow" or "rain".
     * @throws IllegalHalloweenException If arguments are not legal.
     */
    // 4 parameter constructor invokes mutators
    public Halloween5(int yr, int numKids, int[] temps, String weather) throws IllegalHalloweenException {
        setYear(yr);
        setNumMunchkins(numKids);
        setWeather(temps, weather);
    } // end Halloween4 4 parameter constructor

    /**
     * Three parameter constructor.  The weather condition does not have to be supplied.
	 * 利用了方法过载
     * @param yr The year when the data was collected.
     * @param numKids The number of Trick or Treaters.
     * @param temps The air temperatures in degrees Centigrade in an array of int of any size.
     * @throws IllegalHalloweenException if arguments are not legal.
     */
    // 3 parameter constructor invokes 3 parameter constructor with an assumption about the
    // weatherCondition attribute
    public Halloween5(int yr, int numKids, int[] temps) throws IllegalHalloweenException {
        this(yr, numKids, temps, "unknown");
    } // end Halloween4 3 parameter constructor

    /**
     * Sets the year the data was recorded.
     * @param year The calendar year.
     * @throws IllegalHalloweenException if the year does not lie between 1959 and 2016
     */
    public void setYear(int year) throws IllegalHalloweenException {
        if (year < 1950 || year > 2019)
            throw new IllegalHalloweenException("Illegal year: " + year);
        this.year = year;
    } // end year mutator

    /**
     * Sets the number of kids.
     * @param numKids The number of kids arriving at the door.
     * @throws IllegalHalloweenException if the number of kids is less than zero or greater
     * than 500.
     */
    public void setNumMunchkins(int numKids) throws IllegalHalloweenException {
        if (numKids < 0 || numKids > 500)
            throw new IllegalHalloweenException("Illegal number of kids: " + numKids);
        numMunchkins = numKids;
    } // end numMunchkinds mutator

    /**
     * Sets the temperatures array and the weather condition String.  The temperatures are 
     * recorded with one temperature per hour.
     * @param temps An array of temperatures between -30 and 30 degrees C.
     * @param weather The weather condition as a String.
     * @throws IllegalHalloweenException if the condition is not "rain", "snow", "clear" or "unknown",
     * or if the array is empty or any temperatures are not legal. 
     */
    public void setWeather(int[] temps, String weather) throws IllegalHalloweenException {
        double avgTemperature = 0;
        if (temps.length == 0)
            throw new IllegalHalloweenException("No temperatures supplied");
        for (int temperature : temps) {
            if (temperature > 30 || temperature < -30)
                throw new IllegalHalloweenException("Illegal temperature in array: " + temperature);
            avgTemperature += temperature;
        }
        temperatures = temps.clone();
        avgTemperature = Math.round(10 * avgTemperature / temperatures.length) / 10.0;
        if ((weather.equalsIgnoreCase("rain") && avgTemperature > -5) ||
                (weather.equalsIgnoreCase("snow") && avgTemperature < 5) ||
                weather.equalsIgnoreCase("clear") || weather.equalsIgnoreCase("unknown")) {
            weatherCondition = weather;
        } else
            throw new IllegalHalloweenException("Illegal weather/temperature combination: " +
                    weather + ", " + avgTemperature + " deg C.");    	
    } // end setWeather mutator
    
    /**
     * Returns the calendar year the data was recorded.
     * @return The year the data was recorded.
     */
    public int getYear() {
        return year;
    } // end getYear

    /**
     * Returns the number of visitors.
     * @return the number of Trick or Treaters.
     */
    public int getNumMunchkins() {
        return numMunchkins;
    } // end getNumMunchkins Accessor

    /**
     * Returns the temperatures array.
     * @return The temperatures in degrees Centigrade.
     */
    public int[] getTemperatures() {
        return temperatures.clone();
    } // end getTemperature Accessor

    /**
     * Returns the weather condition.
     * @return The weather condition as a String.
     */
    public String getWeatherCondition() {
        return weatherCondition;
    } // end getWeatherCondition Accessor

    /**
     * A String representation of the current object.
     * @return A String representation of the contents of the object containing the values of
     * all the attributes.
     */
    // Overrides (replaces) the toString method of the Object class.
    @Override
    public String toString() {
        String s = "In " + year + " there were " + numMunchkins + " kids. Temperatures each hour were: ";
        for(int i = 0; i < temperatures.length - 1; i++)
            s += temperatures[i] + ", ";
        s += "and " + temperatures[temperatures.length - 1];
        s += " deg C., and the weather was ";
        s += weatherCondition + ".";
        return s;
    } // end toString

    /**
     * Tests two Halloween5 objects for equality.
     * @return <code>true</code> if all the attributes of both objects are exactly equal, <code>false</code>
     * otherwise.
     * @param otherObject The other Halloween5 object.
     */
    // Overrides the equals method of the Object class.
    @Override
    public boolean equals(Object otherObject) {
        if (otherObject instanceof Halloween5) {
            Halloween5 otherH = (Halloween5)otherObject;
            boolean arrayCheck = true;
            if (otherH.temperatures.length != temperatures.length)
                return false;
            for(int i = 0; i < temperatures.length && arrayCheck; i++)
                arrayCheck = temperatures[i] == otherH.temperatures[i];
            if (arrayCheck)
                return year == otherH.year &&
                    numMunchkins == otherH.numMunchkins &&
                    weatherCondition.equalsIgnoreCase(otherH.weatherCondition);
        } // end if
        return false;
    } // end equals

    /**
     * Compares Halloween5 objects on the basis of the number of visitors only.
     * @param otherH The other Halloween5 object.
     * @return A negative <code>int</code> if the supplied object had more vistors, zero if they have the same
     * number and a positive number if the current object has more visitors.
     */
    public int compareTo(Halloween5 otherH) {
        return numMunchkins - otherH.numMunchkins;
    } // end compareTo
    
    /**
     * Returns a copy of the of the current Halloween5 object.
     * @return A copy of the current object.
     */
    // Overrides the clone method in the Object class.
    @Override
    public Halloween5 clone() {
        Halloween5 hwCopy = null;
        try {
            hwCopy = new Halloween5(year, numMunchkins, temperatures, weatherCondition);
        } catch (IllegalHalloweenException e) {
            // Should never get here!
            return null;
        } // end try/catch
        return hwCopy;
    } // end clone
}
```
- 上面就是一个Halloween5的类，他有五个变量其中<code>serialVersionUID</code>是一个静态变量，也就是说别的对象也可以使用
- 构造函数就是constructor，构造函数没有返回值，并且构造函数的名字与类名相同，构造函数也是可以过载的
- <code>this</code>关键字的作用是对当前对象的引用；或者更高级一点的对当前方法所属对象的引用。这个东西在一个类中常见于构造函数内用来区分构造函数的局部变量与类的成员变量

#### 继承(Inheritance)
- 继承是java三大特性之二，它允许创建分等级分层次的类。继承就是子类继承父类的特征和行为，使得子类对象（实例）具有父类的实例域和方法，或子类从父类继承方法，使得子类具有父类相同的行为。

```java
class Person {
    private String name;
    private int age;

    public String getName() {...}
    public void setName(String name) {...}
    public int getAge() {...}
    public void setAge(int age) {...}
}

class Student extends Person {
    // 不要重复name和age字段/方法,
    // 只需要定义新增score字段/方法:
    private int score;

    public int getScore() { … }
    public void setScore(int score) { … }
}
```
- 可以看到以上的代码，student类继承了person类，那么此时person就是student的父类，超类，基类；而student是person的子类，扩展类
- 子类可以直接访问父类中非私有的属性与方法，注意是非私有的，也就是说如果一个属性/方法被<code>private</code>修饰符给修饰了，那么即使是子类也无法访问，但如果是一个加上了<code>protected</code>修饰符的变量/方法，是可以被子类访问的
- **任何类都是Object类的子类**
- *一个类只可以继承自一个类，也就是说，任何类都只有一个父类。但是一个父类却可以有多个子类* 
- 向上转型和向下转型：
	- 向上转型（upcasting）指的是把一个子类类型安全的变为父类类型: <code>Person p = new Student();</code>，注意这个操作是可以的
	- 向下转型（downcasting）指的是令一个引用类型为父类的变量指向其子类，这个操作是不允许的
- <code>super</code>这个关键字可以给子类指向父类，并且在子类的构造函数中，必须符合以下规定：
	1. 每一个构造函数都会默认访问父类的构造函数<code>
	2. **每一个构造函数第一行默认是super()**
	3. 先执行父类的构造函数，再执行自己的
	4. 如果父类没有空参数构造函数，子类必须实打实的使用有参数的构造函数，并且子类可以访问本类其他构造函数，再访问父类的构造函数

	```java
	class Student extends Person {
    protected int score;

    public Student(String name, int age, int score) {
        super(name, age); // 调用父类的构造方法Person(String, int)
        this.score = score;
    }
}
	```
- 方法的重写（override）：指的是子类将父类的方法重新实现，要利用<code>@override</code>关键字，*子类方法的访问权限要大于等于父类方法的访问权限*（不可以父类是public的，然后子类重写了之后来个private），静态方法只可以覆盖静态方法，子类不能覆盖父类私有方法

#### 多态(Polymorphism)
- 从理论的层面上来看：**多态就是指程序中定义的引用变量所指向的具体类型和通过该引用变量发出的方法调用在编程时并不确定，而是在程序运行期间才确定，即一个引用变量倒底会指向哪个类的实例对象，该引用变量发出的方法调用到底是哪个类中实现的方法，必须在由程序运行期间才能决定。因为在程序运行时才确定具体的类，这样，不用修改源程序代码，就可以让引用变量绑定到各种不同的类实现上，从而导致该引用调用的具体方法随之改变，即不修改程序代码就可以改变程序运行时所绑定的具体代码，让程序可以选择多个运行状态，这就是多态性。**
- 先说回之前就讲过的向上转型，即<code>Parent p = new Child();</code>，这一行的意义是：定义了Parent类型的p，这个p指向Child类的对象实例。这样做的好处，也即是他的目的，是因为这个父类引用类型是指向子类的，所以他除了可以引用父类的共性之外，还可以使用子类强大的功能。但是这个upcasting肯定是存在缺陷的，这个缺陷就是：父类类型的引用可以调用**父类中定义的所有属性和方法，对于只存在子类的方法和属性他就望尘莫及了。**也就是说如果一个函数在父类中被定义，在子类中被重写；另一个函数在父类中被定义，在子类中被重载，当我们用upcasting的这个方法定义的父类对象，这个对象会使用父类中的没被重载的函数（因为子类中被重载的函数并没有定义在父类），还有在子类中被重写了的函数（被重写的函数是被定义在父类的）
- 所以统一的对多态的机制进行了一个总结：指向子类的父类由于由于向上转型了，他只能访问父类中拥有的方法和属性，而对于只存在子类中而不存在父类中的方法，他无法引用，即使是在子类中重载的方法也无法使用；但是如果是子类中重写了父类中的某些方法，在调用这些方法的时候，必定是使用子类中定义的这些方法。
- Java实现多态的三个必要条件：
	1. *在多态中必须存在有继承关系的子类和父类*
	2. *子类对父类中某些方法进行重写，那么在调用时就会调用在子类中覆盖的版本*
	3. 在多态中需要将子类的引用赋予给父类对象，只有这样该引用此啊具备技能调用父类的方法和子类的方法
- ***当超类对象引用变量引用子类对象时，被引用对象的类型而不是引用变量的类型决定了调用谁的成员方法，但是这个被调用的方法必须是在超类中定义过的，也就是说被子类覆盖的方法。***
- 多态中的成员特点：
	- 成员变量：编译运行全都是以父类为基准，编译时看父类有没有这个变量；运行时运行父类的变量
	- 成员方法：编译看父类，运行看子类，编译的时候会看父类中有没有这个方法，有的话就编译成功；运行的时候，实际运行的是子类的重写的方法
	- 静态方法：**静态方法是无法被子类override的**，所以一样编译运行都看父类
- 向下转型更具体来说是这样

	```java
	Parent p = new Parent();
	Child c = (Child)p;//注意这是不安全的
	```
以下内容大部分转载自<a href="https://www.cnblogs.com/dolphin0520/p/3811437.html">深入理解Java的接口和抽象类</a>
#### 抽象类(Abstract Class)
- A class which also have concrete method definition and any kind of attribute but it can only be **extended**.
- 要知道什么是抽象类，就要知道什么是抽象方法：<code>abstract void fun();</code>，抽象方法只有方法的声明，却没有具体的实现。如果一个类被<code>abstract</code>这个关键字所修饰，那么这个类是个抽象类，而抽象类中，十有八九有抽象方法（因为如果一个类中没有抽象方法，那么把这个类声明为抽象类也没有什么意义），但是，只要有一个方法是抽象方法，那么这个类就一定是被定义成抽象类的
- 从阿兰的话里也可以读出来的是，抽象类只可以被继承，他是为了继承而存在的，如果定义了抽象类却不去继承他，那么相当于白定义了。如果一个父类中
- 抽象类和普通类的区别
	- 抽象方法只可以为public/protected，如果定义成private/final/static的话就很傻逼了，子类无法重写这个抽象方法，不能被子类继承
	- 抽象类不能用来创建对象
	- 如果一个类继承于一个抽象类，则子类必须实现父类的抽象方法。如果子类没有实现父类的抽象方法，则必须将子类也定义为抽象类

#### 接口(Interface)
- 在JAVA编程语言中是一个特殊的抽象类，但是接口并不是类，因为他不继承于Object。是抽象方法的集合，接口通常以interface来声明。从语义的角度解释，接口泛指供别人调用的方法或者函数，所以接口可以被看作是对行为的抽象。
- 接口是这么样子定义的：<code>interface InterfaceName{}</code>，接口中可以含有 变量和方法。但是要注意，接口中的变量会被隐式地指定为public static final变量（并且只能是public static final变量，用private修饰会报编译错误），而方法会被隐式地指定为public abstract方法且只能是public abstract方法（用其他关键字，比如private、protected、static、 final等修饰会报编译错误），并且接口中所有的方法不能有具体的实现，也就是说，接口中的方法必须都是抽象方法。从这里可以隐约看出接口和抽象类的区别，接口是一种极度抽象的类型，它比抽象类更加“抽象”，并且一般情况下不在接口中定义变量。
- 接口不是类，所以是不可以被类继承(extend)的，但是接口却是可以被implemented的：<code>class ClassName implements Interface1, Interface2,... {}</code>, 可以看到一个类可以遵循多个接口，和抽象类的继承一样，但凡是遵循了某接口的类都必须实现这个接口中定义的抽象方法；如果他不打算实现这个接口中的抽象方法，那么这个类就得是个抽象类。但是对于另一个接口来说，接口是可以继承接口的，并且一个接口是可以继承多个接口的
- 接口和抽象类的区别：
	- 抽象类有构造函数，抽象类的成员方法可以有普通方法和抽象方法，甚至还可以只有普通方法，抽象类的成员变量是很普通的
	- 而接口没有构造函数，接口只可以有抽象方法，接口的成员变量全都是被final修饰的
	- 接口与类的实现方式是多实现，抽象类与类的继承关系是单继承
	- 从意义上来讲，抽象类是对类的抽象，继承了此抽象类的子类，那么子类也是这个抽象类；而接口是对行为的抽象，实现了这个接口的类，只能说他能干到这个接口中的行为，而不能说这个类是这个接口
- 所以当只有部分子类要完成的方法，我们可以直接把它封装到一个接口里面，但是对于全部子类都要实现的方法，应该使用抽象类

#### 内部类(Inner Class)
- 关于内部类的内容多选自<a href="https://www.cnblogs.com/chenssy/p/3388487.html">java提高篇（八）----详解内部类</a>
- A class defined within a class。就是在一个类的内部再定义一个类。里面定义的这个类就叫做内部类。

- 成员内部类（成员内部类是最普通的内部类，它的定义为位于另一个类的内部）
	```java
	class Circle {
    	double radius = 0;
     	
    	public Circle(double radius) {
        	this.radius = radius;
    	}
    	 
    	class Draw {     //内部类
        	public void drawSahpe() {
            	System.out.println("drawshape");
        	}
    	}
	}

	```
	- 内部类可以访问外部类的成员，包括私有的成员，但是如果外部类想要访问内部类的成员，必须要创建内部类对象，才可以访问

- 为什么要使用内部类？**使用内部类最吸引人的原因是：每个内部类都能独立地继承一个接口的实现，所以无论外围类是否已经继承了某个接口的实现，对于内部类没有影响**

```java
public interface Father {

}

public interface Mother {

}

public class Son implements Father, Mother {

}

public class Daughter implements Father{

    class Mother_ implements Mother{
        
    }
}
```
- 以上的实例
- 如果要引用inner class的一些东西的话需要：<code>OuterClass.InnerClass.method</code>

---
layout: post
updated: 2020-05-10 10:22
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

### 集合IO

#### 集合
- 集合是java中的一个大的框架，这个框架上有非常多的东西，首先集合可以分为：
	- Collection集合，collection集合中又可以细分为
		- List集合，list集合又可以细分为
			- ArrayList
			- Vector
			- LinkedList
		- Set集合，set集合又可以细分为
			- HashSet
			- TreeSet
	- Map集合, map集合又可以细分为
		- HashMap
		- TreeMap
		- Hashtable
	- 泛型

##### 泛型(Generic)
- 泛型指的是参数化类型，参数化类型指的就是，我们把数据的类型作为其参数的一种，加了泛型可以让我们避免出现运行时异常，并且强制要求了在集合中只能加入一种类型的数据
- **泛型类**

	```java

	//这就是一个简单的泛型类，当实例化这个类的时候，可以把我们要处理的数据类型，当作是一个参数给传入，具体的例子看下面
	public class Sample<T>{
	
		private T data;
	
		public void setData(T newData){};
		
		public T getData(){};
	}//end Sample<T>

	```
	实例化泛型类`Sample<Integer> num2 = new Sample<>();`，在泛型类定义的时候，是可以在<>里面加入多个类型的。或者说有的时候，希望限制那些被允许传递到一个类型参数的类型种类范围，那么就是使用*bounding有界的类型参数*。**要声明一个有界的类型参数，首先列出类型参数的名称，后跟extends关键字，最后紧跟他的上届**
	
	```java
	<T extends RootClass> //利用extend关键字声明上界，也就是说这个类型只可以是RootClass类及其子类的的
	<T extends RootClass & Pizza> //利用extend关键字声明上界，也就是说这个类型只可以是RootClass类和Pizza类以及他们的子类的的

	<T super Integer> //利用super关键字声明下界，表示参数化类型是此类型的超类型（父类型），直至Object，在这里就是
					  //Integer，Number，Object
	```
	
	在限定类型的时候，不仅仅可以用T，还有别的标识符：
		- E: Element(在集合中使用，因为集合中存放的是元素)
		- T: Type，指的是java类
		- K: Key
		- V: Value
		- N: Number
		- **?: 表示不确定的java类型（无限制通配符类型）**
	
	*使用泛型的好处*（once again）: Object是所有类的根类，任何类的对象都可以设置给该Object引用变量，使用的时候可能需要类型强制转换，但是使用了泛型标识符之后，类型在使用之前就已经确定了，不需要在进行类型强制转换
	- 上界指的是使用了extends的bounding，例如`<? extends T>`，表示参数化类型的可能是T或是T的子类
	- 下界指的是使用了super的bounding，例如`<? super T>`，这个学名叫做超类型限定，表示参数化类型的可能是此类型的超类型，直至Object

- **泛型方法**
	- 泛型方法既可以存在于泛型类中，也可以存在于普通类中。**如果通过泛型方法就可以解决问题，那么应该尽量使用泛型方法**

	```java
	class DataHolder<T>{
    	T item;
    	
    	public void setData(T t) {
    		this.item=t;
    	}
   	 
    	public T getData() {
    		return this.item;
    	}
    	
    	/**
     	* 泛型方法
     	* @param e
     	*/
    	public <E> void PrinterInfo(E e) {
    		System.out.println(e);
    	}
	}

	//作者：dreamGong
	//链接：https://juejin.im/post/5b614848e51d45355d51f792
	//来源：掘金
	//著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
	```
	上面这个就是在一个泛型类中定义了一个泛型方法PrinterInfo，注意在泛型方法中声明的类型参数跟他所处的泛型类的类型参数是独立的，也就是说，我实例化的时候，可以为这个泛型类实例化一个String类型的，但是我们在利用这个对象的泛型方法PrinterInfo的时候，是可以把它应用在Double类型的。
- **泛型接口**
	- 泛型接口就也是一个将类型参数化的接口，他的定义和泛型类的定义很相似

	```java
	public interface Sample<T>{}; //一个未传入实参的泛型接口
	public interface Sample<String>{}; //一个传入实参（String）的泛型接口
	```
	而对于实现了这个接口的类，对于未传入实参和传入实参的泛型接口的处理也是不一样的
	
	```java
	Class class1<T> implements Sample<T>{}; //当一个类实现一个未传入实参的泛型接口时，他自己也变成了泛型类
	Class class2 implements Sample<String>{}; //当一个类实现一个传入实参的泛型接口时，他还是个普通的类
	```
##### Collection集合
- Collection集合包含两大体系：List和Set
###### List
- 存取有序，有索引，可以根据索引来取值，元素可以重复
- ArrayList
	- 底层是使用数组实现的，所以查询速度快，增删速度慢

	```java
	package  //好好学java;
	
	import java.util.ArrayList;
	import java.util.Iterator;
	import java.util.List;
	
	
	public class Test {
    	// 使用ArrayList进行添加和遍历
    	public static void main(String[] args) {
        	List<String> list = new ArrayList<String>();
        	
        	list.add("接口1");
        	list.add("接口2");
        	list.add("接口3");
        	
        	// 第一种遍历方式,使用迭代器
        	Iterator<String> it = list.iterator();
        	while(it.hasNext()){
            	String next = it.next();
            	System.out.println(next);
        	}
        	System.out.println("-------------------");
        	// 第二种遍历方式，使用foreach
        	for (String str : list){
            	System.err.println(str);
        	}
    	}
	
	}
	
	//作者：欧阳思海
	//链接：https://juejin.im/post/5ad82dbef265da503825b240
	//来源：掘金
	//著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
	```
- LinkedList
	- 也就是链表啦，有头有尾一条线，是基于链表结构实现的，查询速度慢，增删速度快，提供了特殊的方法，对头尾的元素操作
	- 以下这个例子是使用了linkedlist来实现栈（栈是先进后出（LIFO），而队列是先进先出（FIFO））

	```java
	package com.xiaoshitou.classtest;

	import java.util.LinkedList;
	
	/**
 	* 利用LinkedList来模拟栈
 	* 栈的特点：先进后出
 	* @author Beck
 	*
 	*/
	public class MyStack {
    	private LinkedList<String> linkList = new LinkedList<String>();
   	 
    	// 压栈
    	public void push(String str){
        	linkList.addFirst(str);
    	}
    	
    	// 出栈
    	public String pop(){
        	return linkList.removeFirst();
    	}
    
    	// 查看
    	public String peek(){
        	return linkList.peek();
    	}
    
    	// 判断是否为空
    	public boolean isEmpty(){
        	return linkList.isEmpty();
    	}
	}
	
	//作者：欧阳思海
	//链接：https://juejin.im/post/5ad82dbef265da503825b240
	//来源：掘金
	//著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
	```
- Vector
	- Vector类实现了一个动态数组，和ArrayList很相似，但是两者是不同的
		- Vector是同步访问的
		- Vector包含了许多传统的方法，这些方法不属于集合框架
		- Vector是线程安全的，ArrayList不是线程安全的
		- ArrayList在底层数组不够用时在原来的基础上扩展0.5倍，Vector是扩展一倍
	- 为什么说Vector是线程安全的呢？因为在Vector的源码里面，凡是比较关键的操作，都使用了<code>synchronized</code>这个关键字，保证了线程的安全性，加了这个关键字的操作，每一次只可以被一个线程执行，而不可以并发执行
###### Set
- 存取无序，元素不可以重复, 无下标Set集合下面有：HashSet，LinkedHashSet，TreeSet
- HashSet
	- 哈希集，每个加入哈希集的元素，都会先用hashcode来生成对这个元素的哈希值，然后根据计算得出的哈希值和数组的长度进行计算出存储的下标；如果下标的位置无元素，那么直接存储，如果有元素的话，使用equals来判断这个位置的这个元素和要存入的元素是不是一样的，如果结果为真，就不存了，因为已经有了，如果结果为假，那么就以链表的形式存在这个位置上

	```java
	package  好好学java;
	
	import java.util.HashSet;
	import java.util.Iterator;
	import java.util.Set;
	
	public class Test {
    	public static void main(String[] args) {
        	// 利用HashSet来存取
        	Set<String> set = new HashSet<String>();
        	
        	set.add("我的天");
        	set.add("我是重复的");
        	set.add("我是重复的");
        	set.add("welcome");
        	
        	// 遍历 第一种方式 迭代器
        	Iterator<String> it = set.iterator();
        	while(it.hasNext()){
            	String str = it.next();
            	System.out.println(str);
        	}
        
        	System.out.println("--------------");
        	for (String str : set){
            	System.out.println(str);
        	}
        	// 打印结果，重复的已经去掉了
        	/*我的天
        	welcome
        	我是重复的
        	--------------
        	我的天
        	welcome
        	我是重复的*/
    	}

	//作者：欧阳思海
	//链接：https://juejin.im/post/5ad82dbef265da503825b240
	//来源：掘金
	//著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
	```
- LinkedHashSet
	- 是一个Set的实现，所以他其中存的不是键值对，而是值，这个东西是HashSet的子类，继承于HashSet，然后是基于LinkedHashMap来实现的
	


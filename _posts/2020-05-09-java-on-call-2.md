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
- 方法的重写（override）：指的是子类将父类的方法重新实现，要利用<code>@override</code>关键字，子类方法的访问权限要大于等于父类方法的访问权限（不可以父类是public的，然后子类重写了之后来个private），静态方法只可以覆盖静态方法，子类不能覆盖父类私有方法

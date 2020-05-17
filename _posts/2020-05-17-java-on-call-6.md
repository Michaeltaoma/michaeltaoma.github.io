---
layout: post
updated: 2020-05-12 17:31
description: Spring框架, AOP, IOC应用, Maven, 主要是关于依赖注入的
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

### Notes of this video
<iframe width="560" height="315" src="https://www.youtube.com/embed/If1Lw4pLLEo" frameborder="0" allowfullscreen></iframe>

- **Dependenct Injection**: 
	- Object depends on other objects.(Dependency) 
	- Coupling（耦合性）：我们追求的是对象间的低耦合性，但是只要我们在一个对象中说new的时候，这个耦合性就会变高了，那为什么高耦合性会不好呢？
		- Coupling的标准定义是：Degree of direct knowledge that one element has of each other. 
		- Tight Coupling:  In general, Tight coupling means the two classes often change together. In other words, if A knows more than it should about the way in which B was implemented, then A and B are tightly coupled.
		- 为什么高耦合性的程序设计不好？In general, Tight Coupling is bad in but most of the time, because it reduces flexibility and re-usability of code, it makes changes much more difficult, it impedes test ability etc.
	- 所以我们不用自己在对象中实例化他的依赖对象，而是通过一个外部的服务，外部的服务帮助注入这个依赖的对象， 这就是依赖注入。
	- 因为在对象中我们写代码的时候不需要实例化对象，所以要让容器知道你要注入什么对象，就需要配置，配置在java Spring框架中有的是用XML来配置的。或者是用Spring Boot，用关键字来声明配置

	```java
	@Component
	class dependingObj implements dependingObjParent{
	//..
	//..
	}

	class Laptop
	{
	@Autowired
	dependingObj obj1;
	}
	```
	- 以上使用了component这个关键字后，这个dependingObj就是一个我们需要注入的对象
	- 使用了autowired之后，框架就会帮助注入你的对象
	- 依赖注入的原因：除了希望设计出松耦合的程序，还有个原因就是在做测试的时候，如果没有依赖注入的话，我们在测试一个对象的时候，同时需要测试他依赖的对象；但是更合理的难道不是依赖的对象测试成功之后，就不需要在测试别的对象的时候重复测试了嘛？有个例子是如果一个对象依赖于一个跟数据库相关的对象，那么难道当我们在测试这个对象的时候，要不停的manipulate这个数据库嘛？如果用松耦合的程序的话就可以用mock class去避免重复测试

- **Maven and 如何用Spring来做依赖注入**:
	- Maven是一个项目构建和管理工具，为开发人员提供了一个项目构建（build）的生命周期框架。
	- 就是当我们在写一个项目的时候，需要用到很多的库，假设你全都把库手动下载到电脑上，是可以的，但是，如果需要更新的时候就裂了。所以Maven这个工具就是，通过声明在Maven中的project中的<code>pom.xml</code>中的需要哪个库，Maven会帮你把这些库给拉进来，像这样声明

	```java
	<!-- https://mvnrepository.com/artifact/org.springframework/spring-web -->
	<dependency>
    	<groupId>org.springframework</groupId>
    	<artifactId>spring-web</artifactId>
    	<version>5.2.6.RELEASE</version>
	</dependency>
	```
	- Maven有一个本地仓，也有一个网络上的仓库，当Maven看到了你需要的dependency之后，Maven会首先搜索本地仓，看看本地仓有没有这个库，如果有的话就直接使用；如果没有的话就会去网络的仓库下载到本地仓中。
	- Maven里面的Archetype可以被看作是一类项目的基本框架
	- GroupID是package name，ArtifactID是项目的名字
	- <code>getBean();</code>是定义在BeanFactory/ApplicationContext接口的方法，这两个接口都是springFramework中，区别是ApplicationContext中有BeanFactory更多的东西，这两个都是IoC容器且BeanFactory是最基础的IoC
	- 注入的流程是首先你得有一个xml文件，这个文件里面定义了你的bean，这个bean声明了要注入的是什么类，像下面这样
	
	```java
	<bean id="vehicle" class="com.taoma.TestMaven2.car"></bean>
	```

	- 然后在你的对象里面，比如你的对象是依赖于上面这个对象的，那么你就得在声明这个对象的时候使用以下的语句

	```java
	ApplicationContext context = new ClassPathXmlApplicationContext("spring.xml");
    	 
    Vehicle newCar = (Vehicle)context.getBean("Vehicle");
	```

	而不再是使用new了

- 依赖注入在java中有三种实现方式，其中一种就是像上面说的用xml去配置，还有种办法是用**Annotation based configurations**，这种方式就是@Component这样的

```java
package com.taoma.TestMaven2;

import org.springframework.stereotype.Component;

@Component
public class Car implements Vehicle {

	public void drive() {
		
		System.out.println("I am TaoMa");
		
	}

}
```
那么此时相应的在xml文件中就应该加上这一行并且把刚刚定义的bean给删除来告诉框架现在使用这种方法来声明

```java
<context:component-scan base-package="com.taoma.TestMaven2"></context:component-scan>
```
- **Spring变量注入**: 像下面这例子，如果Car是一个你要注入的对象，这个对象的声明中含有变量，但是因为是用容器注入，整体的设计思路是松耦合，那么声明一个变量相当于“这个对象是基于这个变量和存在了”，这又把耦合度给提高了，所以容器不会怎么搞这个变量。需要在xml文件中注入这个变量

```java
package com.taoma.TestMaven2;

import org.springframework.stereotype.Component;

@Component
public class Car implements Vehicle {

	Private String brand;

	public void drive() {
		
		System.out.println("I am TaoMa");
		
	}

}

```

注入这个变量，并且可以定义这个值，这就是这个bean的参数（property），使用这个property且定义他的参数就像是用setter一样

```java
	<bean id="vehicle" class="com.taoma.TestMaven2.car">
		<property name="brand" value="Tao"></property>
	</bean>
```

- 当然我们也可以在需要有变量的地方定义一个constructor，然后在xml中就不使用property而是使用以下的语句，这样子的方式叫做Constructor Injection

```java
	<bean id="vehicle" class="com.taoma.TestMaven2.car">
		<constructor-arg value="Tao"></constructor-arg>
	</bean>
```
- 我们编写spring框架的代码的时候，一直遵循着这样的原则：所有在Spring中注入的bean都建议定义成私有的域变量。并且要配套写上get和set方法。以下的例子就是用这种原则编写的代码，其中Car和Office是我们要注入Boss的对象

```java
package com.baobaotao;   
  
public class Boss {   
    private Car car;   
    private Office office;   
  
    // 省略 get/setter   
  
    @Override  
    public String toString() {   
        return "car:" + car + "/n" + "office:" + office;   
    }   
}   

//-------------------------------------------------

<?xml version="1.0" encoding="UTF-8" ?>   
<beans xmlns="http://www.springframework.org/schema/beans"  
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
    xsi:schemaLocation="http://www.springframework.org/schema/beans    
http://www.springframework.org/schema/beans/spring-beans-2.5.xsd">   
    <bean id="boss" class="com.baobaotao.Boss">   
        <property name="car" ref="car"/>   
        <property name="office" ref="office" />   
    </bean>   
    <bean id="office" class="com.baobaotao.Office">   
        <property name="officeNo" value="002"/>   
    </bean>   
    <bean id="car" class="com.baobaotao.Car" scope="singleton">   
        <property name="brand" value=" 红旗 CA72"/>   
        <property name="price" value="2000"/>   
    </bean>   
</beans> 

```

- **Autowired Annotation**：也就是最开始举的例子，使用@Autowired去修饰依赖对象。Autowire注释可以对类成员变量、方法及构造函数进行标注，完成自动装备的工作。Autowire之后，他的代码会变化成以下这样

```java
package com.baobaotao;   
  
public class Boss {   
	@Autowired
    private Car car;   
	@Autowired
    private Office office;   
  
    @Override  
    public String toString() {   
        return "car:" + car + "/n" + "office:" + office;   
    }   
}   

//-------------------------------------------------

<?xml version="1.0" encoding="UTF-8" ?>   
<beans xmlns="http://www.springframework.org/schema/beans"  
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
    xsi:schemaLocation="http://www.springframework.org/schema/beans    
http://www.springframework.org/schema/beans/spring-beans-2.5.xsd">   
    <bean id="boss" class="com.baobaotao.Boss"></bean>   
    <bean id="office" class="com.baobaotao.Office">   
        <property name="officeNo" value="002"/>   
    </bean>   
    <bean id="car" class="com.baobaotao.Car" scope="singleton">   
        <property name="brand" value=" 红旗 CA72"/>   
        <property name="price" value="2000"/>   
    </bean>   
</beans> 

```
把getter和setter可以去掉，并且加上注释。这样，当 Spring 容器启动时，AutowiredAnnotationBeanPostProcessor 将扫描 Spring 容器中所有 Bean，当发现 Bean 中拥有 @Autowired 注释时就找到和其匹配（默认按类型匹配）的 Bean，并注入到对应的地方中去。

- **Annotation Configuration**：就是说之前是从xml文件里面找Bean，不过现在可以定义一个class文件，这个类里面有取的对象的方法，像下面这个一样

```java
package com.taoma.TestMaven2;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.configuration;

@Configuration
public class AppConfig
{
	@Bean
	public Samsung getPhone(){return new Samsung();}
}

//-----------------------------
ApplicationContext context = new ClassPathXmlApplicationContext(AppCongig.class);
    	 
Samsung newCar = (Samsung)context.getBean(Samsung.class);
```
所以这样定义就方便很多了，在配置类写bean，用@Configuration来声明配置类，用@Bean来声明bean的方法，像上面那样
- 然后其实只要被Component修饰了的东西，且在配置类中用@ComponentScan注释，那么这个配置类就相当于自动生成了所有被Component修饰的类的bean，就连上面的<code>getPhone()</code>这种东西都不用写

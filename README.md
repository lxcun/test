一．Java基础
1.1.Java基本特性1
.1、面向对象和面向过程区别
（1）、面向对象。
优点：易维护、易扩展、易复用。由于面向对象有封装、继承、多态性的特性，可以设计出低耦合的系统，使系统更加灵活、更加易于维护。
缺点：程序性能没有面向过程高。
（2）、面向过程
优点：性能高。因为类调用需要实列化，会消耗系统资源。单片机/嵌入式和Unix和Linux采用面向过程编程，性能是重要因素。
缺点：没有面向对象的易复用、易扩展、易维护。
.2、Java语言有哪些特性？
（1）、简单易学
（2）、面向对象（封装、继承、多态）
（3）、平台无关性（与Java虚拟机实现平台无关）
（4）、可靠性
（5）、安全性
（6）、支持多线程编程（C++没有内置的多线程，必须调用操作系统的多线程来实现多线程，而Java提供了多线程支持）
（7）、支持网络编程（Java 语言诞生本身就是为简化网络编程设计的，因此 Java 语言不仅支持网络编程而且很方便）；
（8）、编译和解释并存。
（9）、Java还实现了真数组，避免了覆盖数据的可能。
（10）、Java致力于检查程序在编译和运行时的错误

.3、JDK和JRE？
JDK是Java Development Kit，它是功能齐全的Java SDK。它拥有JRE所拥有的一切，还有编译器（javac）和工具（如javadoc和jdb）。它能够创建和编译程序。
JRE 是 Java运行时环境。它是运行已编译 Java 程序所需的所有内容的集合，包括 Java虚拟机（JVM），Java类库，java命令和其他的一些基础构件。但是，它不能用于创建新程序。如果你只是为了运行一下 Java 程序的话，那么你只需要安装 JRE 就可以了。如果你需要进行一些 Java 编程方面的工作，那么你就需要安装JDK了。但是，这不是绝对的。有时，即使您不打算在计算机上进行任何Java开发，仍然需要安装JDK。例如，如果要使用JSP部署Web应用程序，那么从技术上讲，您只是在应用程序服务器中运行Java程序。那你为什么需要JDK呢？因为应用程序服务器会将 JSP 转换为 Java servlet，并且需要使用 JDK 来编译 servlet。
.4、Java和C++的区别
1、Java 是纯粹的面向对象语言，所有的对象都继承自 java.lang.Object，C++ 为了兼容 C 即支持面向对象也支持面向过程。都是面向对象的语言，都支持封装、继承和多态。
2、Java 不提供指针来直接访问内存，它的引用可以理解为安全指针，程序内存更加安全，而 C++ 具有和 C 一样的指针。
3、Java 的类是单继承的，C++ 支持多重继承；虽然 Java 的类不可以多继承，但是接口可以多继承。
4、Java 通过虚拟机从而实现跨平台特性，但是 C++ 依赖于特定的平台。
5、Java 没有指针，Java 支持自动垃圾回收，有自动内存管理机制，不需要程序员手动释放无用内存
6、Java 不支持操作符重载，虽然可以对两个 String 对象执行加法运算，但是这是语言内置支持的操作，不属于操作符重载，而 C++ 可以。
7、Java 的 goto 是保留字，但是不可用，C++ 可以使用 goto。
8、Java 不支持条件编译，C++ 通过 #ifdef #ifndef 等预处理命令从而实现条件编译。
.5、Java 面向对象编程三大特性: 封装 继承 多态
1、封装
封装把一个对象的属性私有化，同时提供一些可以被外界访问的属性的方法，如果属性不想被外界访问，我们大可不必提供方法给外界访问。但是如果一个类没有提供给外界访问的方法，那么这个类也没有什么意义了。
2、继承
继承是使用已存在的类的定义作为基础建立新类的技术，新类的定义可以增加新的数据或新的功能，也可以用父类的功能，但不能选择性地继承父类。通过使用继承我们能够非常方便地复用以前的代码。
关于继承如下 3 点请记住：
子类拥有父类非 private 的属性和方法。
子类可以拥有自己属性和方法，即子类可以对父类进行扩展。
子类可以用自己的方式实现父类的方法。（以后介绍）。
3、多态
所谓多态就是指程序中定义的引用变量所指向的具体类型和通过该引用变量发出的方法调用在编程时并不确定，而是在程序运行期间才确定，即一个引用变量到底会指向哪个类的实例对象，该引用变量发出的方法调用到底是哪个类中实现的方法，必须在由程序运行期间才能决定。
在Java中有两种形式可以实现多态：继承（多个子类对同一方法的重写）和接口（实现接口并覆盖接口中同一方法）
.6、接口和抽象类的区别
1、接口的方法默认是 public，所有方法在接口中不能有实现(Java 8 开始接口方法可以有默认实现），抽象类可以有非抽象的方法
2、接口中的实例变量默认是 final 类型的，而抽象类中则不一定
3、抽象类可以包含静态方法、构造方法和普通成员变量，而接口不能
3、一个类可以实现多个接口，但最多只能继承一个抽象类
4、一个类实现接口的话要实现接口的所有方法，而抽象类不一定
5、接口不能用 new 实例化，但可以声明，但是必须引用一个实现该接口的对象，从设计层面来说，抽象是对类的抽象，是一种模板设计，接口是行为的抽象，是一种行为的规范。
6、备注:在JDK8中，接口也可以定义静态方法，可以直接用接口名调用。实现类和实现是不可以调用的。如果同时实现两个接口，接口中定义了一样的默认方法，必须重写，不然会报错。(详见issue:https://github.com/Snailclimb/JavaGuide/issues/146)
.7、成员变量与局部变量的区别有那些
1、从语法形式上，看成员变量是属于类的，而局部变量是在方法中定义的变量或是方法的参数；成员变量可以被 public,private,static 等修饰符所修饰，而局部变量不能被访问控制修饰符及 static 所修饰；但是，成员变量和局部变量都能被 final 所修饰；
2、从变量在内存中的存储方式来看:如果成员变量是使用static修饰的，那么这个成员变量是属于类的，如果没有使用使用static修饰，这个成员变量是属于实例的。而对象存在于堆内存，局部变量存在于栈内存。
3、从变量在内存中的生存时间上看:成员变量是对象的一部分，它随着对象的创建而存在，而局部变量随着方法的调用而自动消失。
4、成员变量如果没有被赋初值:则会自动以类型的默认值而赋值（一种情况例外被 final 修饰的成员变量也必须显示地赋值）；而局部变量则不会自动赋值。
.8、hashCode 与 equals (重要)
1、hashCode（）介绍
hashCode() 的作用是获取哈希码，也称为散列码；它实际上是返回一个int整数。这个哈希码的作用是确定该对象在哈希表中的索引位置。hashCode() 定义在JDK的Object.java中，这就意味着Java中的任何类都包含有hashCode() 函数。
散列表存储的是键值对(key-value)，它的特点是：能根据“键”快速的检索出对应的“值”。这其中就利用到了散列码！（可以快速找到所需要的对象）
2、为什么要有 hashCode，我们以“HashSet 如何检查重复”为例子来说明为什么要有 hashCode：
当你把对象加入 HashSet 时，HashSet 会先计算对象的 hashcode 值来判断对象加入的位置，同时也会与其他已经加入的对象的 hashcode 值作比较，如果没有相符的hashcode，HashSet会假设对象没有重复出现。但是如果发现有相同 hashcode 值的对象，这时会调用 equals（）方法来检查 hashcode 相等的对象是否真的相同。如果两者相同，HashSet 就不会让其加入操作成功。如果不同的话，就会重新散列到其他位置。（摘自我的Java启蒙书《Head first java》第二版）。这样我们就大大减少了 equals 的次数，相应就大大提高了执行速度。
3、hashCode（）与equals（）的相关规定
如果两个对象相等，则hashcode一定也是相同的
两个对象相等,对两个对象分别调用equals方法都返回true
两个对象有相同的hashcode值，它们也不一定是相等的
因此，equals 方法被覆盖过，则 hashCode 方法也必须被覆盖
hashCode() 的默认行为是对堆上的对象产生独特值。如果没有重写 hashCode()，则该 class 的两个对象无论如何都不会相等（即使这两个对象指向相同的数据）
.9、== 与 equals(重要)
== : 它的作用是判断两个对象的地址是不是相等。即，判断两个对象是不是同一个对象。(基本数据类型==比较的是值，引用数据类型==比较的是内存地址)
equals() : 它的作用也是判断两个对象是否相等。但它一般有两种使用情况：
情况1：类没有覆盖 equals() 方法。则通过 equals() 比较该类的两个对象时，等价于通过“==”比较这两个对象。
情况2：类覆盖了 equals() 方法。一般，我们都覆盖 equals() 方法来两个对象的内容相等；若它们的内容相等，则返回 true (即，认为这两个对象相等)。
说明：
String 中的 equals 方法是被重写过的，因为 object 的 equals 方法是比较的对象的内存地址，而 String 的 equals 方法比较的是对象的值。
当创建 String 类型的对象时，虚拟机会在常量池中查找有没有已经存在的值和要创建的值相同的对象，如果有就把它赋给当前引用。如果没有就在常量池中重新创建一个 String 对象。
.10、关于 final 关键字的一些总结
final关键字主要用在三个地方：变量、方法、类。
1、对于一个final变量，如果是基本数据类型的变量，则其数值一旦在初始化之后便不能更改；如果是引用类型的变量，则在对其初始化之后便不能再让其指向另一个对象。
2、当用final修饰一个类时，表明这个类不能被继承。final类中的所有成员方法都会被隐式地指定为final方法。
3、使用final方法的原因有两个。第一个原因是把方法锁定，以防任何继承类修改它的含义；第二个原因是效率。在早期的Java实现版本中，会将final方法转为内嵌调用。但是如果方法过于庞大，可能看不到内嵌调用带来的任何性能提升（现在的Java版本已经不需要使用final方法进行这些优化了）。类中所有的private方法都隐式地指定为final。
.11、BIO、NIO和AIO区别
1）BIO：就是阻塞IO，每个TCP连接进来服务端都需要创建一个线程来建立连接并进行消息的处理。如果中间发生了阻塞(比如建立连接、读数据、写数据时发生阻碍)，线程也会发生阻塞，并发情况下，N个连接需要N个线程来处理。
2）NIO：也就是非阻塞IO，是基于事件驱动的思想(Reactor线程模型)。对比于BIO来说，NIO使用一个线程来管理所有的Socket 通道，也就是基于Selector机制，当查询到事件时(连接、接受连接、读、写)，就会转发给不同的处理线程(handler)。
3）AIO：异步非阻塞IO，AIO在进行读写操作时，只需要调用相应的read/write方法，并传入CompletionHandler(动作完成时处理器)，在动作完成后会调用CompletionHandler。 
.12、如果我们在finally块中改变某个返回值的变量的值，最后的return结果会变吗？
不会，比如下面的例子：
public static int i=0;
public static int testtest(){
    try {
        i=10;
        System.out.println("try");
        return i;
    }finally {
        i=100;
        System.out.println("finally: " + i);
    }
}
@org.junit.Test
public void test1(){
    System.out.println("test:"+ testtest());

    System.out.println(“i= ”i);

}
输出就是：
try
finally: 100
test:10
i= 100
根据输出我们就可以知道： 在执行return 操作的时候，其实return的值就已经准备好了（这里的准备好了应该类似于副本），无论你在finally怎么对变量改变都不会影响return的值。
.13、静态内部类和非静态内部类的区别？
1）java允许我们在一个类里面定义静态内部类（nested class），把nested class封闭起来的类叫外部类。在java中，我们不能用static修饰顶级类（top level class）。只有内部类可以为static。
2）静态内部类和非静态内部类之间到底有什么不同呢？
①静态内部类不需要有指向外部类的引用。但非静态内部类需要持有对外部类的引用。
②静态内部类不能访问外部类的非静态成员，他只能访问外部类的静态成员。
非静态内部类能够访问外部类的静态和非静态成员。
③一个非静态内部类不能脱离外部类实体被创建，必须通过外部类的引用创建实例。一个非静态内部类可以访问外部类的数据和方法，因为他就在外部类里面。

.14、Java的反射作用原理与作用
1、原理：在程序运行的时候能够获取自身的的Class信息，比如属性和方法，且能够调用它的任意的方法和属性，这就为Java提供了动态的特性。
2、Java反射的作用：
①. 在运行时判断任意一个对象所属的类； 
②. 在运行时构造任意一个类的对象； 
③. 在运行时判断任意一个类所具有的成员变量和方法； 
④. 在运行时调用任意一个对象的方法； 
⑤. 生成动态代理。
.15、Java的动态代理怎么理解？
1、Java的动态代理可以动态的创建代理并动态的处理对所代理方法的调用。
2、在动态代理上所做的所有调用都会被重定向到单一的调用处理器上，它的工作是揭示调用的类型并确定相应的对策。
3、常规套路是向调用处理器的构造器传递一个“实际”对象的引用，从而使得调用处理器在执行其中介任务时，可以将请求转发。
.16、Java中线程有哪些状态，怎么转换的？
.17、final关键字与参数传递特点
1.final 类。表示该类不可继承,
2.final 方法。表示该方法不可被覆盖
3.final 域。表示该字段一被初始化就不能再改变(必须确保在构造器执行之后final域均被设置,且不可改变)
final用于基本类型和不可变类型,对象类型不可变的只是引用没有意义
4.final 参数。表示在作用域里只能读取不能赋值该final变量
参数传递	
Java传递是"值传递":
1.基础类型+布尔。是把变量copy了一份传给函数,对原变量无影响
2.对象类型。是把改引用copy了一份(新旧引用指向同一对象),
　　a.在函数内部对新引用的赋值操作不会影响原引用的指向以及指向的对象
　　b.在函数内部对新引用进行对象改变属性操作,不会影响原引用的指向,但是会影响原引用指向的对象
基础类型和对象类型传递的都是值,只是一个是值本身,一个是引用
.18、Object类有哪些方法，分别是什么作用？
1）protected Object clone()  创建并返回此对象的一个副本。（浅克隆）
2）boolean equals(Object obj)  指示其他某个对象是否与此对象“相等”。   
3）protected void finalize()  当垃圾回收器确定不存在对该对象的更多引用时，由对象的垃圾回收器调用此方法。   
4）Class<?> getClass()返回此Object的运行时类对象。   
5）int hashCode()  返回该对象的哈希码值。   
6）void notify()  唤醒在此对象监视器上等待的单个线程。   
7）void notifyAll()  唤醒在此对象监视器上等待的所有线程。   
8）String toString()  返回该对象的字符串表示。   
9）void wait() 在其他线程调用此对象notify()方法或 notifyAll()方法前，导致当前线程等待。   
10）void wait(long timeout)  在其他线程调用此对象的 notify() 方法或 notifyAll() 方法，或者超过指定的时间量前，导致当前线程等待。   
11）void wait(long timeout, int nanos)  在其他线程调用此对象的 notify() 方法或 notifyAll() 方法，或者其他某个线程中断当前线程，或者已超过某个实际时间量前，导致当前线程等待。
.19、继承和实现接口，方法覆盖遵循原则？
两同两小一大原则：
方法名相同，参数类型相同
子类返回类型小于等于父类方法返回类型， 
子类抛出异常小于等于父类方法抛出异常， 
子类访问权限大于等于父类方法访问权限。
1、子类构造函数调用父类构造函数用super
2、子类重写父类方法后，若想调用父类中被重写的方法，用super
3、未被重写的方法可以直接调用。
4、编译看左边，运行看右边->Base base = new Son();
1、Java 中单实现通过 implements 关键字，多实现通过 extends 关键字
2、Java 中单继承通过 extends 关键字，没有多继承
3、如果同时出现继承和实现，则必须先继承（extends）再实现（implements）
.20、java concurrent包下的4个类，差别最大的一个
A、Semaphore：类，控制某个资源可被同时访问的个数;
B、ReentrantLock：类，具有与使用synchronized方法和语句所访问的隐式监视器锁相同的一些基本行为和语义，但功能更强大；
C、 Future：接口，表示异步计算的结果；
D、 CountDownLatch：类，可以用来在一个线程中等待多个线程完成任务的类。
.21、构造器 Constructor 是否可被 override
在讲继承的时候我们就知道父类的私有属性和构造方法并不能被继承，所以 Constructor 也就不能被 override（重写）,但是可以 overload（重载）,所以你可以看到一个类中有多个构造函数的情况。
.22、方法的重写规则
1）参数列表必须完全与被重写方法的相同；
2）返回类型必须完全与被重写方法的返回类型相同；（备注:这条信息是标准的重写方法的规则,但是在java 1.5 版本之前返回类型必须一样,1.5(包含)j 版本之后java放宽了限制,返回类型必须小于或者等于父类方法的返回类型 ）。才有了
子类返回类型小于等于父类方法返回类型。在java里面这个怎么样都是正确的,请小伙伴谨记。
3）访问权限不能比父类中被重写的方法的访问权限更低。例如：如果父类的一个方法被声明为public，那么在子类中重写该方法就不能声明为protected。
4）父类的成员方法只能被它的子类重写。
5）声明为final的方法不能被重写。
6）声明为static的方法不能被重写，但是能够被再次声明。
7）子类和父类在同一个包中，那么子类可以重写父类所有方法，除了声明为private和final的方法。
8）子类和父类不在同一个包中，那么子类只能够重写父类的声明为public和protected的非final方法。
9）重写的方法能够抛出任何非强制异常，无论被重写的方法是否抛出异常。但是，重写的方法不能抛出新的强制性异常，或者比被重写方法声明的更广泛的强制性异常，反之则可以。
10）构造方法不能被重写。
11）如果不能继承一个方法，则不能重写这个方法。
.22、Java关键字
abstract                continue           for            new             
switch                  default            if             package         
synchronized            do                 goto           private         
this                    break              double         implements       
protected               throw              byte           else             
import                  public             throws         case            
enum                    instanceof         return         transient      
catch                   extends            int            short           
try                     char               final          interface       
static                  void               class          finally         
long                    strictfp           volatile       const          
float                   native             super          while           
boolean                 assert 
.23、Java内部类
1、内部类不能被public、private、static修饰；
2、在外部类中不能创建内部类的实例；
3、创建内部类的实例只能在包含他的方法中；
4、内部类访问包含他的方法中的变量必须有final修饰；
5、外部类不能访问局部内部类，只能在方法体中访问局部内部类，且访问必须在内部类定义之后。
6、一个.java文件中定义多个类
(1) public权限类只能有一个（也可以一个都没有，但最多只有一个）；
(2)这个.java文件名只能是public 权限的类的类名；
(3)倘若这个文件中没有public 类，则它的.java文件的名字是随便的一个类名；
(4)当用javac命令生成编译这个.java 文件的时候，则会针对每一个类生成一个.class文件；
.24、Swing的顶层容器
Swing提供三个顶层容器类：JFrame，JDialog和JApplet。
.25、Java运算符优先级
.26、Java文件处理
1.FileInputStream :获取文件字节流，获取对文件读取；
2.FileReader提供对文件的字符获取
3.FileWriter提供对文件的字符写入
4.File提供对文件的基本操作，删除，创建，文件路径等
.27、JDK中提供的ClassLoader
三大类加载器，启动类加载器，扩展类加载器，应用程序类加载器，应用程序类加载器又叫系统类加载器。
Bootstrap ClassLoader，主要加载JVM自身工作需要的类。
Extension ClassLoader，主要加载%JAVA_HOME%\lib\ext目录下的库类。
Application ClassLoader，主要加载Classpath指定的库类，一般情况下这是程序中的默认类加载器，也是ClassLoader.getSystemClassLoader() 的返回值。（这里的Classpath默认指的是环境变量中配置的Classpath，但是可以在执行Java命令的时候使用-cp 参数来修改当前程序使用的Classpath）
JVM加载类的实现方式，我们称为双亲委托模型：
如果一个类加载器收到了类加载的请求，他首先不会自己去尝试加载这个类，而是把这个请求委托给自己的父加载器，每一层的类加载器都是如此，因此所有的类加载请求最终都应该传送到顶层的Bootstrap ClassLoader中，只有当父加载器反馈自己无法完成加载请求时，子加载器才会尝试自己加载。
双亲委托模型的重要用途是为了解决类载入过程中的安全性问题。
假设有一个开发者自己编写了一个名为Java.lang.Object的类，想借此欺骗JVM。现在他要使用自定义ClassLoader来加载自己编写的java.lang.Object类。然而幸运的是，双亲委托模型不会让他成功。因为JVM会优先在Bootstrap ClassLoader的路径下找到java.lang.Object类，并载入它。
.28、 java 中的 Math.round(-1.5) 等于多少？
等于 -1，因为在数轴上取值时，中间值（0.5）向右取整，所以正 0.5 是往上取整，负 0.5 是直接舍弃
.29、普通类和抽象类有哪些区别？
普通类不能包含抽象方法，抽象类可以包含抽象方法。
抽象类不能直接实例化，普通类可以直接实例化。
.30、抽象类能使用 final 修饰吗？
不能，定义抽象类就是让其他类继承的，如果定义为 final 该类就不能被继承，这样彼此就会产生矛盾，所以 final 不能修饰抽象类，编辑器也会提示错误信息。
.31、 java 中 IO 流分为几种？
按功能来分：输入流（input）、输出流（output）。
按类型来分：字节流和字符流。
字节流和字符流的区别是：字节流按 8 位传输以字节为单位输入输出数据，字符流按 16 位传输以字符为单位输入输出数据。
.32、Files的常用方法都有哪些？
①Files.exists()：检测文件路径是否存在。
②Files.createFile()：创建文件。
③Files.createDirectory()：创建文件夹。
④Files.delete()：删除一个文件或目录。
⑤Files.copy()：复制文件。
⑥Files.move()：移动文件。
⑦Files.size()：查看文件个数。
⑧Files.read()：读取文件。
⑨Files.write()：写入文件。
.33、File类的常用方法和说明
1.访问文件名相关方法
①String getName(); 返回此File对象所表示的文件名和路径名（如果是路径，则返回最后一级子路径名）。
②String getPath(); 返回此File对象所对应的路径名。
③File getAbsolutePath(); 返回此File对象所对应的绝对路径名。
④String getParent(); 返回此File对象所对应目录（最后一级子目录）的父路径名。
⑤boolean renameTo(File newName); 重命名此File对象所对应的文件或目录，如果重命名成功，则返回true:否则返回false.
2.文件检测相关方法
①boolean exists(); 判断File对象所对应的文件或目录是否存在。
②boolean canRead(); 判断File对象所对应的目录或文件是否可读。
③boolean isFile(); 判断File对象所对应的是否是文件，而不是目录。
④boolean isDirectory(); 判断File对象所对应的是否是目录，而不是文件。
⑤boolean isAbsolute(); 判断File对象所对应的文件或目录是否是绝对路径。该方法消除了不同平台的差异，可以直接判断File对象是否为绝对路径。在UNIX/Linux/BSD等系统上，如果路径名开头是一条斜线（/）,则表明该File对象对应一个绝对路径；在Windows等系统上，如果路径开头是盘符，则说明它是绝对路径。
3.获取常规文件信息
①long lastModified(); 返回文件最后修改时间。
②long length(); 返回文件内容的长度。
4.文件操作相关的方法
①boolean createNewFile(); 当此File对象所对应的文件不存在时，该方法将新建的一个该File对象所指定的新文件，如果创建成功则返回true；否则返回false.
②boolean delete(); 删除File对象所对应的文件或路径。
③static File CreateTempFile(String prefix,String suffix);在默认的临时文件目录创建一个临时空文件，使用给定前缀、系统生成的随机数和给定后缀作为文件名。这是一个静态方法，可以直接通过File来调用。preFix参数必须至少是3个字节长。建议前缀使用一个短的、有意义的字符串。建议前缀使用一个短的、有意义的字符串，比如”hjb“ 或”main”. suffix参数可以为null,在这种情况下，将使用默认的后缀”.tmp”.
④static File CreateTempFile(String prefix,String suffix,File directory);在directory所指定的目录中创建一个临时空文件，使用给定前缀、系统生成的随机数和给定后缀作为文件名。这是一个静态方法，可以直接通过File来调用。
⑤void deleteOnExit(); 注册一个删除钩子，指定当Java虚拟机退出时，删除File对象随对应的文件和目录。
5.目录操作相关方法
①boolean mkdir(); 试图创建一个File对象所对应的目录，如果创建成功，则返回true;否则返回false. 调用该方法时File对象必须对应一个路径，而不是一个文件。
②String[] list(); 列出File对象的所有子文件名和路径名，返回String数组。
③File[] listFiles(); 列出File对象的所有子文件和路径，返回File数组。
④static File[] listRoots(); 列出系统所有的根路径。这是一个静态方法，可以直接通过File类来调用。
http://blog.csdn.net/nightcurtis/article/details/51385934

.34、什么是 java 序列化？什么情况下需要序列化？ 
简单说就是为了保存在内存中的各种对象的状态（也就是实例变量，不是方法），并且可以把保存的对象状态再读出来。虽然你可以用你自己的各种各样的方法来保存object states，但是Java给你提供一种应该比你自己好的保存对象状态的机制，那就是序列化。
什么情况下需要序列化：
a）当你想把的内存中的对象状态保存到一个文件中或者数据库中时候；
b）当你想用套接字在网络上传送对象的时候；
c）当你想通过RMI传输对象的时候；
.35、动态代理是什么？有哪些应用？
动态代理：
当想要给实现了某个接口的类中的方法，加一些额外的处理。比如说加日志，加事务等。可以给这个类创建一个代理，故名思议就是创建一个新的类，这个类不仅包含原来类方法的功能，而且还在原来的基础上添加了额外处理的新类。这个代理类并不是定义好的，是动态生成的。具有解耦意义，灵活，扩展性强。
动态代理的应用：
Spring的AOP
加事务;
加权限;
加日志。
.36、怎么实现动态代理？
首先必须定义一个接口，还要有一个InvocationHandler(将实现接口的类的对象传递给它)处理类。再有一个工具类Proxy(习惯性将其称为代理类，因为调用他的newInstance()可以产生代理对象,其实他只是一个产生代理对象的工具类）。利用到InvocationHandler，拼接代理类源码，将其编译生成代理类的二进制码，利用加载器加载，并将其实例化产生代理对象，最后返回。
.37、为什么要使用克隆？
想对一个对象进行处理，又想保留原有的数据进行接下来的操作，就需要克隆了，Java语言中克隆针对的是类的实例。
.38、如何实现对象克隆？
有两种方式：
1). 实现Cloneable接口并重写Object类中的clone()方法；
2). 实现Serializable接口，通过对象的序列化和反序列化实现克隆，可以实现真正的深度克隆。
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;
public class MyUtil {
    private MyUtil() {
        throw new AssertionError();
    }
    @SuppressWarnings("unchecked")
    public static <T extends Serializable> T clone(T obj) throws Exception {
        ByteArrayOutputStream bout = new ByteArrayOutputStream();
        ObjectOutputStream oos = new ObjectOutputStream(bout);
        oos.writeObject(obj);
ByteArrayInputStream bin = new ByteArrayInputStream(bout.toByteArray());
        ObjectInputStream ois = new ObjectInputStream(bin);
        return (T) ois.readObject();
        // 说明：调用ByteArrayInputStream或ByteArrayOutputStream对象的close方法没有任何意义
        // 这两个基于内存的流只要垃圾回收器清理对象就能够释放资源，这一点不同于对外部资源（如文件流）的释放
    }
}
注意：基于序列化和反序列化实现的克隆不仅仅是深度克隆，更重要的是通过泛型限定，可以检查出要克隆的对象是否支持序列化，这项检查是编译器完成的，不是在运行时抛出异常，这种方案是明显优于使用Object类的clone方法克隆对象。让问题在编译的时候暴露出来总是好过把问题留到运行时。
.37、为什么要使用克隆？
想对一个对象进行处理，又想保留原有的数据进行接下来的操作，就需要克隆了，Java语言中克隆针对的是类的实例。
.38、如何实现对象克隆？
有两种方式：
1). 实现Cloneable接口并重写Object类中的clone()方法；
2). 实现Serializable接口，通过对象的序列化和反序列化实现克隆，可以实现真正的深度克隆。
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;
public class MyUtil {
    private MyUtil() {
        throw new AssertionError();
    }
    @SuppressWarnings("unchecked")
    public static <T extends Serializable> T clone(T obj) throws Exception {
        ByteArrayOutputStream bout = new ByteArrayOutputStream();
        ObjectOutputStream oos = new ObjectOutputStream(bout);
        oos.writeObject(obj);
ByteArrayInputStream bin = new ByteArrayInputStream(bout.toByteArray());
        ObjectInputStream ois = new ObjectInputStream(bin);
        return (T) ois.readObject();
        // 说明：调用ByteArrayInputStream或ByteArrayOutputStream对象的close方法没有任何意义
        // 这两个基于内存的流只要垃圾回收器清理对象就能够释放资源，这一点不同于对外部资源（如文件流）的释放
    }
}
注意：基于序列化和反序列化实现的克隆不仅仅是深度克隆，更重要的是通过泛型限定，可以检查出要克隆的对象是否支持序列化，这项检查是编译器完成的，不是在运行时抛出异常，这种方案是明显优于使用Object类的clone方法克隆对象。让问题在编译的时候暴露出来总是好过把问题留到运行时。
.39、深拷贝和浅拷贝区别是什么？
浅拷贝只是复制了对象的引用地址，两个对象指向同一个内存地址，所以修改其中任意的值，另一个值都会随之变化，这就是浅拷贝（例：assign()）。
深拷贝是将对象及值复制过来，两个对象修改其中任意的值另一个值不会改变，这就是深拷贝（例：JSON.parse()和JSON.stringify()，但是此方法无法复制函数类型）。
.40、final、finally、finalize 有什么区别？
final可以修饰类、变量、方法，修饰类表示该类不能被继承、修饰方法表示该方法不能被重写、修饰变量表示该变量是一个常量不能被重新赋值。
finally一般作用在try-catch代码块中，在处理异常的时候，通常我们将一定要执行的代码方法finally代码块中，表示不管是否出现异常，该代码块都会执行，一般用来存放一些关闭资源的代码。
finalize是一个方法，属于Object类的一个方法，而Object类是所有类的父类，该方法一般由垃圾回收器来调用，当我们调用System的gc()方法的时候，由垃圾回收器调用finalize(),回收垃圾。 
.41、抽象类和接口可以用的修饰符？
1、抽象类中的抽象方法（其前有abstract修饰）不能用final、private、static、synchronized、native访问修饰符修饰。原因如下：定义抽象类就是让其他类继承的，如果定义为 final 该类就不能被继承，这样彼此就会产生矛盾，所以 final 不能修饰抽象类，编辑器也会提示错误信息；抽象方法没有方法体，是用来被继承的，所以不能用private修饰；static修饰的方法可以通过类名来访问该方法（即该方法的方法体），抽象方法用static修饰没有意义；使用synchronized关键字是为该方法加一个锁。而如果该关键字修饰的方法是static方法。则使用的锁就是class变量的锁。如果是修饰类方法。则用this变量锁。但是抽象类不能实例化对象，因为该方法不是在该抽象类中实现的。是在其子类实现的。所以。锁应该归其子类所有。所以。抽象方法也就不能用synchronized关键字修饰了；native，这个东西本身就和abstract冲突，他们都是方法的声明，只是一个吧方法实现移交给子类，另一个是移交给本地操作系统。如果同时出现，就相当于即把实现移交给子类，又把实现移交给本地操作系统，那到底谁来实现具体方法呢？
2、接口是一种特殊的抽象类，接口中的方法全部是抽象方法（但其前的abstract可以省略），所以抽象类中的抽象方法不能用的访问修饰符这里也不能用。而且protected访问修饰符也不能使用，因为接口可以让所有的类去实现（非继承），不只是其子类，但是要用public去修饰。接口可以去继承一个已有的接口。
.42、类、方法、成员变量和局部变量的可用修饰符？
一．类
类的修饰符：
Public:可以在其他任何类中使用，默认为统一包下的任意类。
Abstract:抽象类，不能被实例化，可以包含抽象方法，抽象方法没有被实现，无具体功能，只能衍生子类。
Final:不能被继承。
二．变量
变量修饰符：
一个类的成员变量的声明必须在类体中，而不能在方法中，方法中声明的是局部变量。
1.可访问修饰符：
2.static：类变量：一个类所拥有的变量，不是类的每个实例有的变量。类变量是指不管类创建了多少对象，系统仅在第一次调用类的时候为类变量分配内存，所有对象共享该类的类变量，因此可以通过类本身或者某个对象来访问类变量。
3.final：常量。
4. volatile：声明一个可能同时被并存运行的几个线程所控制和修改的变量。
实例变量：和类变量对应，即每个对象都拥有各自独立的实例变量。
三．方法：（和变量对象分为实例方法和类方法，并用有无static修饰区别）
类方法：使用static关键字说明的方法
1.第一次调用含类方法的类是，系统只为该类创建一个版本，这个版本被该类和该类的所有实例共享。
2.类方法只能操作类变量，不能访问实例变量。类方法可以在类中被调用，不必创建实例来调用，当然也可以通过对象来调用。
实例方法：实例方法可以对当前对象的实例变量操作，而且可以访问类变量。
方法可以重载，要求：方法名相同，但是参数必须有区别。（参数不同可以使类型不同，顺序不同，个数不同）
方法的返回类型：若无返回类型，则声明为void.
方法中的变量作用域：
1.成员变量：整个类。
2.局部变量：定义起到方法块结束为止。
3.方法参数：整个方法或者构造方法。
4.异常处理参数：参数传递给异常处理方法。
构造方法：和类同名的方法。为新建对象开辟内存空间后，用于初始化新建的对象。不能用对象显式的调用。
静态初始化器：格式：static{<赋值语句组>}
静态初始化器与构造方法的区别： 
静态初始化器
构造方法
对类的静态域初始化
对新建的对象初始化
类进入内存后，系统调用执行
执行new后自动执行
属特殊语句（仅执行一次）
属特殊方法
方法的修饰符：
抽象方法：用abstract修饰，只有声明部分，方法体为空，具体在子类中完成。
类方法：静态方法，用static修饰，
1.调用时，使用类名作为前缀，而不是类的某个实例对象名
2.不能被单独对象拥有，属于整个类共享。
3.不能处理成员变量。
最终方法：用final修饰，不能被子类重新定义的方法。
本地方法：用native修饰的方法，表示用其他语言书写的特殊方法，包括C，C++，FORTRAN，汇编语言等。
四．类成员的访问控制符：
即类的方法和成员变量的访问控制符，一个类作为整体对象不可见，并不代表他的所有域和方法也对程序其他部分不可见，需要有他们的访问修饰符判断。
1.2.Java基本特性2
.1、Lanbda表达式？
Lanbda表达式的主要作用就是代替匿名内部类的繁琐语法， 它由三部分组成：
（1） 形参列表。形参列表允许省略形参类型。如果形参列表中只有一个参数，甚至连形参列表的圆括号也可以省略。
（2） 箭头（→）。必须通过英文中画线和大于符号组成。
（3）代码块。如果代码块只包含一条语句，Lambda表达式允许省略代码块的花括号，那么那条语句就不要用花括号表示语句结束。Lambda代码块只有一条return语句，甚至可以省略return关键字。Lambda表达式需要返回值，而它的代码块中仅有一套省略了return的语句。Lambda表达式会自动返回这条语句的值。
lamdda中，箭头左边表示的是参数，右边表示的是方法体。
若无参无返回值，左边为()
若只有一个参数，左边为(参数a)，也可以直接将括号省略。
若有两个参数，左边为(参数a,参数b)
若方法体中只有一条语句，可省略大括号和return。
1.3.Java数据类型
.1、String、StringBuffer、StringBuilder区别？
1）在JDK源码中，String类是被修饰成final的，所以String类是不可变的。我们对于String对象的操作都会返回一个新的String对象。所以对String进行字符串的拼接的时候会创建大量的String实例对象，这是一个非常耗时的操作，所以String直接拼接字符串效率很低。
2）StringBuffer和StringBuilder是可变的。他们两个都是继承于AbstractStringBuilder，内部是基于char[]字符数组实现的，其对于字符串的拼接等操作是基于数组，所以效率很高。此外StringBuilder是非线程安全的，StringBuffer是线程安全的。StringBuffer内部的所有方法都是使用synchronized锁实现的同步方法，所以在多线程环境下使用StringBuffer。StringBuilder的方法没有使用任何同步机制，所以是非线程安全的。注意在单线程环境下StringBuilder效率比StringBuffer高，因为没有加锁释放锁的时间。
.2、Java基本类型
byte/8
char/16
short/16
int/32
float/32
long/64
double/64
boolean/~
boolean 只有两个值：true、false，可以使用 1 bit 来存储，但是具体大小没有明确规定。JVM 会在编译时期将 boolean 类型的数据转换为 int，使用 1 来表示 true，0 表示 false。JVM 并不直接支持 boolean 数组，而是使用 byte 数组来表示 int 数组
.3、Java类型的缓存池
new Integer(123) 与 Integer.valueOf(123) 的区别在于：
1、new Integer(123) 每次都会新建一个对象；
2、Integer.valueOf(123) 会使用缓存池中的对象，多次调用会取得同一个对象的引用。
valueOf() 方法的实现比较简单，就是先判断值是否在缓存池中，如果在的话就直接返回缓存池的内容。
在 Java 8 中，Integer 缓存池的大小默认为 -128~127。
编译器会在自动装箱过程调用 valueOf() 方法，因此多个 Integer 实例使用自动装箱来创建并且值相同，那么就会引用相同的对象。
基本类型对应的缓冲池如下：
boolean values true and false
all byte values
short values between -128 and 127
int values between -128 and 127
char in the range \u0000 to \u007F
在使用这些基本类型对应的包装类型时，就可以直接使用缓冲池中的对象。
.4、Java包装和基本类型的值比较
1、基本型和基本型封装型进行“==”运算符的比较，封装型将会自动拆箱变为基本型后再进行比较，因此Integer(0)会自动拆箱为int类型再进行比较；
2、两个Integer类型进行“==”比较，如果其值在-128至127，那么返回true，否则返回false, 这跟Integer.valueOf()的缓冲对象有关，这里不进行赘述。
3、两个基本型的封装型进行equals()比较，首先equals()会比较类型，如果类型相同，则继续比较值，如果值也相同，返回true
4、基本型封装类型调用equals(),但是参数是基本类型，这时候，先会进行自动装箱，基本型转换为其封装类型，再进行比较
.5、String的replaceAll方法
由于replaceAll方法的第一个参数是一个正则表达式，而"."在正则表达式中表示任何字符，所以会把 String classFile = "com.jd.". replaceAll(".", "/") + "MyClass.class";前面字符串的所有字符都替换成"/"。如果想替换的只是"."，那么久要写成"\\."
.6、String str="i"与 String str=new String("i")一样吗？
不一样，因为内存的分配方式不一样。String str="i"的方式，java 虚拟机会将其分配到常量池中；而 String str=new String("i") 则会被分到堆内存中。
.7、如何将字符串反转？
使用 StringBuilder 或者 stringBuffer 的 reverse() 方法。
.8、String 类的常用方法都有那些？
1.indexOf()：返回指定字符的索引。
2.charAt()：返回指定索引处的字符。
3.replace()：字符串替换。
4.trim()：去除字符串两端空白。
5.split()：分割字符串，返回一个分割后的字符串数组。
6.getBytes()：返回字符串的 byte 类型数组。
7.length()：返回字符串长度。
8.toLowerCase()：将字符串转成小写字母。
9.toUpperCase()：将字符串转成大写字符。
10.substring()：截取字符串。
11.equals()：字符串比较。
12.toCharArray()：返回字符串的char类型数组。
.9、Java表达式转型规则由低到高转换？
1、所有的byte,short,char型的值将被提升为int型；
2、如果有一个操作数是long型，计算结果是long型；
3、如果有一个操作数是float型，计算结果是float型；
4、如果有一个操作数是double型，计算结果是double型；
5、被fianl修饰的变量不会自动改变类型，当2个final修饰相操作时，结果会根据左边变量的类型而转化。

1.4.Java变量
.1、Java初始化顺序
普通类：
静态变量--静态代码块--普通变量--普通代码块--构造函数
继承的子类：
父类静态变量--父类静态代码块--子类静态变量--子类静态代码块--父类普通变量--父类普通代码块--父类构造函数--子类普通变量--子类普通代码块--子类构造函数
抽象的实现子类: 接口 - 抽线类 - 实现类
接口静态变量--抽象类静态变量--抽象类静态代码块--实现类静态变量--实习类静态代码块--抽象类普通变量--抽象类普通代码块--抽象类构造函数--实现类普通变量--实现类普通代码块--实现类构造函数
接口注意：
声明的变量都是静态变量并且是final的，所以子类无法修改，并且是固定值不会因为实例而变化
接口中能有静态方法，不能有普通方法，普通方法需要用defalut添加默认实现
接口中的变量必须实例化
接口中没有静态代码块、普通变量、普通代码块、构造函数
1.5.Java集合
.1、Java的Collection接口和Map接口

.2、HashMap是怎么实现的？
数据结构上是基于：数组+单链表；
无序，特别说明这个无序指的是遍历HashMap的时候，得到的元素的顺序基本不可能是put的顺序。
.3、HashMap和HashTable的区别？
1）继承的类不一样：
HashMap继承的是AbstractMap，Hashtable继承的是Dictionary。实现的接口一致(Map、Cloneable和Serializable)；
2）初始容量不一样：
HashMap默认容量是16，且容量只能是2 的幂次方，这与计算key的hashcode算法有关，计算key的存储位置时，用的是i=hashcode&(table.length-1)， 只有容量是2的幂次方时才与hashcode%( table.length-1)等价，此外HashMap是在第一次put键值对时才初始化。
HashTable默认容量是11，容量没有2的幂次方限制，每次扩容大小是oldCap*2+1;
3）HashMap 是非线程安全的，HashTable是线程安全的：
默认下，HashMap没有对方法进行同步，HashTable中方法均是使用synchronized进行了同步。
4）HashMap允许有一个key为null, 并且存储在table[0]位置，允许多个value为null；       
但是HashTable不允许value 为空。
5）hashMap去掉了HashTable 的contains方法，但是加上了containsValue（）和containsKey（）方法。
.4、Vector、ArrayList、LinkedList的区别？
1）Vector 和ArrayList最大的区别在于，Vector里面的核心方法都是synchronized方法，此外Vector每次扩容都是2倍扩容，而ArrayList是扩容50%。
2）ArrayList是基于数组实现的，里面的元素允许为空且允许重复，且基本有序(插入和遍历顺序一致)，但是是非线程安全的。还有一点需要注意的是ArrayList的subList()函数返回的并不是一个新的List对象，仅仅只是父类的一个视图，对subList的修改会影响到原本的父List。
3）LinkedList实现了Queue接口，所以可以作为一个FIFO的队列使用。LinkedList内部是基于双向链表实现的，元素可为空也可重复，并且遍历的时候是有序的。和ArrayList一样同样是非线程安全的。
4）LinkedList千万不能用for循环遍历，for循环遍历会比迭代器慢上n倍，因为LinkedList是基于双向链表实现的，for循环遍历，每次遍历数据都会把前面的数据走一遍，所以是非常耗时的。
.5、HashMap 和 ConcurrentHashMap的区别？
1）线程安全的Map，
2）基于分段锁实现，默认是16级分段，这里面的每个Segment都相当于一个HashTable
3）每个Segment只允许一个线程写，但是不限制读。
1）ConcurrentHashMap是基于分段锁实现的，具体可以理解成把一个大的Map拆分成N个小的HashTable（默认是16个），根据key.hashCode()来决定把key放到哪个HashTable。在ConcurrentHashMap中就是把Map分成了N个Segment，put和get的时候，都是先根据key.hashCode()算出放在哪个Segment中，然后对对应的Segment加锁，这样就不会影响其余Segment的并发访问。这样效率就提升了N倍，默认提升了16倍。其实也就是同时允许16个线程分别对16个Segment操作，只有写操作才需要锁住Segment，读线程基本不受限制。 
2）基本上ConcurrentHashMap是HashMap 和 HashTable的结合。那么为什么ConcurrentHashMap里面的get()操作，也就是读操作不用加锁呢，除非读到的值是空的才会加锁重读？
原因是它的get方法里将要使用的共享变量都定义成volatile，如用于统计当前Segement大小的count字段和用于存储值的HashEntry的value。定义成volatile的变量，能够在线程之间保持可见性，能够被多线程同时读，并且保证不会读到过期的值，但是只能被单线程写（有一种情况可以被多线程写，就是写入的值不依赖于原值），在get操作里只需要读不需要写共享变量count和value，所以可以不用加锁。之所以不会读到过期的值，是根据java内存模型的happen before原则，对volatile字段的写入操作优先于读操作，即使两个线程同时修改和获取volatile变量，get操作也能拿到最新的值，这是用volatile替换锁的经典应用场景。
3）ConcurrentHashMap不允许key或则value为空。
.6、Collection和Collections有什么区别？
java.util.Collection 是一个集合接口（集合类的一个顶级接口）。它提供了对集合对象进行基本操作的通用接口方法。Collection接口在Java 类库中有很多具体的实现。Collection接口的意义是为各种具体的集合提供了最大化的统一操作方式，其直接继承接口有List与Set。
Collections则是集合类的一个工具类/帮助类，其中提供了一系列静态方法，用于对集合中元素进行排序、搜索以及线程安全等各种操作。
.7、List、Set、Map 之间的区别是什么？
.8、如何决定使用 HashMap 还是 TreeMap？
对于在Map中插入、删除和定位元素这类操作，HashMap是最好的选择。然而，假如你需要对一个有序的key集合进行遍历，TreeMap是更好的选择。基于你的collection的大小，也许向HashMap中添加元素会更快，将map换为TreeMap进行有序key的遍历。
.9、说一下 HashMap 的实现原理？
1.HashMap概述： HashMap是基于哈希表的Map接口的非同步实现。此实现提供所有可选的映射操作，并允许使用null值和null键。此类不保证映射的顺序，特别是它不保证该顺序恒久不变。 
2.HashMap的数据结构： 在java编程语言中，最基本的结构就是两种，一个是数组，另外一个是模拟指针（引用），所有的数据结构都可以用这两个基本结构来构造的，HashMap也不例外。HashMap实际上是一个“链表散列”的数据结构，即数组和链表的结合体。
3.当我们往Hashmap中put元素时,首先根据key的hashcode重新计算hash值,根据hash值得到这个元素在数组中的位置(下标),如果该数组在该位置上已经存放了其他元素,那么在这个位置上的元素将以链表的形式存放,新加入的放在链头,最先加入的放入链尾.如果数组中该位置没有元素,就直接将该元素放到数组的该位置上。
4.需要注意Jdk 1.8中对HashMap的实现做了优化,当链表中的节点数据超过八个之后,该链表会转为红黑树来提高查询效率,从原来的O(n)到O(logn)。
.10、说一下HashSet的实现原理？
1.HashSet底层由HashMap实现。
2.HashSet的值存放于HashMap的key上。
3.HashMap的value统一为PRESENT。
.11、如何实现数组和 List 之间的转换？
List转换成为数组：调用ArrayList的toArray方法。
数组转换成为List：调用Arrays的asList方法。
.12、ArrayList 和 Vector 的区别是什么？
Vector是同步的，而ArrayList不是。然而，如果你寻求在迭代的时候对列表进行改变，你应该使用CopyOnWriteArrayList。 
ArrayList比Vector快，它因为有同步，不会过载。 
ArrayList更加通用，因为我们可以使用Collections工具类轻易地获取同步列表和只读列表。
.13、Array 和 ArrayList 有何区别？
Array可以容纳基本类型和对象，而ArrayList只能容纳对象。 
Array是指定大小的，而ArrayList大小是固定的。 
Array没有提供ArrayList那么多功能，比如addAll、removeAll和iterator等。
.14、在 Queue 中 poll()和 remove()有什么区别？
poll() 和 remove() 都是从队列中取出一个元素，但是 poll() 在获取元素失败的时候会返回空，但是 remove() 失败的时候会抛出异常。
.15、哪些集合类是线程安全的？
vector：就比arraylist多了个同步化机制（线程安全），因为效率较低，现在已经不太建议使用。在web应用中，特别是前台页面，往往效率（页面响应速度）是优先考虑的。
statck：堆栈类，先进后出。
hashtable：就比hashmap多了个线程安全。
enumeration：枚举，相当于迭代器。
.16、迭代器 Iterator 是什么？
迭代器是一种设计模式，它是一个对象，它可以遍历并选择序列中的对象，而开发人员不需要了解该序列的底层结构。迭代器通常被称为“轻量级”对象，因为创建它的代价小。
.17、Iterator 怎么使用？有什么特点？
Java中的Iterator功能比较简单，并且只能单向移动：
(1) 使用方法iterator()要求容器返回一个Iterator。第一次调用Iterator的next()方法时，它返回序列的第一个元素。注意：iterator()方法是java.lang.Iterable接口,被Collection继承。
(2) 使用next()获得序列中的下一个元素。
(3) 使用hasNext()检查序列中是否还有元素。
(4) 使用remove()将迭代器新返回的元素删除。
Iterator是Java迭代器最简单的实现，为List设计的ListIterator具有更多的功能，它可以从两个方向遍历List，也可以从List中插入和删除元素。
.18、Iterator 和 ListIterator 有什么区别？
Iterator可用来遍历Set和List集合，但是ListIterator只能用来遍历List。 
Iterator对集合只能是前向遍历，ListIterator既可以前向也可以后向。 
ListIterator实现了Iterator接口，并包含其他的功能，比如：增加元素，替换元素，获取前一个和后一个元素的索引，等等。
1.6.Java中的异常处理
.1、error和exception有什么区别？

①.首先Exception和Error都是继承于Throwable 类，在 Java 中只有 Throwable 类型的实例才可以被抛出（throw）或者捕获（catch），它是异常处理机制的基本组成类型。
②.Exception和Error体现了JAVA这门语言对于异常处理的两种方式。
③.Exception是java程序运行中可预料的异常情况，咱们可以获取到这种异常，并且对这种异常进行业务外的处理。
④.Error是java程序运行中不可预料的异常情况，这种异常发生以后，会直接导致JVM不可处理或者不可恢复的情况。所以这种异常不可能抓取到，比如
⑤.OutOfMemoryError、NoClassDefFoundError等。
其中的Exception又分为检查性异常和非检查性异常。两个根本的区别在于，检查性异常 必须在编写代码时，使用try catch捕获（比如：IOException异常）。⑥.非检查性异常在代码编写使用，可以忽略捕获操作（比如：ArrayIndexOutOfBoundsException），这种异常是在代码编写或者使用过程中通过规范可以避免发生的。 
⑦.Exception（异常）:是程序本身可以处理的异常。 
⑧.Error（错误）: 是程序无法处理的错误。这些错误表示故障发生于虚拟机自身、或者发生在虚拟机试图执行应用时，一般不需要程序处理。
⑨.检查异常（编译器要求必须处置的异常）：除了Error，RuntimeException及其子类以外，其他的Exception类及其子类都属于可查异常。这种异常的特点是Java编译器会检查它，也就是说，当程序中可能出现这类异常，要么用try-catch语句捕获它，要么用throws子句声明抛出它，否则编译不会通过。
⑩.非检查异常(编译器不要求处置的异常): 包括运行时异常（RuntimeException与其子类）和错误（Error）。
.2、常见的异常类有哪些？
1.NullPointerException：当应用程序试图访问空对象时，则抛出该异常。
2.SQLException：提供关于数据库访问错误或其他错误信息的异常。
3.IndexOutOfBoundsException：指示某排序索引（例如对数组、字符串或向量的排序）超出范围时抛出。 
4.NumberFormatException：当应用程序试图将字符串转换成一种数值类型，但该字符串不能转换为适当格式时，抛出该异常。
5.FileNotFoundException：当试图打开指定路径名表示的文件失败时，抛出此异常。
6.IOException：当发生某种I/O异常时，抛出此异常。此类是失败或中断的I/O操作生成的异常的通用类。
7.ClassCastException：当试图将对象强制转换为不是实例的子类时，抛出该异常。
8.ArrayStoreException：试图将错误类型的对象存储到一个对象数组时抛出的异常。
9.IllegalArgumentException：抛出的异常表明向方法传递了一个不合法或不正确的参数。
10.ArithmeticException：当出现异常的运算条件时，抛出此异常。例如，一个整数“除以零”时，抛出此类的一个实例。 
11.NegativeArraySizeException：如果应用程序试图创建大小为负的数组，则抛出该异常。
12.NoSuchMethodException：无法找到某一特定方法时，抛出该异常。
13.SecurityException：由安全管理器抛出的异常，指示存在安全侵犯。
14.UnsupportedOperationException：当不支持请求的操作时，抛出该异常。
15.RuntimeExceptionRuntimeException：是那些可能在Java虚拟机正常运行期间抛出的异常的超类。
.3、throw 和 throws 的区别？
throws是用来声明一个方法可能抛出的所有异常信息，throws是将异常声明但是不处理，而是将异常往上传，谁调用我就交给谁处理。而throw则是指抛出的一个具体的异常类型。
Java通过面向对象的方法进行异常处理，把各种不同的异常进行分类，并提供了良好的接口。
在Java中，每个异常都是一个对象，它是Throwable类或其它子类的实例。
当一个方法出现异常后便抛出一个异常对象，该对象中包含有异常信息，调用这个对象的方法可以捕获到这个异常并进行处理。
Java的异常处理是通过5个关键词来实现的：try、catch、throw、throws和 finally。
一般情况下是用try来执行一段程序，如果出现异常，系统会抛出（throws）一个异常，这时候你可以通过它的类型来捕捉（catch）它，或最后（finally）由缺省处理器来处理。
用try来指定一块预防所有"异常"的程序。紧跟在try程序后面，应包含一个catch子句来指定你想要捕捉的"异常"的类型。 Throw语句用来明确地抛出一个"异常"。
Throws用来标明一个成员函数可能抛出的各种"异常"。 Finally为确保一段代码不管发生什么"异常"都被执行一段代码。 可以在一个成员函数调用的外面写一个try语句，在这个成员函数内部写另一个try语句保护其他代码。每当遇到一个try语句，"异常"的框架就放到堆栈上面，直到所有的try语句都完成。如果下一级的try语句没有对某种"异常"进行处理，堆栈就会展开，直到遇到有处理这种"异常"的try语句。
.4、try-catch-finally 中哪个部分可以省略？
答：catch 可以省略
原因：
更为严格的说法其实是：try只适合处理运行时异常，try+catch适合处理运行时异常+普通异常。也就是说，如果你只用try去处理普通异常却不加以catch处理，编译是通不过的，因为编译器硬性规定，普通异常如果选择捕获，则必须用catch显示声明以便进一步处理。而运行时异常在编译时没有如此规定，所以catch可以省略，你加上catch编译器也觉得无可厚非。
理论上，编译器看任何代码都不顺眼，都觉得可能有潜在的问题，所以你即使对所有代码加上try，代码在运行期时也只不过是在正常运行的基础上加一层皮。但是你一旦对一段代码加上try，就等于显示地承诺编译器，对这段代码可能抛出的异常进行捕获而非向上抛出处理。如果是普通异常，编译器要求必须用catch捕获以便进一步处理；如果运行时异常，捕获然后丢弃并且+finally扫尾处理，或者加上catch捕获以便进一步处理。
至于加上finally，则是在不管有没捕获异常，都要进行的“扫尾”处理。
throws声明抛出的异常，throw抛出异常对象，try语句块里面可以嵌套try{}catch{}，所以try块中也可以抛出异常
.5、try-catch-finally 中，如果 catch 中 return 了，finally 还会执行吗？
答：会执行，在 return 前执行。
1.7.Java8新特性


1.8.其他
.1、Swing
Swing是一个用于开发Java应用程序用户界面的开发工具包。它以抽象窗口工具包（AWT）为基础使跨平台应用程序可以使用任何可插拔的外观风格。Swing开发人员只用很少的代码就可以利用Swing丰富、灵活的功能和模块化组件来创建优雅的用户界面。 
  工具包中所有的包都是以swing作为名称，例如javax.swing,javax.swing.event
  用Swing创建图形界面步骤：
  （1）导入Swing包
  （2）选择界面风格
  （3）设置顶层容器
  （4）设置按钮和标签
  （5）将组件放到容器上
  （6）为组件增加边框
  （7）处理事件
  （8）辅助技术支持
1.导入Swing包
下面语句导入Swing包
  import javax.swing.*;
大部分Swing程序用到了AWT的基础底层结构和事件模型,因此需要导入两个包：
  import java.awt.*;
  import java.awt.event.*;
如果图形界面中包括了事件处理，那么还需要导入事件处理包：
  import javax.swing.event.*;
2.选择界面风格
  Swing允许选择程序的图形界面风格常用的有java风格，windows风格等
  下面的代码用于选择图形界面风格，这里选择的是跨平台的Java界面风格。
  try { UIManager.setLookAndFeel( 
  UIManager.getCrossPlatformLookAndFeelClassName( )); } 
  catch (Exception e) { }
3.设置顶层容器
  图形界面至少要有一个顶级Swing容器
  顶级Swing容器为其它Swing组件在屏幕上的绘制和处理事件提供支持
  常用的顶级容器：
  JFrame（框架）：表示主程序窗口
  JDialog（对话框）：每个JDialog对象表示一个对话框，对话框属于二级窗口
  JApplet（小程序）：在浏览器内显示一个小程序界面
  一个框架包括边界、菜单栏、工具栏、状态栏，以及中间占主要部分的窗格
  窗格也可以看作是一种面板，但它是框架的一个组成部分
  组件不会直接放到框架上，而是放在若干个面板上，这些面板再放到窗格上
用框架对象的getContentPane()函数来获得窗格，再调用窗格的add()函数放置面板
public static void main(String[ ]args){JFrame frame=new JFrame("SwingApplication");
  JPanel panel1=new JPanel();
  frame.getContentPane().add(panel1,BorderLayout.CENTER);
  ......//添加其他组件
  frame.pack();frame.setVisible(true);}
swing是单线程的，当swing界面程序启动的时候，会启动3个进程，
1、主线程
2、系统工具包线程:负责捕获操作系统事件，然后将事件转换成swing的事件，然后发送到事件派发线程EDT
3、事件派发线程(EDT):将事件派发到各个组件，并负责调用绘制方法更新界面
.2、AWT和Swing之间的区别
1)AWT 是基于本地方法的C/C++程序，其运行速度比较快；Swing是基于AWT的Java程序，其运行速度比较慢。
Swing 是在AWT的基础上构建的一套新的图形界面系统，它提供了AWT 所能够提供的所有功能，并且用纯粹的Java代码对AWT 的功能进行了大幅度的扩充。
2)AWT的控件在不同的平台可能表现不同，而Swing在所有平台表现一致。
在实际应用中，应该使用AWT还是Swing取决于应用程序所部署的平台类型。例如：
1)对于一个嵌入式应用，目标平台的硬件资源往往非常有限，而应用程序的运行速度又是项目中至关重要的因素。在这种矛盾的情况下，简单而高效的AWT当然成了嵌入式Java的第一选择。
2)在普通的基于PC或者是工作站的标准Java应用中，硬件资源对应用程序所造成的限制往往不是项目中的关键因素。所以在标准版的Java中则提倡使用Swing， 也就是通过牺牲速度来实现应用程序的功能。
AWT和Swing都是java中的包。
AWT(Abstract Window Toolkit)：抽象窗口工具包，早期编写图形界面应用程序的包。
Swing ：为解决 AWT 存在的问题而新开发的图形界面包。Swing是对AWT的改良和扩展。    
AWT和Swing的实现原理不同：
AWT的图形函数与操作系统提供的图形函数有着一一对应的关系。也就是说，当我们利用 AWT构件图形用户界面的时候，实际上是在利用操作系统的图形库。
不同的操作系统其图形库的功能可能不一样，在一个平台上存在的功能在另外一个平台上则可能不存在。为了实现Java语言所宣称的"一次编译，到处运行"的概念，AWT不得不通过牺牲功能来实现平台无关性。因此，AWT 的图形功能是各操作系统图形功能的“交集”。
因为AWT是依靠本地方法来实现功能的，所以AWT控件称为“重量级控件”。 
而Swing ，不仅提供了AWT 的所有功能，还用纯粹的Java代码对AWT的功能进行了大幅度的扩充。
例如：并不是所有的操作系统都提供了对树形控件的支持， Swing则利用了AWT中所提供的基本作图方法模拟了一个树形控件。
由于 Swing是用纯粹的Java代码来实现的，因此Swing控件在各平台通用。
因为Swing不使用本地方法，故Swing控件称为“轻量级控件”。 
3、 事务属性
事务属性的种类：传播行为、隔离级别、只读和事务超时
.a)传播行为定义了被调用方法的事务边界。
传播行为	意义
PROPERGATION_MANDATORY
(propergation_mandatory)	表示方法必须运行在一个事务中，如果当前事务不存在，就抛出异常
PROPAGATION_NESTED
(propagation_nested)	表示如果当前事务存在，则方法应该运行在一个嵌套事务中。否则，它看起来和PROPAGATION_REQUIRED 看起来没什么俩样
PROPAGATION_NEVER
(propagation_never)	表示方法不能运行在一个事务中，否则抛出异常
PROPAGATION_NOT_SUPPORTED
(propagation_not_supported)	表示方法不能运行在一个事务中，如果当前存在一个事务，则该方法将被挂起
PROPAGATION_REQUIRED
(propagation_required)	表示当前方法必须运行在一个事务中，如果当前存在一个事务，那么该方法运行在这个事务中，否则，将创建一个新的事务
PROPAGATION_REQUIRES_NEW
(propagation_requires_new)	表示当前方法必须运行在自己的事务中，如果当前存在一个事务，那么这个事务将在该方法运行期间被挂起
PROPAGATION_SUPPORTS
(propagation_supports)	表示当前方法不需要运行在一个是事务中，但如果有一个事务已经存在，该方法也可以运行在这个事务中
.b)隔离级别
在操作数据时可能带来 3 个副作用，分别是脏读、不可重复读、幻读。为了避免这 3 中副作用的发生，在标准的 SQL 语句中定义了 4 种隔离级别，分别是未提交读、已提交读、可重复读、可序列化。而在 spring 事务中提供了 5 种隔离级别来对应在 SQL 中定义的 4 种隔离级别，如下：
隔离级别	意义
ISOLATION_DEFAULT
(isolation_default)	使用后端数据库默认的隔离级别
ISOLATION_READ_UNCOMMITTED
(isolation_read_uncommitted)	允许读取未提交的数据（对应未提交读），可能导致脏读、不可重复读、幻读
ISOLATION_READ_COMMITTED
(isolation_read_cimmitted)	允许在一个事务中读取另一个已经提交的事务中的数据（对应已提交读）。可以避免脏读，但是无法避免不可重复读和幻读
ISOLATION_REPEATABLE_READ
(isolation_repreatable_read)	一个事务不可能更新由另一个事务修改但尚未提交（回滚）的数据（对应可重复读）。可以避免脏读和不可重复读，但无法避免幻读
ISOLATION_SERIALIZABLE
(isolation_serializable)	这种隔离级别是所有的事务都在一个执行队列中，依次顺序执行，而不是并行（对应可序列化）。可以避免脏读、不可重复读、幻读。但是这种隔离级别效率很低，因此，除非必须，否则不建议使用。
.c)只读
如果在一个事务中所有关于数据库的操作都是只读的，也就是说，这些操作只读取数据库中的数据，而并不更新数据，那么应将事务设为只读模式（ READ_ONLY_MARKER ） , 这样更有利于数据库进行优化 。
因为只读的优化措施是事务启动后由数据库实施的，因此，只有将那些具有可能启动新事务的传播行为 (PROPAGATION_NESTED 、 PROPAGATION_REQUIRED 、 PROPAGATION_REQUIRED_NEW) 的方法的事务标记成只读才有意义。
如果使用 Hibernate 作为持久化机制，那么将事务标记为只读后，会将 Hibernate 的 flush 模式设置为 FULSH_NEVER, 以告诉 Hibernate 避免和数据库之间进行不必要的同步，并将所有更新延迟到事务结束。
.d)事务超时
如果一个事务长时间运行，这时为了尽量避免浪费系统资源，应为这个事务设置一个有效时间，使其等待数秒后自动回滚。与设
置“只读”属性一样，事务有效属性也需要给那些具有可能启动新事物的传播行为的方法的事务标记成只读才有意义。
.4、加载驱动方法
1.Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");
2. DriverManager.registerDriver(new com.mysql.jdbc.Driver());
3.System.setProperty("jdbc.drivers", "com.mysql.jdbc.Driver");
.5、编译和解释
目标程序是编译系统生成的，解释系统不生成目标程序。
编译： 源代码->目标代码
解释：源代码->中间代码->目标代码
目标代码是机器可直接执行的代码
不管编译还是解释,都需要转为机器识别的才能执行, 只不过解释是靠虚拟机或者其他机制
脚本的特点是，脚本本身不编译为机器码。而是依托于寄主（虚拟机，脚本解释器等）。
其实真正起执行作用的是寄主。脚本命令寄主按照脚本的需求来执行操作。
而常规的编译型的代码，通过编译器编译成独立的可执行文件。可执行文件本身就包含了执行语句。它自己来执行自己所需的操作。
你可以简单这么理解：常规编译型的代码，是奔跑的人。而脚本是骑马的人，脚本解释器就是他的坐骑。真正跑起来的是马而不是人。
一般脚本执行效率会低一些，但开发起来容易一些。（只是一般情况）

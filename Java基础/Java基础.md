# 九种基本数据类型的大小，以及他们的封装类。
基本数据类型及其封装类

| 基本类型 | 大小(字节) | 默认值 | 封装类    |
| -------- | ---------- | ------ | --------- |
| byte     | 1          | 0      | Byte      |
| short    | 2          | 0      | Short     |
| int      | 4          | 0      | Integer   |
| long     | 8          | 0L     | Long      |
| float    | 4          | 0.0f   | Float     |
| double   | 8          | 0.0d   | Double    |
| boolean  | 1          | false  | Boolean   |
| char     | 2          | \u0000 | Character |
| void     | -          | -      | Void      |

值得注意的是是有 void 和其封装类 java.lang.Void 的

# switch 能否用 String 做参数？
从Java 1.7开始的版本可以使用 String 作为 switch 的参数, 而在其之前只能使用 int 和 char 作为参数.

而在Java 5以前, 只能使用byte, short, char, int类型. 在Java 5 中引入了 Enum 类型.

# equals与==的区别

`==` 表示比较左右两个值是否相等. 也就是说对于基础类型来说, 由于基础类型的引用是直接保存的值, 也就直接进行比较. 对于引用类型来说, 是比较两个引用是否指向同一个对象, 也就是说两个'指针'是否相等.

而`equals()`方法是从`Object`类产生的, 默认的实现是比较两个对象的地址, 也就是跟`==`相同, 但是很多类会重写`equals`方法. 会使其语意转换为比较引用指向对象值的相等.

这里要注意Integer对于-128到127之间的值有一个缓存, 这个之后再说.

# Object有哪些公用方法

https://www.cnblogs.com/zhousysu/p/5483795.html

# Hashcode的作用

`Java中的hashCode方法就是根据一定的规则将与对象相关的信息(比如对象的存储地址，对象的字段等)映射成一个数值, 这个数值称作为散列值.`

https://www.cnblogs.com/dolphin0520/p/3681042.html

# 面向对象和面向过程的区别

## 面向对象
易维护、易复用、易扩展，由于面向对象有封装、继承、多态性的特性，可以设计出低耦合的系统，使系统更加灵活、更加易于维护
## 面向过程
性能比面向对象高，因为类调用时需要实例化，开销比较大，比较消耗资源;比如单片机、嵌入式开发、Linux/Unix等一般采用面向过程开发，性能是最重要的因素。

# JDK JRE JVM
JDK : Java Develop Kit   给开发者提供的工具箱, 包括JRE和其他的类库.
JRE : Java 运行时环境. 有JRE就可以运行.
JVM : 当我们运行一个程序时, JVM 负责将字节码转换为特定机器代码, JVM 提供了内存管理/垃圾回收和安全机制等. 这种独立于硬件和操作系统, 正是 java 程序可以一次编写多处执行的原因.

区别与联系:
- JDK 用于开发, JRE 用于运行java程序
- JDK 和 JRE 中都包含 JVM
- JVM 是 java 编程语言的核心并且具有平台独立性

# TODO
- Java的四种引用，强弱软虚，用到的场景。

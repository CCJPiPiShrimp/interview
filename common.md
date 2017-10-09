1. Android 消息机制  Handler、Message、MessageQueue、Loop
2. Activity 和Fragment的生命周期   activity的启动模式 
3. Arraylist的内部实现、增长触发时机、怎么增长的
4. 业务需求，优化点   内存泄露、组件拆分、模块化集成
5. 服务端和客户端交互怎么保证接口的安全,不被刷接口   https和参数携带签名
6. Get 和Post的区别   能否传多媒体数据
7. Http请求状态码  1xx—5xx
8. 链表删除操作  int head



3(A).  add()时判断容量大小，在java 6中是 采用 ( ementSize * 3) / 2 + 1 ，而java 7中采用的位运算进行扩容int newCapacity = oldCapacity + (oldCapacity >> 1)，扩容的大小是1.5倍。并且有最大大小限制。


1. bindService() 后能startServiece()吗？    可以， startService走的是 没有通道的
2. intentService   是一个工作完成了，自动调用stopSelf()
3. Apt 编译时注解， 自动生成代码
4. retrofit 动态代理，invoke

1. activity 显示dialog时生命周期是什么样子的？  onPause() 会不会调用     不会
2. activity启动模式， context.startActiviy() 为什么需要设置 NEW_TASK 、 解析下返回栈和任务栈
3.  Asynctask 的缺点，  没有采用线程池，最大并发量有限制
4. 事件分发机制，dispatchTouchEvent() 返回 true 或false 事件还继续往下传么？ 
5. JVM 内存模型和回收算法，怎么使应用程序stackoverflowerror，怎么避免        
6. 进程和线程的区别，多线程的实现方式、进程、线程间通信、同步，线程的几种状态，怎么停止一个线程，在各个状态下？   Cpu调用算法有哪几种？
7. 一个Servie中执行下载任务，怎么在activity中得到下载进度，bindService 调用download方法中添加callback监听、广播
8.  HashMap 的数据结构、hash冲突,    得到index的方法和Java 6中有什么改进，HashMap和SparseArray的区别，为什么android推荐使用？ 
9. 单例模式、抽象工厂、责任链模式、门面模式，怎么理解设计模式的6个基本准则，java中允许多继承么？
10. 单例模式中还问到了  一个类中  构造方法、成员变量、静态代码块、静态变量、静态内部类的执行顺序。
11. 有哪些操作会导致内存泄露，怎么避免  ->  弱引用、正确使用ApplicationContext、bitmap、cursor等。
12. 怎么合理设计网络请求Api 和保证传输安全，作为客户端怎么优化接口
13. OKHttp中是怎么使用线程池或连接池的，自己实现一个线程池该如何考虑？ 伪代码(就是讲下思路)
14. 如何设计一个图片加载框架，内存和磁盘缓存、LRU算法伪代码实现
15. MVP架构优缺点，怎么处理Presenter层的生命周期问题
16. AMS和WS 以及一些系统的Service 有了解过么？   平时怎么阅读源码的。
17. Git版本控制比SVN好在哪里，git fetch 和 git pull的区别

算法，操作系统，网络，Android，Java挨个问了个遍。


  ● 算法： 常用排序算法，复杂度，比较器用的哪种？快排怎么写？完全二叉树高度为n结点最多有多少，汉诺塔问题怎么解决，链表和数组比较？
  ● 操作系统： 进程冲突，生产者消费者问题，设逻辑分页和物理分页好处是什么，什么是脏内存。
  ● 网络：http1.1相比以前版本有什么改变，七层/五层模型，tcpip分别对应哪层。https的对称加密。
  ● java: public等四个权限关键字的区别，synchronized的用法区别，可否嵌套。 hashmap底层实现，扩容策略，初始化。 arraylist和linkedlist的实现和区别。 classloader的作用，双亲委托。 gc算法(优缺点)，为什么叫新生代老年代(晋升机制)，强软弱虚四种引用的区别。
  ● android: activity退出怎么保存数据。 怎么把数据写入文件。 picasso的缓存策略，lrucache底层实现，linkedhashmap底层实现，缓存文件怎么命名。 RxJava优缺点，实习项目相关。 自定义view有几个构造方法，第三个参数作用。 listview的convert view作用，用viewholder为什么可以优化他。

（3）百度

百度一面问了很多性能优化的问题，还有app被杀死怎么启动，耗电太多怎么破，怎么统计crash，怎么减少用户流量消耗，事件分发机制，ontouchlistener返回false才会调用onclicklistener，消息机制，view的绘制原理，方法数超过65535怎么办，binder，anr，listview优化，bitmap怎么避免oom。 Java静态内部类和内部类的区别，垃圾回收机制，元空间有哪些东西，hashmap和hashtable区别，list和set区别。

（4）今日头条

头条暑期一面： 二维数组二分查找的最优算法，数组元素从左到右从上到下递增。 retrofit原理，recyclerview和listview异同，各自缓存原理，handler原理，activity生命周期，四种启动模式区别，singletask启动standard的activity在哪个栈，android多进程和多线程的实现，进程和线程区别。

java泛型类型擦除发生在什么时候，通配符有什么需要注意的。

hashmap删除键值对的过程，扩容算法，hashcode和equals有什么关系。java保证线程安全有哪些方法，volatile和synchronized各有何作用。 浏览器打开一个网页的过程发生了什么。 擅长android哪些方面？

（5）腾讯

  ● 内推一面： final作用。 下拉刷新加载更多的原理。 RxJava优点，map，flatmap的原理。 可不可以多次subscribeOn，ObserveOn，会有什么后果。 lambda表达式？和匿名内部类的不同。 http协议和https，ssl和tls握手。
  ● 内推一面： 自我介绍，项目经历。 java finalize关键字的用法。 try 里面return了finally还会执行吗？执行顺序是？ wait和sleep的区别，应用场景。 gc发生在什么时候。 死锁发生的条件。 tcp三次握手的过程？如果确认信号没传到服务器会发生什么？为什么不是两次握手？ 一个无序数组怎么找出两个和为特定值的数？快排后首尾两游标。 12个鸡蛋有一个质量不同，如何只称三次测出。 开发过程中有没有实际遇到内存泄露情况，怎么解决的。 activity四种启动模式区别和应用场景。 service生命周期，两种启动方式的区别。 实现ipc的方法有哪些？ handler的内在原理。消息队列为空会怎样？ 换主题功能怎么实现 如果有机会来腾讯实习，你比较感兴趣的技术有哪些？
  ● 网申一面：当时面完没记录，主要是针对简历提问，大致问了，动画，handler的原理，GC,双亲委托模型，容器类源码，四大组件，红黑树，activity四种启动模式及其用途，Java实现线程安全有哪些方式，TCP三次握手四次挥手，线程进程区别，Android多进程相关，socket相关，怎么设计一个检测内存泄漏的第三方框架，为什么用Picasso不用更好的库，RxJava相关。手写一个线程安全的单例模式。
  ● 网申二面：技术总监面，学到了很多。基础真的很重要。基础不好就会更早迎来瓶颈。大致问了项目，NP问题，断点调试功能怎么设计，也聊到一点在实验室做过的APK逆向工程，写编译器，APP启动过程以及其中的堆栈分配，以及技术成长道路什么的。这是印象最深的一次我感觉面完非常畅快并且受益匪浅，正了我在技术方面的误区，非常感谢面试官。
  ● HR面：HR面就轻松一点了，问面了哪些公司，为什么没过。家庭情况，爱好，项目经历和自己负责的部分，成绩，对部门了解多少，看过哪些专业书籍，想去哪里发展，经常回家吗，和聊天差不多。面完第二天显示已完成所有面试。
总结就是简历很重要，一份好的简历可以大大提升拿offer的概率，简历上实习经历和项目经历是亮点。

面试之前准备工作也很重要（尤其简历上的东西要非常熟悉，面经也可以刷一刷）。

基础知识也很重要，切不可只会写Android APP而忽视了算法，网络等基础。个人认为，对校招来说，想进大公司光能够写出漂亮的APP是不够的。正如二面面试官所说那样，非科班的也能做。

基础和深度是很重要的，比如Android可以多看看源码或者原理，而Java，算法，网络，操作系统，编译原理这些都应该熟练掌握。下面推荐一些我大一到大三看过的技术书籍。
1.hashmap原理及实现的数据结构，扩容策略，初始化

1.hashmap和hashtable区别，SparseArray和HashMap区别，为什么android推荐使用SparseArray？

2.线程锁有哪些，原理是什么？

3.java中允许多继承么？

4.线程池知识

5.wait()和sleep()的区别

7.JVM 内存模型和回收算法，如何造成StackOverflow

8.跨线程安全单例模式

9.面向对象的理解

10.public等四个权限关键字的区别

11.synchronized和volatile用法=

12.arraylist和linkedlist的实现和区别

13.强软弱虚四种引用的区别

14.双亲委派模型

15.Java静态内部类和内部类的区别

17.list和set区别

18.android多进程和多线程的实现，进程和线程区别

19.hashcode、equals、==有什么关系

20.java保证线程安全有哪些方法

21. final作用

22.finalize关键字的用法

23.try 里面return了finally还会执行吗？执行顺序是？ 

24.wait和sleep的区别

25.死锁发生的条件

26.Arraylist的内部实现、增长触发时机、怎么增长的

27.Android的集合类

collection类包括（list;set;queue）
list(arraylist;linkedlist;vector~stack)
queue(deque双端队列)
set(hashset;treeset)

28.如何停止一个线程，进程、线程间通信、同步，线程的几种状态

29. 单例模式中还问到了  一个类中  构造方法、成员变量、静态代码块、静态变量、静态内部类的执行顺序。
30. View的渲染机制
31. 动画的原理，底层如何给上层信号
32. 编译打包的过程
33. Android有多个资源文件夹，应用在不同分辨率下是如何查找对应文件夹下的资源的，描述整个过程
34. ANR的原理（回答主线程5秒阻塞是不行的，要读源码）
##BrainStorm---最近总结

一、 java1.5之后，sychorized锁和reentrantLock锁性能相当，但是reentrantLock锁粒度更小，可以更灵活的控制锁的释放和中断，不过使用reentrantLock需要开发人员有较高的素质，滥用会导致程序有严重的问题；  

二、 java异常类顶级接口：throwable-下面两个实现分别为Error和Exception，Error为jvm错误，分别为StackOutOfMemoryError和HeapOutOfMemoryError。Exception分为运行时异常和非运行时异常。
  
三、jvm虚拟机分为五个区，主要可分为线程私有和线程共享两个部分；
线程私有：程序计数器，虚拟机栈（调用方法地址，参数，返回类型），本地方法栈；线程共享：java堆（java对象存放），方法区（方法代码，常量池，静态变量，类信息）。且程序计数器不会有内存溢出的可能。 
 
四、java性能调优，使用jvisualVM查看内存，线程等情况，查看大内存，死锁发生地方，再检查程序代码逻辑。  

五、实现线程的几种方式，继承Thread，实现Runnable接口，实现Callable接口（可以有返回值），线程池调用，匿名内部类。  

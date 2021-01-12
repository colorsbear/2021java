## java 虚拟机

###线程运行诊断  
**案例1：cpu占用过多**

linux解决方式：  
1. 使用命令：top,查看cup占用情况，获取cpu进程  
2. ps H -eo pid,tid,%cpu(查看进程，线程，cpu占用情况，如果需要筛选， | grep 进程id)  
3. jstack 进程id （输出的线程编号是16进制的）
4. 可以根据线程id，找到有问题的代码行数


**案例2：运行程序不返回结果**

jstack 进程id

**工具使用jconsole** 
idea控制台输入jmap 进程id，可以查看java堆内存使用情况  
idea控制台直接输入jconsole，弹出图形化界面，连接线程后，可以查看线程运行情况。  

**案例3：垃圾回收后，内存占用依然很高**  
jvisualVM查看占用内存的对象


##java多线程
###java创建多线程的方式： 
 
###1.集成Thread类： 没有返回值
 
```java
public class T_Thread extends Thread{  
	@overide  
	public void run(){
		System.out.print(“继承Thrad实现多线程”);
	}
}
```

###2.实现Ruanable接口：没有返回值

```java
public class T_Runnable implements Runnable{
	@Overide
	public void run(){
	System.out.print(“实现Runnable接口");
	}
}
```

###3.匿名内部类  
"方式1：相当于继承了Thread类，作为子类重写run()实现"
//方式2:实现Runnable,Runnable作为匿名内部类
```java
public class DemoClass{
	public static void main(String [] args){
	
	 new Thead(){
	 	publid void run(){
	 		System.out.print("匿名内部类实现-1");
	 	};
	 }.start();
	 
	 new Thead(new Runnable(){
	 publid void run(){
	 		System.out.print("匿名内部类实现-2");
	 	};
	 }).start();
	}
}
```

###4.含返回值且可抛出异常的线程创建启动方式：有返回值
/*   
	call()只是线程任务,对线程任务进行封装  
			class FutureTask<V> implements   RunnableFuture<V>  
			interface RunnableFuture<V> extends Runnable,   Future<V>  */   
			
```java
public class ResultThread implements Callable<String>{
	public String call(){
	System.out.print(”正在执行线程任务");
	Thread.sleep(1000);
	return "线程执行完毕";
	}
	
	public static void main(String [] args){
		ResultThread t = new ResultThread();
		FutureTask<String> task = new FutureTask<>(d);
		Thread td = new Thread(task);
		td.start();
		String result = task.getResult();
		System.out.print("返回的结果是："+result);
	}
}

```

###5.线程池实现

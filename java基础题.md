#java基础  
1. Object中有哪些公共方法?
equals(),clone(),getClass(),notify(),notifyAll(),wait(),toString
2. ==和equals的区别  
``` 
 public static void testEquals(){ 		             
    String a =new String("123");       	
    String b= new String ("123");    
        System.out.println(a==b); //false,比较的是引用地址
        System.out.println(a.equals(b)); //true，比较的是内容值
    }
```
3. 抽象类和接口的区别
 - 抽象类不能实现，只能继承，子类继承后需要实现抽象方法。抽象类里面可以定义方法。  
 - 接口。

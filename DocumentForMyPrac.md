Questions
________________________________________
Question 1)
Which of the following lines will compile without warning or error. 

    1) float f=1.3; 
    2) char c="a"; 
    3) byte b=257; 
    4) boolean b=null; 
    5) int i=10; 
 
- A：
- 1) float f= 1.3F or f=1.3f;
- 2) c = 'a'
- 3)byte [-128,127]
- 4)boolean value is only true or false 
- 5) correct
> 
> 1、
基本类型：byte 二进制位数：8
包装类：java.lang.Byte
最小值：Byte.MIN_VALUE=-128（-2的7次方）
最大值：Byte.MAX_VALUE=127（2的7次方-1）
2、
基本类型：int 二进制位数：32
包装类：java.lang.Integer
最小值：Integer.MIN_VALUE= -2147483648 （-2的31次方）
最大值：Integer.MAX_VALUE= 2147483647 （2的31次方-1）
3、
基本类型：short 二进制位数：16
包装类：java.lang.Short
最小值：Short.MIN_VALUE=-32768 （-2的15次方）
最大值：Short.MAX_VALUE=32767 （2的15次方-1）
4、
基本类型：long 二进制位数：64
包装类：java.lang.Long
最小值：Long.MIN_VALUE=-9223372036854775808 （-2的63次方）
最大值：Long.MAX_VALUE=9223372036854775807 （2的63次方-1）
5、
基本类型：float 二进制位数：32
包装类：java.lang.Float
最小值：Float.MIN_VALUE=1.4E-45 （2的-149次方）
最大值：Float.MAX_VALUE=3.4028235E38 （2的128次方-1）
6、
基本类型：double 二进制位数：64
包装类：java.lang.Double
最小值：Double.MIN_VALUE=4.9E-324 （2的-1074次方）
最大值：Double.MAX_VALUE=1.7976931348623157E308 （2的1024次方-1）

_______________________________________
Question 2)
What will happen if you try to compile and run the following code 
    
    public class MyClass {
    public static void main(String arguments[]) {
    	amethod(arguments);
    }
    public void amethod(String[] arguments) {
    	System.out.println(arguments);
    	System.out.println(arguments[1]);
    }
    }
    
1. 1) error Can't make static reference to void amethod. 
1. 2) error method main not correct 
1. 3) error array must include parameter 
1. 4) amethod must be declared with String 

A：1） 无法从静态上下文中引用非静态变量
________________________________________
Question 3)
Which of the following will compile without error
 
    1) 
    import java.awt.*;
    package Mypackage;
    class Myclass {}
    2) 
    package MyPackage;
    import java.awt.*;
    class MyClass{}
    3) 
    /*This is a comment */
    
    package MyPackage;
    import java.awt.*;
    class MyClass{}
      
A： （2）&（3）
> 包声明应在源文件第一行；注释可以在任何地方；import语句应在package语句之后，所有类之前，
_______________________________________
    
    Question 4)
    A byte can be of what size 
    1) -128 to 127 
    2) (-2 power 8 )-1 to 2 power 8 
    3) -255 to 256 
    4)depends on the particular implementation of the Java Virtual machine

A：（1） 
________________________________________
Question 5)

    What will be printed out if this code is run with the following command line? 
    java myprog good morning
    public class myprog{
    public static void main(String argv[])
    {
    	System.out.println(argv[2]);
    }
    }
    1) myprog 
    2) good 
    3) morning 
    4) Exception raised: "java.lang.ArrayIndexOutOfBoundsException: 2" 
  
A：(4)
程序名不能做参数，这里参数为[good,morning]，所以为数组下标越界
________________________________________
Question 6)

    Which of the following are keywords or reserved words in Java? 
    1) if 
    2) then 
    3) goto 
    4) while 
    5) case 

A：（1）（3）（4）（5）注意 goto为保留字（reserved words）
________________________________________
Question 7)

    Which of the following are legal identifiers 
    1) 2variable 
    2) variable2 
    3) _whatavariable 
    4) _3_ 
    5) $anothervar 
    6) #myvar 
A：2 3 4 5 

> Java变量的基本命名法则：
> 1、以下划线、字母、美元符开头。( _ $ a )
> 2、后面跟下划线、字母、美元符以及数字。
> 3、 没有长度限制（但也不能太长！）。
> 4、对大小写敏感（意思是大小写代表不同含义）
> 
> Java驼峰式命名法：
> 1、变量名必须为有意义的单词
> 2、变量名如果只有一个单词，则小写
> 3、如果有2个以及多个单词，则从第一个单词的首字母小写，其后单词的首字母大写
> 4:
> 1、合法的变量名：$ad 、abc 、ajhs01
> 2、符合驼峰式命名法的变量名：play 、 $play01 、 playGame
> 关系：合法的变量名不一定遵守驼峰式命名法的规范，但符合驼峰是命名法的变量名一定合法。
> 在java变量命名中不仅变量名要合法而且也要遵守驼峰式命名法。

________________________________________
Question 8)

    What will happen when you compile and run the following code? 
      
    public class MyClass{
     static int i;
     public static void main(String argv[]){
     System.out.println(i);
     }
    }
    1) Error Variable i may not have been initialized 
    2) null 
    3) 1 
    4) 0 
A:(4)

> Java 八种基本类型 默认初始值：
> 
> 如果是 byte,short,int,long初值为0
> 
> 而float,double则为0.0
> 
> 至于   char则是 ' '(空格字符)
> 
> 最后是boolean   为false
> 
> ps:
> 对象->null
> 
> pps:上述是针对类中成员变量，
> 如1)   int[] a;   //声明,没有初始化默认值是null
> 
> 2)   int[] a=new int[5];   //初始化为默认值,int型为0
> 
> 如果是局部成员变量，JVM不会为其设置初始值，故必须先初始化才能使用




________________________________________
Question 9)

    What will happen if you try to compile and run the following code? 
    public class Q {
     public static void main(String argv[]){
     int anar[]=new int[]{1,2,3};
     System.out.println(anar[1]);
     }
    }
    1) 1 
    2) Error anar is referenced before it is initialized 
    3) 2 
    4) Error: size of array must be defined 
A: (3)

> 
> Java语法规定的，给数组赋值有以下方式
> 
> 1:int [] a = {1,3};
> 
> 2:int[] a = new int[]{1,3};
> 
> 3:int[] a = new int[2]; a[0] = 1; a[1] = 3;
> 
 

________________________________________
Question 10)

    What will happen if you try to compile and run the following code? 
    public class Q {
     public static void main(String argv[]){
     int anar[]=new int[5];
     System.out.println(anar[0]);
     }
    }
    1) Error: anar is referenced before it is initialized 
    2) null 
    3) 0 
    4) 5 
A：（3）
________________________________________
Question 11)

    What will be the result of attempting to compile and run the following code? 
    abstract class MineBase {
     abstract void amethod();
     static int i;
    }
    public class Mine extends MineBase {
     public static void main(String argv[]){
     int[] ar=new int[5];
     for(i=0;i < ar.length;i++)
     System.out.println(ar[i]);
     }
    }
    1) a sequence of 5 0's will be printed 
    2) Error: ar is used before it is initialized 
    3) Error Mine must be declared abstract 
    4) IndexOutOfBoundes Error 
A：（3）
要么声明为抽象类（declare abstract）要么把所有抽象方法都实现（implement all abstract methods）
________________________________________
Question 12)
    
    What will be printed out if you attempt to compile and run the following code ? 
    int i=1;
     switch (i) {
     case 0:
     System.out.println("zero");
     break;
     case 1:
     System.out.println("one");
     case 2:
     System.out.println("two");
     default:
     System.out.println("default");
     }
    1) one 
    2) one, default 
    3) one, two, default 
    4) default 
A:3)
________________________________________
Question 13)

    What will be printed out if you attempt to compile and run the following code? 
    int i=9;
    switch (i) {
     default:
     System.out.println("default");
     case 0:
     System.out.println("zero");
     break;
     case 1:
     System.out.println("one");
     case 2:
     System.out.println("two");
    }
    1) default 
    2) default, zero 
    3) error default clause not defined 
    4) no output displayed 
A：（2）

当找不到case label 时从default执行。
________________________________________
Question 14)

    Which of the following lines of code will compile without error 
    1) 
    int i=0;
    if(i) {
     System.out.println("Hello");
     }
    2) 
    boolean b=true;
    boolean b2=true;
    if(b==b2) {
     System.out.println("So true");
     }
    3) 
    int i=1;
    int j=2;
    if(i==1|| j==2)
     System.out.println("OK");
    4) 
    int i=1;
    int j=2;
    if(i==1 &| j==2)
    
     System.out.println("OK");

A：2 3
________________________________________
Question 15)

    What will be output if you try to compile and run the following code, but there is 
    no file called Hello.txt in the current directory?. 
    import java.io.*;
    public class Mine {
    public static void main(String argv[]){
    	Mine m=new Mine();
    	System.out.println(m.amethod());
    }
    public int amethod() {
    	try {
    	FileInputStream dis=new FileInputStream("Hello.txt");
    	}catch (FileNotFoundException fne) {
    	System.out.println("No such file found");
    	return -1;
    	}catch(IOException ioe) {
    	} finally{
    	System.out.println("Doing finally");
    	}
    
    	return 0;
    }
    
    }
    1) No such file found 
    2 No such file found ,-1 
    3) No such file found, Doing finally, -1 
    4) 0 
！！！！ A: （3）
这题很重要，可以结合Java源码和另一篇finally文档

> *finally 语句的执行顺序：
> finally 语句块是在 try 或者 catch 中的 return 语句之前执行的*
________________________________________
Question 16)

    Which of the following statements are true? 
    1) Methods cannot be overriden to be more private
    2) static methods cannot be overloaded
    3) private methods cannot be overloaded
    4) An overloaded method cannot throw exceptions not checked in the base class
A：(1）

**静态方法可以overload 但不可以override**



> override 和 overload 区别：
> override--**子类对父类方法的扩展**；在Java中覆盖继承父类的方法就是通过方法的重写来实现的。所谓方法的重写是指子类中的方法与父类中继承的方法**有完全相同的返回值类型、方法名、参数个数以及参数类型**。
> overload -- **在同一个类或其子类中的不同方法**，体现多态性
> 
> 
> **在重写override方法时，需要遵循以下的规则**： 

> (一) 父类方法的参数列表必须完全与被子类重写的方法的**参数列表相同**，否则不能称其为override而是overload。

> (二) 父类的返回类型必须与被子类重写的方法**返回类型相同**，否则不能称其为override而是overload。

> (三) Java中规定，**被子类重写的方法不能拥有比父类方法更加严格的访问权限**。编写过Java程序的人就知道，父类中的方法并不是在任何情况下都可以重写的，**当父类中方法的访问权限修饰符为private时，该方法只能被自己的类访问，不能被外部的类访问，在子类是不能被重写的。**如果定义父类的方法为public，在子类定义为private，程序运行时就会报错。

> (四) 在继承过程中如果父类当中的方法抛出异常，那么在子类中重写父类的该方法时，也要抛出异常，而且抛出的异常不能多于父类中抛出的异常(可以等于父类中抛出的异常)。**换句话说，重写方法一定不能抛出新的检查异常，或者比被重写方法声明更加宽泛的检查型异常。**例如，父类的一个方法申明了一个检查异常IOException，在重写这个方法时就不能抛出Exception，只能抛出IOException的子类异常，可以抛出非检查异常。同样的道理，如果子类中创建了一个成员变量，而该变量和父类中的一个变量名称相同，称作变量重写或属性覆盖。但是此概念一般很少有人去研究它，因为意义不大。
> 
> 
> 在使用**重载overload**要注意以下的几点: 

> - 1.在使用重载时只能通过不同的参数列表，**必须具有不同的参数列表**。 
- 2.不能通过访问权限、返回类型、抛出的异常进行重载。 
- 3.方法的**异常类型和数目不会对重载造成影响**。 
- 4.**可以有不同的返回类型**，只要参数列表不同就可以了。 
- 5.**可以有不同的访问修饰符**。 
- 6.**可以抛出不同的异常**。


________________________________________
Question 17)

    What will happen if you attempt to compile and run the following code? 
    class Base {}
    class Sub extends Base {}
    class Sub2 extends Base {}
    public class CEx{
    public static void main(String argv[]){
    	Base b=new Base();
    	Sub s=(Sub) b;
    }
    }
    1) Compile and run without error 
    2) Compile time Exception 
    3) Runtime Exception 
A：（3）ClassCastExceptin

子类不能强制转换为父类，除非父类是子类构造出的实例,如：

	Sub a = new Sub();
    Base up = a;
________________________________________
Question 18)

    Which of the following statements are true?
    1) System.out.println( -1 >>> 2);will output a result larger than 10
    2) System.out.println( -1 >>> 2); will output a positive number 
    3) System.out.println( 2 >> 1); will output the number 1 
    4) System.out.println( 1 <<< 2); will output the number 4

A：1 2 3


>  移位操作符操作的运算对象也是二进制的“位”。移位操作符只可用来处理整数类型，左移位操作符（<<）能按照操作符右侧指定的位数将操作符左边的操作数向左移动（在低位补0），“有符号”右移位操作符（>>）则按照操作符右侧指定的位数将操作符左边的操作数向右移。“有符号”右移位操作符使用“符号扩展”；若符号位正，则在高位插入0；若符号位负。则在高位插入1。java中增加了一种“无符号”右移位操作符（>>>）,他使用“零扩展”；无论正负，都在高位插入0。这一操作符是C或C++中所没有的

________________________________________
Question 19)

    What will happen when you attempt to compile and run the following code?
    public class Tux extends Thread{

        static String sName = "vandeleur";
        public static void main(String argv[]){
        Tux t = new Tux();
        t.piggy(sName);
        System.out.println(sName);
        
        }
        public void piggy(String sName){
                sName = sName + " wiggy";
        start();
        }
        public void run(){
        
        for(int i=0;i  <  4; i++){
                sName = sName + " " + i;
                
        }
        }

    }

    1) Compile time error
    2) Compilation and output of "vandeleur wiggy"
    3) Compilation and output of "vandeleur wiggy 0 1 2 3"
    4) Compilation and output of either "vandeleur", "vandeleur 0", "vandeleur 0 1" "vandaleur 0 1 2" or "vandaleur 0 1 2 3"
A：（4）
________________________________________
Question 20)

    What will be displayed when you attempt to compile and run the following code 
    //Code start
    import java.awt.*;
    public class Butt extends Frame{
    public static void main(String argv[]){
    	Butt MyBut=new Butt();
    }
    Butt(){
    	Button HelloBut=new Button("Hello");
    	Button ByeBut=new Button("Bye");
    	add(HelloBut);
    	add(ByeBut);
    	setSize(300,300);
    	setVisible(true);
    }
    }
    //Code end
    1) Two buttons side by side occupying all of the frame, Hello on the left and Bye on 
    the right 
    2) One button occupying the entire frame saying Hello 
    3) One button occupying the entire frame saying Bye 
    4) Two buttons at the top of the frame one saying Hello the other saying Bye 
 A：（3）   
________________________________________
Question 21)

    What will be output by the following code? 
    public class MyFor{
    public static void main(String argv[]){
    	int i;
    	int j;
    outer:
    	for (i=1;i <3;i++)
    	inner:
    	for(j=1; j<3; j++) {
    	if (j==2)
    		continue outer;
    	System.out.println("Value for i=" + i + " Value for j=" +j);
    	}
    }
    
    }
    1) Value for i=1 Value for j=1 
    2) Value for i=2 Value for j=1 
    3) Value for i=2 Value for j=2 
    4) Value for i=3 Value for j=1 

A： 1 2 
________________________________________
Question 22)

    Which statement is true of the following code?
    public class Agg{
    public static void main(String argv[]){
    	Agg a = new Agg();
    	a.go();
    	}
    	public void go(){
    		DSRoss ds1 = new DSRoss("one");
    		ds1.start();
    	}
    }
    
    class DSRoss extends Thread{
    private String sTname="";
    DSRoss(String s){
    	sTname = s;
    }
    public void run(){
    	notwait();
    	System.out.println("finished");
    }
    public void notwait(){
    	while(true){
    		try{
    	 		System.out.println("waiting");
    	 		wait();
    			}catch(InterruptedException ie){}
    		System.out.println(sTname);
    		notifyAll();
    		}
    	}
    	
    }
    1) It will cause a compile time error
    2) Compilation and output of "waiting"
    3) Compilation and output of "waiting" followed by "finished"
    4) Runtime error, an exception will be thrown
A：4
________________________________________
Question 23)

    Which of the following methods can be legally inserted in place of the comment //Method Here ? 
    class Base{
     public void amethod(int i) { }
    }
    
    public class Scope extends Base{
     public static void main(String argv[]){
     }
     //Method Here
    }
    1) void amethod(int i) throws Exception {} 
    2) void amethod(long i)throws Exception {} 
    3) void amethod(long i){} 
    4) public void amethod(int i) throws Exception {} 
 A ： 2 3 overload  
 ________________________________________

Question 24)

    Which of the following will output -4.0 
    1) System.out.println(Math.floor(-4.7)); 
    2) System.out.println(Math.round(-4.7)); 
    3) System.out.println(Math.ceil(-4.7)); 
    4) System.out.println(Math.min(-4.7)); 

A： 3

1 - > -5.0; 2 -> -5; 4 -> error min（a，b）
________________________________________
Question 25)
    
    What will happen if you attempt to compile and run the following code? 
    Integer ten=new Integer(10);
    Long nine=new Long (9);
    System.out.println(ten + nine);
    int i=1;
    System.out.println(i + ten);
    1) 19 followed by 20 
    2) 19 followed by 11 
    3) Compile time error 
    4) 10 followed by 1 
________________________________________
Question 26)

If you run the code below, what gets printed out? 
String s=new String("Bicycle");
int iBegin=1;
char iEnd=3;
System.out.println(s.substring(iBegin,iEnd));
1) Bic 
2) ic 
3) icy 
4) error: no method matching substring(int,char) 
________________________________________
Question 27)
If you wanted to find out where the position of the letter v (ie return 2) in the string s 
containing "Java", which of the following could you use? 
1) mid(2,s); 
2) charAt(2); 
3) s.indexOf('v'); 
4) indexOf(s,'v'); 
________________________________________
Question 28)
Given the following declarations 
String s1=new String("Hello")
String s2=new String("there");
String s3=new String();
Which of the following are legal operations? 
1) s3=s1 + s2; 
2) s3=s1-s2; 
3) s3=s1 & s2; 
4) s3=s1 && s2 
________________________________________
Question 29)
What is the result of the following operation? 
System.out.println(4 | 3); 
1) 6 
2) 0 
3) 1 
4) 7 
________________________________________
Question 30)
public class MyClass1 {
public static void main(String argv[]){ }
/*Modifier at XX */ class MyInner {}
}
What modifiers would be legal at XX in the above code? 
1) public 
2) private 
3) static 
4) friend 
________________________________________
Question 31)

What will happen when you attempt to compile and run the following code?
public class Holt extends Thread{
        private String sThreadName; 
        public static void main(String argv[]){
                Holt h = new Holt();
                h.go(); 
        }
Holt(){}

Holt(String s){
        sThreadName = s;
}
public String getThreadName(){
        return sThreadName;
}

public void go(){
        Holt first = new Holt("first");
        first.start();
        Holt second = new Holt("second");
        second.start();
}

        public void start(){
                for(int i = 0; i < 2; i ++){
                        System.out.println(getThreadName() +i);
                try{
                        Thread.sleep(100);
                        } catch(InterruptedException e){System.out.println(e.getMessage());}
                }
        }
}

1) Compile time error
2) Output of first0, second0, first0, second1
3) Output of first0, first1, second0, second1
4) Runtime error
________________________________________
Question 32)
An Applet has its Layout Manager set to the default of FlowLayout. What code would be correct to change to another Layout Manager. 
1) setLayoutManager(new GridLayout()); 
2) setLayout(new GridLayout(2,2)); 
3) setGridLayout(2,2);
4) setBorderLayout(); 
________________________________________
Question 33)

What will happen when you attempt to compile and run the following code?. 
class Background implements Runnable{
	int i=0;
		public int run(){
			 while(true){
				 i++;
				 System.out.println("i="+i);
				 } //End while
		     return 1;
	 }//End run

}//End class
1) It will compile and the run method will print out the increasing value of i. 
2) It will compile and calling start will print out the increasing value of i. 
3) The code will cause an error at compile time. 
4) Compilation will cause an error because while cannot take a parameter of true. 

________________________________________
Question 34)
Which of the following statements about this code are true?
public class Morecombe{
public static void main(String argv[]){
 	Morecombe m = new Morecombe();
	m.go(new Turing(){});	
}
public void go(Turing t){
	t.start();
	}

}
class Turing extends Thread{
	public void run(){
		for(int i =0; i < 2; i++){
			System.out.println(i);
		}	
	}	

}

1) Compilation error due to malformed parameter to go method
2) Compilation error, class Turing has no start method
3) Compilation and output of 0 followed by 1
4) Compilation but runtime error
________________________________________
Question 35)

What will be the result when you attempt to compile and run the following code?. 
public class Conv{
    public static void main(String argv[]){
	Conv c=new Conv();
	String s=new String("ello");
	c.amethod(s);
    }

    public void amethod(String s){
	char c='H';
	c+=s;
	System.out.println(c);
    }
}
1) Compilation and output the string "Hello" 
2) Compilation and output the string "ello" 
3) Compilation and output the string elloH 
4) Compile time error 
________________________________________
Question 36)
Given the following code, what test would you need to put in place of the comment line? 
//place test here 
to result in an output of the string 
Equal 
public class EqTest{
	 public static void main(String argv[]){
		 EqTest e=new EqTest();
 	}

	EqTest(){
		 String s="Java";
		 String s2="java";
		 //place test here {
			 System.out.println("Equal");
			 }else
			 {
			 System.out.println("Not equal");
		 }
	 }
}
1) if(s==s2) 
2) if(s.equals(s2) 
3) if(s.equalsIgnoreCase(s2)) 
4)if(s.noCaseMatch(s2)) 
________________________________________
Question 37)
Given the following code 
import java.awt.*;
public class SetF extends Frame{
public static void main(String argv[]){
 SetF s=new SetF();
 s.setSize(300,200);
 s.setVisible(true);
 }

}
How could you set the frame surface color to pink 
1)s.setBackground(Color.pink); 
2)s.setColor(PINK); 
3)s.Background(pink); 
4)s.color=Color.pink 
________________________________________
Question 38)

How can you change the current working directory using an instance of the File class called FileName? 
1) FileName.chdir("DirName") 
2) FileName.cd("DirName") 
3) FileName.cwd("DirName") 
4) The File class does not support directly changing the current directory. 
________________________________________
Question 39)
If you create a TextField  with a constructor to set it to occupy 5 columns, what difference will it make if you use it with a proportional font (ie Times Roman) or a fixed pitch typewriter style font (Courier). 
1)With a fixed font you will see 5 characters, with a  proportional it will depend on the width of the characters 
2)With a fixed font you will see 5 characters,with a  proportional it will cause the field to expand to fit the text 
3)The columns setting does not affect the number of characters displayed 
4)Both will show exactly 5 characters 
________________________________________
Question 40)

Given the following code how could you invoke the Base constructor that will print out the string "base constructor"; 
class Base{
    Base(int i){
	System.out.println("base constructor");
    }
    Base(){
    }
}

public class Sup extends Base{
    public static void main(String argv[]){
	Sup s= new Sup();
	//One
    }
    Sup()
    {
	//Two
    }

    public void derived()
    {
	//Three
    }
}
1) On the line After //One put Base(10); 
2) On the line After //One put super(10); 
3) On the line After //Two put super(10); 
4) On the line After //Three put super(10); 
________________________________________
Question 41)
Given the following code what will be output? 
public class Pass{
    static int j=20;
    public static void main(String argv[]){
	int i=10;
	Pass p = new Pass();
	p.amethod(i);
	System.out.println(i);
	System.out.println(j);
    }

    public void amethod(int x){
	x=x*2;
	j=j*2;
    }
}
1) Error: amethod parameter does not match variable 
2) 20 and 40 
3) 10 and 40 
4) 10, and 20 
________________________________________
Question 42)

What code placed after the comment //For loop would result in the population of every element of the array ia[] with a value from variable i.? 
public class Lin{
    public static void main(String argv[]){
	Lin l = new Lin();
	l.amethod();
    }
    public void amethod(){
	int ia[] = new int[4];
	//Start For loop
	{
	    ia[i]=i;
	    System.out.println(ia[i]);
	}
    }
}
1) for(int i=0; i < ia.length() -1; i++) 
2) for (int i=0; i< ia.length(); i++) 
3) for(int i=1; i < 4; i++) 
4) for(int i=0; i< ia.length;i++) 
________________________________________
Question 43)

What will be the result when you try to compile and run the following code? 
private class Base{
    Base(){
	int i = 100;
	System.out.println(i);
    }
}

public class Pri extends Base{
    static int i = 200;
    public static void main(String argv[]){
	Pri p = new Pri();
	System.out.println(i);
    }
}
1) Error at compile time 
2) 200 
3) 100 followed by 200 
4) 100 ________________________________________
Question 44)
What will the following code print out? 
public class Oct{
    public static void main(String argv[]){
	Oct o = new Oct();
	o.amethod();
    }
    public void amethod(){
	int oi= 012;
	System.out.println(oi);
    }
}
1)12 
2)012 
3)10 
4)10.0 
  
________________________________________
Question 45
What will happen when you try compiling and running this code? 
public class Ref{
    public static void main(String argv[]){
	Ref r = new Ref();
	r.amethod(r);
    }
    public void amethod(Ref r){
	int i=99;
	multi(r);
	System.out.println(i);
    }
    public void multi(Ref r){
	r.i = r.i*2;
    }
}
1) Error at compile time 
2) An output of 99 
3) An output of 198 
4) An error at runtime 
________________________________________
Question 46)
You need to create a class that will store unique object elements. You do not need to sort these elements but they must be unique. 
What interface might be most suitable to meet this need? 
1)Set 
2)List 
3)Map 
4)Vector 
  
________________________________________
Question 47)
Which of the following will successfully create an instance of the Vector class and add an element? 
1) Vector v=new Vector(99); 
v[1]=99; 
  
2) Vector v=new Vector(); 
v.addElement(99); 
  
3) Vector v=new Vector(); 
v.add(99); 
  
4 Vector v=new Vector(100); 
v.addElement("99"); 
________________________________________
Question 48)
You have created a simple Frame and overridden the paint method as follows 
public void paint(Graphics g){
g.drawString("Dolly",50,10);

}

What will be the result when you attempt to compile and run the program? 
1) The string "Dolly" will be displayed at the centre of the frame 
2) An error at compilation complaining at the signature of the paint method 
3) The lower part of the word Dolly will be seen at the top of the frame, with the top hidden. 
4) The string "Dolly" will be shown at the bottom of the frame. 
________________________________________
Question 49)
What will be the result when you attempt to compile this program? 
public class Rand{
    public static void main(String argv[]){
	int iRand;
	iRand = Math.random();
	System.out.println(iRand);
    }
}
1) Compile time error referring to a cast problem 
2) A random number between 1 and 10 
3) A random number between 0 and 1 
4) A compile time error about random being an unrecognised method 
________________________________________
Question 50)
Given the following code 
import java.io.*;
public class Th{
    public static void main(String argv[]){
	Th t = new Th();
	t.amethod();
    }
    public void amethod(){
	try{
	    ioCall();
	}catch(IOException ioe){}
    }
}
What code would be most likely for the body of the ioCall method 
1) public void ioCall ()throws IOException{
 DataInputStream din = new DataInputStream(System.in);
 din.readChar();
 }
2) public void ioCall ()throw IOException{
 DataInputStream din = new DataInputStream(System.in);
 din.readChar();
 }
3) public void ioCall (){
 DataInputStream din = new DataInputStream(System.in);
 din.readChar();
 }
4) public void ioCall throws IOException(){
 DataInputStream din = new DataInputStream(System.in);
 din.readChar();

 }
________________________________________
Question 51)
What will happen when you compile and run the following code? 
public class Scope{
    private int i;
    public static void main(String argv[]){
	Scope s = new Scope();
	s.amethod();
    }//End of main
    public static void amethod(){
	System.out.println(i);
    }//end of amethod
}//End of class

1) A value of 0 will be printed out 
2) Nothing will be printed out 
3) A compile time error 
4) A compile time error complaining of the scope of the variable i 
________________________________________
Question 52)

You want to lay out a set of buttons horizontally but with more space between the first button and the rest. You are going to use the GridBagLayout manager to control the way the buttons are set out. How will you modify the way the GridBagLayout acts in order to change the spacing around the first button? 
  
1) Create an instance of the GridBagConstraints class, call the weightx() method and then pass the GridBagConstraints instance with the component to the setConstraints method of the GridBagLayout class. 
2) Create an instance of the GridBagConstraints class, set the weightx field and then pass the GridBagConstraints instance with the component to the setConstraints method of the GridBagLayout class. 
3) Create an instance of the GridBagLayout class, set the weightx field and then call the setConstraints method of the GridBagLayoutClass with the component as a parameter. 
4) Create an instance of the GridBagLayout class, call the setWeightx() method and then pass the GridBagConstraints instance with the component to the setConstraints method of the GridBagLayout class. 
________________________________________
Question 53)

Which of the following can you perform using the File class? 
1) Change the current directory 
2) Return the name of the parent directory 
3) Delete a file 
4) Find if a file contains text or binary information 
________________________________________
Question 54)
Which statement is true of the following code?
public class Rpcraven{
	public static void main(String argv[]){
	Pmcraven pm1 = new Pmcraven("One");
	pm1.run();
	Pmcraven pm2 = new Pmcraven("Two");
	pm2.run();

	}
}

class Pmcraven extends Thread{
private String sTname="";
Pmcraven(String s){
	sTname = s;

}
public void run(){
	for(int i =0; i < 2 ; i++){
		try{
		 sleep(1000);
		}catch(InterruptedException e){}

		yield();
		System.out.println(sTname);
		}

	}
}
1) Compile time error, class Rpcraven does not import java.lang.Thread
2) Output of One One Two Two
3) Output of One Two One Two
4) Compilation but no output at runtime
________________________________________
Question 55)
You are concerned that your program may attempt to use more memory than is available. To avoid this situation you want to ensure that the Java Virtual Machine will run its garbage collection just before you start a complex routine. What can you do to be certain that garbage collection will run when you want . 
1) You cannot be certain when garbage collection will run 
2) Use the Runtime.gc() method to force garbage collection 
3) Ensure that all the variables you require to be garbage collected are set to null 
4) Use the System.gc() method to force garbage collection 
________________________________________
Question 56)
You are using the GridBagLayout manager to place a series of buttons on a Frame. You want to make the size of one of the buttons bigger than the text it contains. Which of the following will allow you to do that?
1) The GridBagLayout manager does not allow you to do this 
2) The setFill method of the GridBagLayout class 
3) The setFill method of the GridBagConstraints class 
4) The fill field of the GridBagConstraints class 
  
________________________________________
Question 57)
Which of the following most closely describes a bitset collection? 
1) A class that contains groups of unique sequences of bits 
2) A method for flipping individual bits in instance of a primitive type 
3) An array of boolean primitives that indicate zeros or ones 
4) A collection for storing bits as on-off information, like a vector of bits 
________________________________________
Question 58)

You have these files in the same directory. What will happen when you attempt to compile and run Class1.java if you have not already compiled Base.java 
//Base.java
package Base;
class Base{
    protected void amethod(){
	System.out.println("amethod");
    }//End of amethod
}//End of class base
package Class1;
//Class1.java
public class Class1 extends Base{
    public static void main(String argv[]){
	Base b = new Base();
	b.amethod();
    }//End of main

}//End of Class1



1) Compile Error: Methods in Base not found 
2) Compile Error: Unable to access protected method in base class 
3) Compilation followed by the output "amethod" 
4)Compile error: Superclass Class1.Base of class Class1.Class1 not found 
________________________________________
Question 59)
What will happen when you attempt to compile and run the following code 
class Base{
    private void amethod(int iBase){
	System.out.println("Base.amethod");
    }
}



class Over extends Base{
    public static void main(String argv[]){
	Over o = new Over();
	int iBase=0;
	o.amethod(iBase);
    }

    public void amethod(int iOver){
	System.out.println("Over.amethod");
    }
}
1) Compile time error complaining that Base.amethod is private 
2) Runtime error complaining that Base.amethod is private 
3) Output of "Base.amethod"
4) Output of "Over.amethod" 
  
________________________________________
Question 60)
You are creating an applet with a Frame that contains buttons. You are using the GridBagLayout manager and you have added Four buttons. At the moment the buttons appear in the centre of the frame from left to right. You want them to appear one on top of the other going down the screen. What is the most appropriate way to do this. 
  
1) Set the gridy value of the GridBagConstraints class to a value increasing from 1 to 4 
2) set the fill value of the GridBagConstraints class to VERTICAL 
3) Set the ipady value of the GridBagConstraints class to a value increasing from 0 to 4 
4) Set the fill value of the GridBagLayouts class to GridBag.VERTICAL 






答案
Answer 1)

Back to question 1) 
Objective 4.5)

5) int i=10;

explanation: 
1) float f=1.3; 
Will not compile because the default type of a number with a floating point component is a double. This would compile with a cast as in

float f=(float) 1.3 
 

2) char c="a";

Will not compile because a char (16 bit unsigned integer) must be defined with single quotes. This would compile if it were in the form

char c='a';

3) byte b=257;

Will not compile because a byte is eight bits. Take of one bit for the sign component you can define numbers between

-128 to +127

4) a boolean value can either be true or false, null is not allowed

http://www.jchq.net/tutorial/04_05Tut.htm.

Answer 2)

Back to question 2)

Objective 4.1

1) Can't make static reference to void amethod.

Because main is defined as static you need to create an instance of the class in order to call any non-static methods. Thus a typical way to do this would be. 
 

MyClass m=new MyClass();

m.amethod(); 
 

Answer 2 is an attempt to confuse because the convention is for a main method to be in the form

String argv[]

That argv is just a convention and any acceptable identifier for a string array can be used. Answers 3 and 4 are just nonsense.

http://www.jchq.net/tutorial/04_01Tut.htm
Answer 3)

back to Question 3) 
Objective 4.1)

2 and 3 will compile without error. 
 

1 will not compile because any package declaration must come before any other code. Comments may appear anywhere

http://www.jchq.net/tutorial/04_01Tut.htm .

Answer 4)

Back to question 4) 
Objective 4.5)

1) A byte is a signed 8 bit integer.

http://www.jchq.net/tutorial/04_05Tut.htm
Answer 5)

Back to question 5) 
Objective 4.2)

4) Exception raised: "java.lang.ArrayIndexOutOfBoundsException: 2"

Unlike C/C++ java does not start the parameter count with the program name. It does however start from zero. So in this case zero starts with good, morning would be 1 and there is no parameter 2 so an exception is raised.

http://www.jchq.net/tutorial/04_02Tut.htm
Answer 6)

Back to question 6) 
Objective 4.3)

1) if 
3) goto 
4) while 
5) case 
 

then is not a Java keyword, though if you are from a VB background you might think it was. Goto is a reserved word in Java.

http://www.jchq.net/tutorial/04_03Tut.htm
Answer 7)

Back to Question 7) 
Objective 4.1)

2) variable2 
3) _whatavariable 
4) _3_ 
5) $anothervar 
 

An identifier can begin with a letter (most common) or a dollar sign($) or an underscore(_). An identifier cannot start with anything else such as a number, a hash, # or a dash -. An identifier cannot have a dash in its body, but it may have an underscore _. Choice 4) _3_ looks strange but it is an acceptable, if unwise form for an identifier.

http://www.jchq.net/tutorial/04_01Tut.htm
Answer 8)

Back to Question 8) 
Objective 4.4)

4) 0

Class level variables are always initialised to default values. In the case of an int this will be 0. Method level variables are not given default values and if you attempt to use one before it has been initialised it will cause the

Error Variable i may not have been initialized
type of error.

http://www.jchq.net/tutorial/04_04Tut.htm
Answer 9)

Back to Question 9) 
Objective 4.4)

3 ) 2

No error will be triggered.

Like in C/C++, arrays are always referenced from 0. Java allows an array to be populated at creation time. The size of array is taken from the number of initializers. If you put a size within any of the square brackets you will get an error.

http://www.jchq.net/tutorial/04_04Tut.htm
Answer 10)

Back to question 10) 
Objective 4.4)

3) 0

Arrays are always initialised when they are created. As this is an array of ints it will be initalised with zeros.

http://www.jchq.net/tutorial/04_04Tut.htm
Answer 11)

Back to Question 11) 
Objective 1.2

3) Error Mine must be declared abstract 
 

A class that contains an abstract method must itself be declared as abstract. It may however contain non abstract methods. Any class derived from an abstract class must either define all of the abstract methods or be declared abstract itself.

http://www.jchq.net/tutorial/01_021Tut.htm
Answer 12)

Back to Question 12) 
Objective 2.1)

3) one, two, default

Code will continue to fall through a case statement until it encounters a break.

http://www.jchq.net/tutorial/02_01Tut.htm
Answer 13)

Back to Question 13) 
Objective 4.1)

2) default, zero

Although it is normally placed last the default statement does not have to be the last item as you fall through the case block. Because there is no case label found matching the expression the default label is executed and the code continues to fall through until it encounters a break.

http://www.jchq.net/tutorial/04_01Tut.htm
Answer 14)

Back to Question 14) 
Objective 5.1

2,3

Example 1 will not compile because if must always test a boolean. This can catch out C/C++ programmers who expect the test to be for either 0 or not 0.

http://www.jchq.net/tutorial/05_01Tut.htm
Answer 15)

Back to Question 15) 
Objective 11.5)

3) No such file found, doing finally, -1

The no such file found message is to be expected, however you can get caught out if you are not aware that the finally clause is almost always executed, even if there is a return statement.

http://www.jchq.net/tutorial/11_05Tut.htm
Answer 16)

Back to Question 16) 
Objective 6.2)

1) Methods cannot be overriden to be more private

Static methods cannot be overriden but they can be overloaded. If you have doubts about that statement, please follow and read carefully the link given to the Sun tutorial below. There is no logic or reason why private methods should not be overloaded. Option 4 is a jumbled up version of the limitations of exceptions for overriden methods

http://www.jchq.net/tutorial/06_02Tut.htm
http://java.sun.com/docs/books/tutorial/java/javaOO/override.html 
 

Answer 17)

 Back to Question 17) 
Objective 6.2)

3) Runtime Exception

Without the cast to sub you would get a compile time error. The cast tells the compiler that you really mean to do this and the actual type of b does not get resolved until runtime. Casting down the object hierarchy is a problem, as the compiler cannot be sure what has been implemented in descendent classes. Casting up is not a problem because sub classes will have the features of the base classes. This can feel counter intuitive if you are aware that with primitives casting is allowed for widening operations (ie byte to int).

http://www.jchq.net/tutorial/06_02Tut.htm
Answer 18)

Back to question 18) 
Objective 5.1)

1) System.out.println( -1 >>> 2);will output a result larger than 10
2) System.out.println( -1 >>> 2); will output a positive number 
3) System.out.println( 2 >> 1); will output the number 1

You can test this with the following class

public class shift{
static int i=2;
public static void main(String argv[]){
        System.out.println( -1  >>> 2);
        System.out.println( -1  >>> 2);
        System.out.println( 2  >> 1);
        }

}
Java does not have a <<< operator. The operation 1 << 2 would output 4

Because of the way twos complement number representation works the unsigned right shift operation means a small shift in a negative number can return a very large value so the output of option 1 will be much larger than 10.

The unsigned right shift places no significance on the leading bit that indicates the sign. For this shift the value 1 of the bit sign is replaced with a zero turning the result into a positive number for option 2.

http://www.jchq.net/tutorial/05_01Tut.htm
Answer 19)

Back to Question 19) 
Objective 7.1)

4) Compilation and output of either "vandaleur", "vandaleur 0", "vandaleur 0 1" "vandaleur 0 1 2" or "vandaleur 0 1 2 3"
If that seems a vauge answer it is because you cannot be certain of the system that the underlying OS uses for allocating cycles for a Thread. The chances are that once the thread has been spun off in the call to start in the method piggy the main method will run to completion and the value of sName will still be vandeluer before the Thread modifies it. You cannot be certain of this though.

http://www.jchq.net/tutorial/07_01Tut.htm

Answer 20)

Back to Question 20) 
Objective 8.1)

3) One button occupying the entire frame saying Bye

The default layout manager for a Frame is a border layout. If directions are not given (ie North, South, East or West), any button will simply go in the centre and occupy all the space. An additional button will simply be placed over the previous button. What you would probably want in a real example is to set up a flow layout as in

setLayout(new FlowLayout()); 

Which would allow the buttons to both appear side by side, given the appropriate font and size.
Applets and panels have a default FlowLayout manager

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 21)

Back to Question 21) 
Objective 2.2)

1,2

Value for i=1 Value for j=1 
Value for i=2 Value for j=1 
 

The statement continue outer causes the code to jump to the label outer and the for loop increments to the next number.

http://www.jchq.net/tutorial/02_02Tut.htm
Answer 22)
Back to Question 22) 
Objective 7.3)

4) Runtime error, an exception will be thrown

A call to wait/notify must be within synchronized code. With JDK1.2 this code throws the error message

java.lang.IllegalMonitorStateException: current thread not owner
        at java.lang.Object.wait(Native Method)
        at java.lang.Object.wait(Object.java:424)
        at DSRoss.notwait(Compiled Code)
        at DSRoss.run(Agg.java:21)
http://www.jchq.net/tutorial/07_03Tut.htm
Answer 23)

Back to Question 23) 
Objective 2.3)

2,3

Options 1, & 4 will not compile as they attempt to throw Exceptions not declared in the base class. Because options 2 and 3 take a parameter of type long they represent overloading not overriding and there is no such limitations on overloaded methods.

http://www.jchq.net/tutorial/02_03Tut.htm
Answer 24)

Back to Question 24) 
Objective 9.1)

3) System.out.println(Math.ceil(-4.7));

Options 1 and 2 will produce -5 and option 4 will not compile because the min method requires 2 parameters.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 25)

Back to Question 25 
Objective 4.5)

3) Compile time error

The wrapper classes cannot be used like primitives.

Depending on your compiler you will get an error that says someting like "Error: Can't convert java lang Integer". Wrapper classes have similar names to primitives but all start with upper case letters.

Thus in this case we have int as a primitive and Integer as a wrapper. The objectives do not specifically mention the wrapper classes but don't be surprised if they come up.

http://www.jchq.net/tutorial/04_05Tut.htm
Answer 26)

Back to Question 26) 
Objective 4.5)

2) ic

This is a bit of a catch question. Anyone with a C/C++ background would figure out that addressing in strings starts with 0 so that 1 corresponds to i in the string Bicycle. The catch is that the second parameter returns the endcharacter minus 1. In this case it means instead of the "icy" being returned as intuition would expect it is only "ic".

http://www.jchq.net/tutorial/04_05Tut.htm
Answer 27)

Back to Question 27) 
Objective 9.2)

3) s.indexOf('v');

charAt returns the letter at the position rather than searching for a letter and returning the position, MID is just to confuse the Basic Programmers, indexOf(s,'v'); is how some future VB/J++ nightmare hybrid, might perform such a calculation.

http://www.jchq.net/tutorial/09_02Tut.htm

Answer 28)

Objective 5.1)
Back to Question 28

1) s3=s1 + s2;

Java does not allow operator overloading as in C++, but for the sake of convenience the + operator is overridden for strings.

http://www.jchq.net/tutorial/05_01Tut.htm
Answer 29)

Back to Question 29) 
Objective 5.3)

4) 7

The | is known as the Or operator, you could think of it as the either/or operator. Turning the numbers into binary gives

4=100

3=011

For each position, if either number contains a 1 the result will contain a result in that position. As every position contains a 1 the result will be

111

Which is decimal 7.

http://www.jchq.net/tutorial/05_03Tut.htm
Answer 30)

Back to Question 30 
Objective 4.1)

1,2,3

public, private, static are all legal access modifiers for this inner class.

http://www.jchq.net/tutorial/04_01Tut.htm
Answer 31)

Back to Question 31 
Objective 7.1

3) Output of first0, first1, second0, second1

Note that this code overrides and calls the start method. If you wished to get the output mixed you would need to override the run method but call the start method.

http://www.jchq.net/tutorial/07_01Tut.htm
Answer 32)

Back to Question 32) 
Objective 8.1) 
 

2) setLayout(new GridLayout(2,2)); 
 

Changing the layout manager is the same for an Applet or an application. Answer 1 is wrong though it might have been a reasonable name for the designers to choose. Answers 3 and 4 are incorrect because changing the layout manager always requires an instance of one of the Layout Managers and these are bogus methods.

Instead of creating the anonymous instance of the Layout manager as in option 2 you can also create a named instance and pass that as a parameter. This is often what automatic code generators such as Borland/Inprise JBuilder do.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 33)

Back to Question 33) 
Objective 7.1) 
 

3) The code will cause an error at compile time

The error is caused because run should have a void not an int return type.

Any class that is implements an interface must create a method to match all of the methods in the interface. The Runnable interface has one method called run that has a void return type.The sun compiler gives the error

Method redefined with different return type: int run() was defined as void run();

http://www.jchq.net/tutorial/07_01Tut.htm
Answer 34)

Back to Question 34) 
Objective 7.1)

3) Compilation and output of 0 followed by 1

The creation of an anonymous class as a parameter to go is fairly strange as you would expect it to override a method in its parent class (Turing). You don't have to though. The fact that class Turing extends Thread means the anonymous instance that is passed to go has a start method which then calls the run method.

http://www.jchq.net/tutorial/07_01Tut.htm
Answer 35)

Back to Question 35 
Objective 5.1)
 

4) Compile time error 
 

The only operator overloading offered by java is the + sign for the String class. A char is a 16 bit integer and cannot be concatenated to a string with the + operator.

http://www.jchq.net/tutorial/05_01Tut.htm
Answer 36)

Back to Question 36 
Objective 5.2)

3) if(s.equalsIgnoreCase(s2))

String comparison is case sensitive so using the equals string method will not return a match. Using the==operator just compares where memory address of the references and noCaseMatch was just something I made up to give me a fourth slightly plausible option.

http://www.jchq.net/tutorial/05_02Tut.htm
Answer 37)

Back to Question 37 
Objective 8.1)

1) s.setBackground(Color.pink);

For speakers of the more British spelt English note that there is no letter u in Color. Also the constants for colors are in lower case.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 38)

Back to Question 38) 
Objective 11.1)

4) The File class does not support directly changing the current directory.

This seems rather surprising to me, as changing the current directory is a very common requirement. You may be able to get around this limitation by creating a new instance of the File class passing the new directory to the constructor as the path name.

http://www.jchq.net/tutorial/011_01Tut.htm
Answer 39)

Back to Question 39) 
Objective 8.1)

1)With a fixed font you will see 5 characters, with a  proportional it will depend on the width of the characters

With a proportional font the letter w will occupy more space than the letter i. So if you have all wide characters you may have to scroll to the right to see the entire text of a TextField.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 40)

Back to Question 40) 
Objective 6.2

3) On the line After //Two put super(10);

Constructors can only be invoked from within constructors.

http://www.jchq.net/tutorial/06_02Tut.htm
Answer 41)

Back to Question 41) 
Objective 5.4)

3) 10 and 40

when a parameter is passed to a method the method receives a copy of the value. The method can modify its value without affecting the original copy. Thus in this example when the value is printed out the method has not changed the value.

http://www.jchq.net/tutorial/05_04Tut.htm
Answer 42)

Back to Question 42 
Objective 1.1

4) for(int i=0; i< ia.length;i++)

Although you could control the looping with a literal number as with the number 4 used in option 3, it is better practice to use the length property of an array. This provides against bugs that might result if the size of the array changes. This question also checks that you know that arrays starts from zero and not One as option 3 starts from one. Remember that array length is a field and not a function like the String length() method.

http://www.jchq.net/tutorial/01_01Tut.htm
Answer 43)

Back to Question 43) 
Objective 1.2

1) Error at compile time

This is a slightly sneaky one as it looks like a question about constructors, but it is attempting to test knowledge of the use of the private modifier. A top level class cannot be defined as private. If you didn't notice the modifier private, remember in the exam to be real careful to read every part of the question.

http://www.jchq.net/tutorial/01_02Tut.htm
Answer 44)

Back to Question 44 
Objective 4.5)

3)10

The name of the class might give you a clue with this question, Oct for Octal. Prefixing a number with a zero indicates that it is in Octal format. Thus when printed out it gets converted to base ten. 012 in octal means the first column from the right has a value of 2 and the next along has a value of one times eight. In decimal that adds up to 10.

http://www.jchq.net/tutorial/04_05Tut.htm
Answer 45)

Back to Question 45 
Objective 1.2)

1) Error at compile time

The variable i is created at the level of amethod and will not be available inside the method multi.

http://www.jchq.net/tutorial/01_02Tut.htm
Answer 46)

Back to Question 46 
Objective 10.1)

1) Set

The Set interface ensures that its elements are unique, but does not order the elements. In reality you probably wouldn't create your own class using the Set interface. You would be more likely to use one of the JDK classes that use the Set interface such as HashSet or TreeSet.

http://www.jchq.net/tutorial/10_01Tut.htm
Answer 47)

Back to Question 47 
Objective 10.1)

4) Vector v=new Vector(100); 
v.addElement("99")

A vector can only store objects not primitives. The parameter "99" for the addElement method pases a string object to the Vector. Option 1) creates a vector OK but then uses array syntax to attempt to assign a primitive. Option 2 also creates a vector then uses correct Vector syntax but falls over when the parameter is a primitive instead of an object.

http://www.jchq.net/tutorial/10_01Tut.htm
Answer 48)

Objective 8.1) 
Back to Question 48

3) The lower part of the word Dolly will be seen at the top of the form

The Second parameter to the drawstring method indicates where the baseline of the string will be placed. Thus the 3rd parameter of 10 indicates the Y coordinate to be 10 pixels from the top of the Frame. This will result in just the bottom of the string Dolly showing up or possibly only the descending part of the letter y.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 49)

Back to Question 49) 
Objective 9.1)

1) Compile time error referring to a cast problem

This is a bit of a sneaky one as the Math.random method returns a pseudo random number between 0 and 1, and thus option 3 is a plausible Answer. However the number returned is a double and so the compiler will complain that a cast is needed to convert a double to an int.

http://www.jchq.net/tutorial/09_01Tut.htm
Answer 50)

Objective 2.3) 
Back to question 50

1) public void ioCall ()throws IOException{
 DataInputStream din = new DataInputStream(System.in);
 din.readChar();
 }
If a method might throw an exception it must either be caught within the method with a try/catch block, or the method must indicate the exception to any calling method by use of the throws statement in its declaration. Without this, an error will occur at compile time.

http://www.jchq.net/tutorial/02_03Tut.htm

Answer 51)

Objective 1.2) 
Back to Question 51)

3) A compile time error

Because only one instance of a static method exists not matter how many instance of the class exists it cannot access any non static variables. The JVM cannot know which instance of the variable to access. Thus you will get an error saying something like

Can't make a static reference to a non static variable
http://www.jchq.net/tutorial/01_02Tut.htm
Answer 52)

Objective 8.1) 
Back to Question 52) 
 

2) Create an instance of the GridBagConstraints class, set the weightx field and then pass the GridBagConstraints instance with the component to the setConstraints method of the GridBagLayout class. 
 

The Key to using the GridBagLayout manager is the GridBagConstraint class. This class is not consistent with the general naming conventions in the java API as you would expect that weightx would be set with a method, whereas it is a simple field (variable).

If you have a copy of the Roberts and Heller Java2 Guide that says the exam does not cover the GridBagLayout, this is an error which is corrected in later versions of the book

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 53)

Objective 11.1) 
Back to Question 53)

2) Return the name of the parent directory 
3) Delete a file

It is surprising that you can't change the current directory. It is not so surprising that you can't tell if a file contains text or binary information.

http://www.jchq.net/tutorial/11_01Tut.htm
Answer 54)

Back to Question 54)
Objective 7.1

2) Output of One One Two Two

Answer 3 would would be true if the code called the start method instead of the run method (well it is on my Windows machine anyway, I'm not sure it would be for ever implementation of Java Threads). If you call the run method directly it just acts as any other method and does not return to the calling code until it has finished executing. 
http://www.jchq.net/tutorial/07_01Tut.htm
Answer 55)

Objective 3.1) 
Back to Question 55)

1) You cannot be certain when garbage collection will run

Although there is a Runtime.gc(), this only suggests that the Java Virtual Machine does its garbage collection. You can never be certain when the garbage collector will run. Roberts and Heller is more specific abou this than Boone. This uncertainty can cause consternation for C++ programmers who wish to run finalize methods with the same intent as they use destructor methods.

http://www.jchq.net/tutorial/03_01Tut.htm
Answer 56)

Objective 8.1) 
Back to Question 56)

4) The fill field of the GridBagConstraints class

Unlike the GridLayout manager you can set the individual size of a control such as a button using the GridBagLayout manager. A little background knowledge would indicate that it should be controlled by a setSomethingOrOther method, but it isn't.

If you have a copy of the Roberts and Heller Java2 Guide that says the exam does not cover the GridBagLayout, this is an error. You can confirm this by looking at the online errata at

http://www.sybex.com/cgi-bin/rd_err_temp.pl?2463err.html.

http://www.jchq.net/tutorial/08_01Tut.htm
Answer 57)

Objective 10.1) 
Back to Question 57)

4) A collection for storing bits as on-off information, like a vector of bits

This is the description given to a bitset in Bruce Eckels "Thinking in Java" book. The reference to unique sequence of bits was an attempt to mislead because of the use of the word Set in the name bitset. Normally something called a set implies uniqueness of the members, but not in this context.

http://www.jchq.net/tutorial/10_01Tut.htm
Answer 58)

Back to Question 58) 
Objective 4.1)

4)Compile error: Superclass Class1.Base of class Class1.Class1 not found

Using the package statement has an effect similar to placing a source file into a different directory. Because the files are in different packages they cannot see each other. The stuff about File1 not having been compiled was just to mislead, java has the equivalent of an "automake", whereby if it was not for the package statements the other file would have been automatically compiled.

http://www.jchq.net/tutorial/04_01Tut.htm
Answer 59)

Back to Question 59) 
Objective 6.2)

4) Output of Over.amethod()

The names of parameters to an overridden method is not important, but as the version of amethod in class Base is set to be private it is not visible within Over (despite Over extending Base) and thus does not take part in overriding.

http://www.jchq.net/tutorial/06_02Tut.htm
Answer 60)

Objective 8.1) 
Back to Question 60)

1) Set the gridy value of the GridBagConstraints class to a value increasing from 1 to 4

Answer 4 is fairly obviously bogus as it is the GridBagConstraints class that does most of the magic in laying out components under the GridBagLayout manager. The fill value of the GridBagConstraints class controls the behavior inside its virtual cell and the ipady field controls the internal padding around a component.

If you have a copy of the Roberts and Heller Java2 Guide that says the exam does not cover the GridBagLayout, this is an error. You can confirm this by looking at t

---
layout: article
title: java 学习笔记

---



# java学习笔记

- 以下哪项不属于计算机硬件的范畴？C

  A、CPU

  B、内存

  C、程序

  D、总线

- 2、

  关于指令集，以下描述有误的一项是？D

  A、机器指令由“0”“1”组成

  B、指令集规定指令格式

  C、指令集能够被机器理解

  D、指令集是一成不变的

- 1、

  以下那种语言是机器能直接理解并执行的？A

  A、机器语言

  B、汇编语言

  C、高级语言

- 2、

  以下哪种语言支持跨平台？C

  A、机器语言

  B、汇编语言

  C、高级语言

  - 1、

    编译 Java 源程序需要以下哪一项？C

    A、JVM

    B、JRE

    C、JDK

  - 2、

    以下哪些命令有错误？ABC

    A、java test.java

    B、javac test.cpp

    C、javac test

    D、javac test.java

    E、java test

- 1、Java 属于什么语言？C

  A、机器语言

  B、汇编语言

  C、高级语言

- 2、Java 在从哪个版本根据用途分为三个版本？B

  A、Java 1.1

  B、Java 1.2

  C、Java 1.3

  D、Java 1.8

  ```java
  package step5;
  //输出入门代码"Hello Java！"
  public class FirstJavaCode {
      //请在指定位置填写代码。
      /********* Begin *********/
  public static void main(String[] args) {
      System.out.print("Hello Java!");
  }
  
      /********* End *********/
  
  }
  ```

  

```java
package step1;
import java.util.Scanner;
//实现求三个数的平均值的功能。
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double result = 0.0;

        //请在指定位置填写代码。
        /********* Begin *********/
        double a = input.nextDouble();
        double b = input.nextDouble();
        double c = input.nextDouble();
        result = (a+b+c)/3;
        /********* End *********/

        input.close();
        System.out.print(String.format("%.1f", result));
    }
}
```

```java
package step2;
import java.util.Scanner;
//摄氏度转华氏度
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double C = input.nextDouble();
        input.close();
        double F;

        //请在指定位置填写代码。
        /********* Begin *********/
        F=C*9.0/5.0+32.00;
        System.out.println(String.format("%.2f",F));

        /********* End *********/

    }
}
```

```java
package step1;
import java.util.Scanner;
/**按要求计算复利值并打印结果。
本金 100，年利率 12%；
月利率 = 0.12/12 = 0.01；
按月复利时，
第一个月的账上金额：100 * (1+0.01) = 101；
第二个月的账上金额： 101 * (1+0.01) = 102.01；
第三个月的账上金额： 102.01 * (1+0.01) = 103.0301；
……
依次类推。
**/
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        double monthrate;
        // 输入本金
        double capital = input.nextDouble();
        // 输入利息
        double interest = input.nextDouble();
        input.close();

        //请在指定位置填写代码。
        /********* Begin *********/
        monthrate = interest/100/12;

        for(int i=0;i<6;i++){
            capital *= (1+monthrate);
            System.out.println(String.format("%.2f",capital));
        }

        /********* End *********/
    }
}
```

```java
package step2;
import java.util.Scanner;
//计算整数各位和
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // 输入十进制整数
        int num;
        int result = 0;
        int number = input.nextInt();
        input.close();

        //请在指定位置填写代码。
        /********* Begin *********/
         while (number!=0){
            num=number%10; //获取每一位
            number=number/10;	//整数退一位
       
            result += num;
         }
         System.out.print(result);
        /********* End *********/

    }
}
```

```java
package step1;
import java.util.Scanner;
//整钱兑零
public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int money = input.nextInt();
        input.close();
        
        //请在指定位置填写代码。
        /********* Begin *********/
		//找出美元数量
		int dollar = money/100;
		money = money%100;
		//找quarter数量
		int quarter = money/25;
		money = money%25;
		//找dime数量
		int dime = money/10;
		money = money%10;
		int nickel = money/5;
		money = money%5;
		int penny = money/1;

            System.out.println(dollar + " dollar");
	    System.out.println(quarter + " quarter");
	    System.out.println(dime + " dime");
	    System.out.println(nickel + " nickel");
	    System.out.println(penny + " penny");

        /********* End *********/
    }
}
```


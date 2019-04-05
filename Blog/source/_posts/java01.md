---
title: JAVA 01 데이터타입
categories:
  - JAVA
tags:
  - JAVA
date: 2019-04-03 18:56:37
---

## 기본용어  
+ `선언`  
	변수의 형을 정의하는 것  
	```java
	int a; char b; double c;
	```
	
+ `할당`  
	값을 주는 것
	```java	
	a = 1;  b = 'A'; c = 12.5;
	```
	
+ `초기화`  
	선언과 동시에 값을 주는 것  
	```java
	int a = 1; char b = 'A' double c = 12.5;
	```
	
+ `나열`  
	같은 데이터 타입일때 쭉 연결하는 것  
	```java
	int a = 1, b = 2;  
	
	```
	
+ `재할당` 
	할당된 값에 다시 할당해서 값을 바꾸는 것	
	```java 
	int a = 1; → int a = 3;  
	```
	
	
## `변수`  
 + `변수`    	
	**데이터를 저장할 메모리 기억공간**  
	기억공간에는 이름이 있어야 한다. ▶ 식별자  
	데이터를 담는 상자 : 크기 ▶ Data Type(자료형)  
	
	※ `변수 이름 작성 규칙`  
	- 반드시 영문자 소문자로 시작
	- 첫글자는 영문자, '_', '$'으로만 시작
	- 예약어(KeyWord)는 사용 불가
	- 띄어쓰기는 사용할 수 없다
	- 가급적이면 이름에 의미가 나타나도록 작성하자  
				
## `자료형`
 + `자료형(Data Type)`
	**변수의 크기와 저장해야 할 데이터의 종류를 결정**  

  1. `기본자료형(PDT)`  
	: 기본 데이터 타입의 크기가 정해져있다.
	 CPU나 운영체제에 따라 변경되지 않는다. 
	
	 `정수형` : byte(1), short(2), int(4), long(8)
	 `실수형` : float(4), double(8)
	 `문자형(단일문자)` : char(2)
	 `부울형(논리형)` : boolean(1)
	 
  2. `사용자정의 자료형(UDDP)`
	: 참조형 자료(Reference Type) → 4Byte	
		
	`클래스 타입`
	`인터페이스 타입`
	`배열(열거) 타입`


## 예제 1
+ `선언`,`할당`,`초기화`  
 		
```java
public class Variable01 {
	public static void main(String[] args) {
		//정수 2개를 저장할 변수를 선언하시오.(변수명은 a.b)
		int a;	//정수형 변수a를 선언
		int b;	//정수형 변수b를 선언
		//int a,b;	//같은 자료형의 변수를 나열(comma(,)구분)
		
		//변수 a에 10, 변수 b에 20을 할당하시오.
		a = 10;	//변수 a에 값(10)을 할당(대입)
		b = 20;	//변수 b에 값(20)을 할당(대입)
		
		//정수형 변수c와 d를 선언하고, c에 30,d에 40을 할당하시오.
		int c = 30;	//선언과 동시에 값을 할당 ▶ 초기화
		int d = 40;	//선언과 동시에 값을 할당 ▶ 초기화
		// int c = 30, d = 40;	//같은 자료형의 변수를 초기화하고 나열
		
		//각각의 변수에 저장된 데이터를 출력
		System.out.println("a의 값:" + a);
		System.out.println("b의 값:" + b);
		System.out.println("c의 값:" + c);
		System.out.println("d의 값:" + d);
	}//main()
}//class

```
  

## 예제 2
+  `재할당`  

```java
public class Variable02 {
	public static void main(String[] args) {
		//정수형 변수 a와 b를 선언하고, a에 10, b에 20을 할당하시오.
		int a = 10;
		int b = 20;
		
		//변수 a와 b의 값을 출력
		System.out.println(a);
		System.out.println(b);
		
		//a의 값을 30으로 b의 값을 40으로 변경하여 출력하시오 ▶ 재할당
		a = 30; // a의 값이 10에서 30으로 변경(재할당)
		b = 40;	// b의 값이 20에서 40으로 변경(재할당)
		System.out.println(a);
		System.out.println(b);
	} //main
} //class		
```

## 예제 3
+ 정수형 `byte`,`short`,`int`,`long`  

```java  
public class Variable03 {
	public static void main(String[] args) {
		//정수형 데이터 타입 : byte, short, int, long
		byte b = 100;	//1Byte (-128 ~ 127)
		System.out.println("변수 b:" + b);
		
		short s = 1000; //2Byte (-32,768 ~ 32,767)
		System.out.println("변수 s:" + s);
		
		int i = 1000000; //4Byte (-2,147,483,648 ~ 2,147,483,647)
		System.out.println("변수 i:" + i);
		
		long l = 12345678900L; // long 타입은 숫자 뒤에 L, 
		// 모든 정수타입 리터럴은 int형으로 처리하기 때문
		System.out.println("변수 l:" + l);
	}	//main()
}	//class
```

## 예제 4
+ 실수형 `float`,`double`  

```java  
public class Variable04 {
	public static void main(String[] args) {
		//실수형 데이터 타입 : float, double
		float f = 123.4567890123456789F;	//4Byte
		double d = 123.4567890123456789; 	//8Byte
		
		System.out.println("변수 f:" + f);	
		//123.45679
		//마지막 숫자 반올림해서 나옴
		System.out.println("변수 d:" + d);	
		//123.45678901234568
		//마지막 숫자 반올림해서 나옴
	}//main()
}//class
```

## 예제 5
+ 문자형 `char` / 문자열 `String`    

```java
public class Variable05 {
	public static void main(String[] args) {
		//문자 데이터 타입 : char(2Byte) ▶ 하나의 글자만 저장
		//값을 할당할 때는 작은따옴표를 사용한다.
		char a = 'A';
		char b = '가';
		char c = '★';
		
		System.out.println("변수 a:" + a);
		System.out.println("변수 b:" + b);
		System.out.println("변수 c:" + c);
		//----------------------------------
		
		//String : 문자,문자열을 저장할 수 있는 클래스(→첫글자 대문자)
		//값을 할당할 때는 쌍따옴표를 사용한다.
		String str1 = "ABC";
		String str2 = "가나다";
		
		System.out.println("변수 str1:" +str1);
		System.out.println("변수 str2:" +str2);
	}//main()
}//class
```

## 예제 6
+ 논리형 `boolean`    

```java  
public class Variable06 {
	public static void main(String[] args) {
		// 논리형(부울형):boolean(1byte)▶true,false 만 기억
		boolean t = true;
		boolean f = false;
	
		System.out.println("변수 t:" + t);
		System.out.println("변수 f:" + f);
	}
}
```
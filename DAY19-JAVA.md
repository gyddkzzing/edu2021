# 2021.10.26 윤정아

toString() 

//해당 다형성에서 toString이 자식의 toString이 호출되게 되어있다. 안 적어주게 되면 부모에 있는 toString이 나온다.

상속, 다형성, public, static

어떨 때 상속을 하는지?

class 앞 final은 무엇일까? -> 다른 클래스한테 상속할 수 없음.

함수 앞에 final은 무엇일까? -> 자식한테 오버라이딩 할 수 없음.

@override (어노테이션)

#### 인터페이스 

인터페이스 안에는 두가지가 올 수 있는데

1) final 상수 //변수는 잘 쓰이지가 않는다. 

2) abstract가 붙게되면 함수 선언만 가능  == 바디는 없다. == 바디 실제 구현 부분이 없음.

//public abstract는 생략이 가능하고 없으면 컴파일러가 붙여줌. 

//public abstract void print (String doc); -> 생략 후  void print (String doc);

//abstract == 는 자손이 구현해라 



인터페이스 활용 => 약속, 규약, 강제 => 표준



### 학습정리

1. Object 클래스란? 
   - 모든 클래스의 가장 최상위 클래스
   - 모든 클래스는 object클래스를 부모  클래스로 상속 받는다.


2. 아래의 소스코드에 대하여 아래와 같이 출력되는 이유는?
  출력 : A@28a418fc

  

  class A{
  }

public class Test {
	public static void main(String[] args) {
		A a = new A();
		System.out.println(a); // String s = String.valueOf(x); -> s가 주소 뿌림
	}
}

- class A안에 값이 있으면 toString()메소드가 경로값을 리턴해주는건데 값이 없기도 없고 그래서 그냥 주소값만 반환된다. 

3. class이름 및 함수에서 final의 의미는?
   - class이름 앞 final은 무엇일까? -> 다른 클래스한테 상속할 수 없음.
   - 함수 앞에 final은 무엇일까? -> 자식한테 오버라이딩 할 수 없음.

4. 아래의 Main 돌아가도록 프로그래밍 하시오.

interface Printable { // MS가 정의하고 제공한 인터페이스
	public void print(String doc);
}

	//SPrinterDriver 와 LPrinterDriver를 만드시오
	public static void main(String[] args) {
		String myDoc = "This is a report about...";
	
		// 삼성 프린터로 출력
		Printable prn = new SPrinterDriver();
		prn.print(myDoc);
		System.out.println();
	
		// LG 프린터로 출력
		prn = new LPrinterDriver();
		prn.print(myDoc);
	}

/*
출력: 
From Samsung printer
This is a report about ...
From LG printer
This is a report about ...
*/



--------------------------------------------------------------------------------



package ac.kr;
//import Printable;

interface Printable {
	public void print (String doc);
}

class SPrinterDriver implements Printable {
	@Override //삼성프린트로 출력
	public void print(String doc) {
		System.out.println("From Samsung printer");
		System.out.println(doc);
	}
}

class LPrinterDriver implements Printable {
	@Override //LG프린터로 출력
	public void print(String doc) {
		System.out.println("From LG printer");
		System.out.println(doc);
	}
}


public class LgSamsungPrinter {
	public static void main(String[] args) {
		
		String myDoc = "This is a report about...";
	    
	    // 삼성 프린터로 출력
	    Printable prn = new SPrinterDriver();
	    prn.print(myDoc);
	    System.out.println();
	
	    // LG 프린터로 출력
	    prn = new LPrinterDriver();
	    prn.print(myDoc);


​		

	}

}




5. @Override 에 대하여 설명하시오.

   - 하나의 어노테이션으로 만약 우리가 철자나 대소문자를 틀렸을 경우 실수를 방지하기 위해 지정해줄 수 있는 것이다.  

6. interface 에 대하여 설명해 보시오.

  - 약속, 규제, 강제, 표준  

7. interface 안에 올 수 있는 두 가지는 무엇인가? 

  - final
  - abstract

8. abstract 키워드란?

  - 추상메소드와 추상클래스를 말한다.

9. 아래의 결과가 나오도록 프로그래밍 하시오.
  Object obj = new Circle(10);
  System.out.println(obj);

  ​	//출력: 넓이는 314.134 입니다. (예시)



package ac.kr;

class Circle {
	private int r;
	Circle (int r){
		this.r =r; //반지름
	}
	public double getArea() {
		return r*r*Math.PI;
	}
	

	public String toString() {
		return "넓이는 "+getArea()+"입니다.";
	}
}

public class ClassCircleTest {

	public static void main(String[] args) {
		
		Object obj = new Circle(10);
		System.out.println(obj);
	
	}

}





10. 아래의 프로그래밍을 하시오.

아래의 인터페이스에 맞추어(상속하여) 아래를 프로그래밍 하시오.

Circle, Rectangle , Triangle

interface AreaGetable{
double getArea();
}


main(){

AreaGetable area = new Circle(4);
sysout(area.getArea())

area = new Rectangle(4,5);
sysout(area.getArea())

area = new Triangle(4,5);
sysout(area.getArea())
}





interface AreaGetable {
	public double getArea();
}

class Circle implements AreaGetable {

	private int r;
	
	public Circle(int r) {
		this.r = r;
	
	}
	
	@Override
	public double getArea() {
		return r * r * Math.PI;
	}

}

class Rectangle implements AreaGetable {

	private int height;
	private int width;
	
	public Rectangle(int width, int height) {
		this.width = width;
		this.height = height;
	}
	
	@Override
	public double getArea() {
	
		return width * height;
	}

}

class Triangle implements AreaGetable {
	private int height;
	private int width;

	public Triangle(int width, int height) {
		this.width = width;
		this.height = height;
	}
	
	@Override
	public double getArea() {
		return (width * height)/2;
	}

}

public class CircleAreaInter {

	public static void main(String[] args) {
	
		AreaGetable area = new Circle(4);
		System.out.println(area.getArea());
	
		AreaGetable area1 = new Rectangle(4, 5);
		System.out.println(area1.getArea());
	
		AreaGetable area11 = new Triangle(4, 5);
		System.out.println(area11.getArea());
	
	}

}
# 2021.10.14 윤정아

경로를 고정 시켜주지 않으면 java -version 했을 때 에러 발생 
=> 

패키지의 이해
패키지 하나도 하나의 폴더로 이해한다. 

import를 쓰는 이유 => 그냥 깔끔하게 보이기 위해

OPP(객체지향 언어: Java) <-> 절차지향 언어 : C언어

OPP의 특징
1. 상속
2. 정보은닉
3. 다형성 (자바의 80% 지분)
4. 캡슐화 -소프트웨어의 최종 목적
(최종 목적자가 최대한 사용하기 편하도록 ..)



class Money {
	private  int m_500, m_100, m_50, m_10, m_5, m_1, money, tmp;

	Money(int money) {	
	
		setMoney(money);
	}
	
	public void setMoney(int money) {
		
		if(money < 0) {
			this.money = 0;
			System.out.println("잘못된 입력입니다.");
			return;
		}
		
		this.money = money;
		
	}
	
	public void show() {
	
		m_500 = money / 50000;
		tmp = money - m_500 * 50000;
	
		m_100 = tmp / 10000;
		tmp = tmp - m_100 * 10000;
	
		m_50 = tmp / 5000;
		tmp = tmp - m_50 * 5000;
	
		m_10 = tmp / 1000;
		tmp = tmp - m_10 * 1000;
	
		m_5 = tmp / 500;
		tmp = tmp - m_5 * 500;
	
		m_1 = tmp / 100;
		System.out.println("오만원 : " + m_500 + "장");
		System.out.println("만원 : " + m_100 + "장");
		System.out.println("오천원 : " + m_50 + "장");
		System.out.println("천원 : " + m_10 + "장");
		System.out.println("오백원 : " + m_5 + "개");
		System.out.println("백원 : " + m_1 + "개");
	
	}

}

### 학습정리 

1. set classpath 에 대하여 설명하시오.

  - .classpath가 어디에 있는지 알려주는 것. 

2. 절대 경로와, 상대 경로란?

  - 절대 경로 : 루트 디렉토리를 시작으로 지정
  - 상대 경로 : 기준 자체가 '나

3. cd  . 관 cd .. 의 차이는?

   cd. 내 자신 => 현재 디렉토리로 이동 

   cd.. 뒤로 가기  => 상위 디렉토리로 이동

4. package 에 대하여 설명해 보시오.

   - 하나의 폴더라고 생각하면 된다. 

5. 정보은닉에 대하여 설명하여 보시오.

   클래스 내부에서 사용할 변수나 메소드를 private로 선언해서 외부에서 접근하지 못하도록 하는 것.

6. 접근제한자에 대하여 설명하시오.

   - public, private, defalt 등이 있다.
   - public 은 다른 패키지에서도 가능
   - private 자기 클래스 내
   - defalt 동일 패키지 내 

7. 지역변수에 접근 제한자가 필요없는 이유는?

- 지역 변수의 특성상 메소드 내에서 선언되고 값이 초기화가 되기 때문에 해당 범위내에서만 메모리가 움직이는 특성을 가진다. 여기서 접근제한자를 통해 해당 정보를 은닉하면 값을 참조할 수 없기에 이를 따로 붙히지 않는다. 

8. 아래의 클래스를 구현하시오. 

Money money = new Money(-126000);
money.show();

출력 
잘못된 입력입니다.
오만원 0장....
오만원 0장....
등등등....



class Money {
	private  int m_500, m_100, m_50, m_10, m_5, m_1, money, tmp;

	Money(int money) {	
	
		setMoney(money);
	}
	
	public void setMoney(int money) {
		
		if(money < 0) {
			this.money = 0;
			System.out.println("잘못된 입력입니다.");
			return;
		}
		
		this.money = money;
		
	}
	
	public void show() {
	
		m_500 = money / 50000;
		tmp = money - m_500 * 50000;
	
		m_100 = tmp / 10000;
		tmp = tmp - m_100 * 10000;
	
		m_50 = tmp / 5000;
		tmp = tmp - m_50 * 5000;
	
		m_10 = tmp / 1000;
		tmp = tmp - m_10 * 1000;
	
		m_5 = tmp / 500;
		tmp = tmp - m_5 * 500;
	
		m_1 = tmp / 100;
		System.out.println("오만원 : " + m_500 + "장");
		System.out.println("만원 : " + m_100 + "장");
		System.out.println("오천원 : " + m_50 + "장");
		System.out.println("천원 : " + m_10 + "장");
		System.out.println("오백원 : " + m_5 + "개");
		System.out.println("백원 : " + m_1 + "개");
	
	}

}



9. 아래의 클래스를 구현하시오.
   Employee employee = new Employee("홍길동", 19, "서울 뉴욕시", "개발 1팀");
   employee.printInfo();
   }

출력:
이름 : 홍길동
나이 : 19
주소 : 서울 뉴욕시
부서 : 개발 1팀

class Employee{
	private String name;
	private int age;
	private String home;
	private String em;
	
	Employee(String name,int age,String home,String em){
		
		this.name=name;
		this.age=age;
		this.home=home;
		this.em=em;
		
	}
	
	public void printInfo() {
		System.out.println("출력:");
		System.out.println("이름 : "+name);
		System.out.println("나이 : "+age);
		System.out.println("주소 : "+home);
		System.out.println("부서 : "+em);
		
	}
}



10. 다음 멤버를 가지고 직사각형을 표현하는 Rectangle 클래스를 작성하라. 
    - int 타입의 x, y, width, height 필드: 사각형을 구성하는 점과 크기 정보
    - x, y, width, height 값을 매개변수로 받아 필드를 초기화하는 생성자
    - int square() : 사각형 넓이 리턴
    - void show(): 사각형의 좌표와 넓이를 화면에 출력
    - boolean contains(Rectangle r): 매개변수로 받은 r이 현 사각형 안에 있으면 true 리턴 (겹치면 안됨, 완전히 안에 있어야 true
    - main() 메소드의 코드와 실행 결과는 다음과 같다. 



public static void main(String[] args) {

​		Rectangle r =new Rectangle(2,2,8,7);
​		Rectangle s =new Rectangle(5,5,6,6);
​		Rectangle t =new Rectangle(1,1,10,10);
​		r.show();
​		System.out.println("의 면적은 "+s.square());
​			if(t.contains(r)) 
​				System.out.println("t는 r을 포함합니다.");
​			if(t.contains(s)) 
​				System.out.println("t는 s을 포함합니다.");

}





/////출력 :

​	(2,2)에서 크기가 8x7인 사각형

 	s의 면적은 36

​	t는 r을 포함합니다.
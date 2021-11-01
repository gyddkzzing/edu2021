# 2021.11.01 윤정아

1. Wrapper class란?
   - 기본 자료타입을 객체로 다루기 위해 사용하는 클래스들을 래퍼 클래스라고 한다. 

2. auto unboxing 이란?

   <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211101165926243.png" alt="image-20211101165926243" style="zoom:80%;" />

   - 래퍼 클래스에서 -> 기본 타입의 값을 얻어내는 과정

3.BigInteger 클래스에 대하여 설명하시오. 

- 범위는 무한대 불변한 정수 , 무한대의 숫자 표시가 가능함. 

--------------------------------------------------



- 클래스 Person은 이름을 저장하는 필드 구성
- 클래스 Person은 상위 클래스 Object의 메소드 equals()를 오버라이딩하여 이름이 같으면 true를 반환하는 메소드 구현
- 다음과 같은 소스로 클래스 Person을 점검

Person p1 = new Person("홍길동");
System.out.println(p1.equals(new Person("홍길동")));
System.out.println(p1.equals(new Person("최명태")));

결과 
true
flase



--------

package Person;

class Person {
	private String name;

	Person(String name) {
		this.name = name;
	}
	
	public boolean equals(Person p) {
		if (this.name.equals(p.name)) {
			return true;
		} else {
			return false;
		}
	}
}

public class EqualsMain {

	public static void main(String[] args) {
	
		Person p1 = new Person("홍길동");
		System.out.println(p1.equals(new Person("홍길동")));
		System.out.println(p1.equals(new Person("최명태")));
	
	}

}

---------





 4. 다음 조건을 만족하는 클래스 String의 객체 이용 프로그램을 작성하여 
메소드 equals()와 연산자 == 의 차이를 비교 설명하시오.

-  equals()와 연산자 == 의 차이는 equals()는 안에 내용을 비교하고 ==는 주소값을 비교함.

String s1 = new String("java");
String s2 = new String("java");
String s3 = s2;

System.out.println(s1 == s2);
System.out.println(s1.equals(s2));
System.out.println(s2 == s3);
System.out.println(s2.equals(s3));



-------

false
true
true
true

--------



5. 아래를 정리하시오.

1) 프로토콜 : 컴퓨터 내부 또는 사이에서 데이터의 교환 방식을 정의하는 규칙 체계, 규칙의 집합.
2) DNS (Domain Name System) : 도메인 이름(예: www.amazon.com)을 머신이 읽을 수 있는 IP주소(예: 192.0.2.44)로 변환하는 것
3) 포트 번호 : 프로그램의 주소
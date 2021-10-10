# 2021.10.06 윤정아

#### 증감 연산

- ++n  전위 연산
- --n    전위 연산
- n++  후위 연산
- n--   후위 연산

public static void main(String[] args) {
		//전위 연산자
		int num =2; //num =num+1을 먼저 연산 후 출력
		System.out.println(++num);
		
		//후위 연산자
		int num1=2; //출력 후 num =num+1 연산
		System.out.println(num1++);
		System.out.println(num1);
	}
출력 결과

3

2

3

public static void main(String[] args) {
		int num =5; 
		System.out.print((num++)+" ");
		System.out.print((num++)+" ");
		System.out.println(num);
		
		System.out.print((num--)+" ");
		System.out.print((num--)+" ");
		System.out.println(num);
	}
출력 결과

5 6 7

7 6 5



#### 비트 연산

=> 2진수의 연산을 비트 연산이라고 표현한다.



True ->1

False ->0

& 비트 단위로 and연산 -> 둘 중 하나라도 0이면 0 // 1 1->1 //1 0 -> 0 // 0 0 -> 0

| 비트 단위로 or연산 ->  둘 중 하나라도 1이면 1 // 0 0 -> 0 // 1 1-> 1 //1 0-> 1

^ 비트 단위로 xor연산 -> 두 비트가 다르면 1 두 비트가 같으면 0 //1 1 -> 0 // 1 0 ->1 // 0 0 ->0

~ 모든 비트 반전 

//>> 쉬프트 연산 

//<<





#### if문 

public static void main(String[] args) {

		int kor = 50;
		int eng = 60;
		int math = 90;
		int total = kor + eng + math;
		
		double avg = (double) total / 3;
	
		if (avg >= 90) {
			System.out.println("평균 90점 이상이므로 수!");
		} else if (avg>=80) {
			System.out.println("아쉽네요 ㅜㅜ 우우~~");
		} else if (avg>=70) {
			System.out.println("미미미미미미자로 끝나는 말은");
		} else
			System.out.println("가가가ㅏ라라ㅏ 집으로 가가");
	
	}
국 영 수 점수 입력 후 if문 사용하기 

**import java.util.Scanner; **

public class IEEEE {

	public static void main(String[] args) {
	
		Scanner sc = new Scanner(System.in);
		int kor = 0, eng = 0, math = 0;
		System.out.print("국어 점수를 입력하세요 :");
		kor = sc.nextInt();
		System.out.print("영어 점수를 입력하세요 :");
		eng = sc.nextInt();
		System.out.print("수학 점수를 입력하세요 :");
		math = sc.nextInt();
	
		int total = kor + eng + math;
		double avg = (double) total / 3;
	
		System.out.println("너의 평균은 " + avg + "란다.");
		if (avg >= 90) {
			System.out.println("평균 90점 이상이므로 수!");
		} else if (avg >= 80) {
			System.out.println("아쉽네요 ㅜㅜ 우우~~");
		} else if (avg >= 70) {
			System.out.println("미미미미미미자로 끝나는 말은");
		} else
			System.out.println("가가가ㅏ라라ㅏ 집으로 가가");
	
	}

}





#### 삼항 연산자 (실무에서 사용하는 단어)



public class Boolean {

	public static void main(String[] args) {
	
		int num1;
		int num2 = 100;
		int num3 = 10;
	
		num1 = (num2 < num3) ? num2 : num3;
		
		System.out.println(num1);
	}
}





#### switch와 break

public class Boolean {

	public static void main(String[] args) {
		
		int n=3; //정수가 들어가야하니까 int로 선언 
		switch (n) { //()안에는 정수만 들어감 1...5..29...
		case 1: //각각의 case는 else if에 해당함.
			System.out.println("Simple Java");
		case 2:
			System.out.println("Funny Java");
		case 3:
			System.out.println("Fantastic Java");
		default:
			System.out.println("자바는 참 좋은 언어구나 에헴");
				//if문 else에 해당된다고 볼 수 있음.
		}	
		System.out.println("자바 좋아함?");
		}
}

중간에 break;문이 없으면 끝까지 돌리고 중간에 berak; 문이 들어가면 switch문을 빠져나가고 거기서 멈춘다. 




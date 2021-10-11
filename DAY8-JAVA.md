# 2021.10.11 윤정아

#### 메소드 



* 함수에는 정의와 호출이 있다
* 함수를 만드는 것 => 정의
* 함수를 써먹는 것 => 호출

public class One {

	public static void main(String[] args) {
	
	double myHeight = 180;
		
	System.out.println("프로그램 시작");	
	hiEveryone(10, 120);
	
	hiEveryone(20, myHeight );
	byEveryone();
	}
	
	public static void hiEveryone(int age, double height) { //함수 만들 때는 변수 선언이 옴. //int age를 파라미터라고 함. 
		System.out.println("제 나이는"+age+"세 입니다.");
		System.out.println("저의 키는" +height+"cm 입니다.");
	}
	
	public static void byEveryone() {
		System.out.println("다음에 뵙겠슴둥");
	}

}



public static void main(String[] args) {
	
	int result;
	result =adder(4,5);
	System.out.println("4+5="+result);
	System.out.println("3.5 X 3.5=" +square(3.5));
}

	private static double square(double num) {
		return num *num; 
	}
	
	private static int adder(int num1, int num2) {
		int addResult =num1+num2;
		return addResult;
	}






int add(int num1, int num2){

​	return num1+num2;

}



리턴타입 함수명(파라미터...){

//실행내용

}







//파라미터에 넣은 값만큼 별 그리기 

public class One {

	public static void main(String[] args) {
	
		int num = add(3, 7);
		System.out.println("두개의 합은: " + num);
	
		num = sub(3, 7);
		System.out.println("두개의 뺄셈은: " + num);
	
		num = mul(6, 7);
		System.out.println("두개의 곱은: " + num);
	
		num = div(6, 0);
		System.out.println("두개의 나눗셈은: " + num);
	
		starPrint(5);
		System.out.println("");
		starPrint(6);
	}
	
	private static void starPrint(int num1) {
		for (int i = 0; i < num1; i++) {
			for (int j = 0; j <= i ; j++) {
					System.out.print("*"); 
			}
			System.out.println();
		}
	}
	
	private static int div(int num1, int num2) {
		int result;
	
		if (num2 == 0) {
			result = 0;
			System.out.println("0이 입력되었네요. 잘못입력하셨답니당");
		} else {
			result = num1 / num2;
		}
		return result;
	}
	
	private static int mul(int num1, int num2) {
		int mul = num1 * num2;
		return mul;
	}
	
	private static int sub(int num1, int num2) {
		int sub = num1 - num2;
		return sub;
	}
	
	private static int add(int num1, int num2) {
	
		return num1 + num2;
	}
}





**public static void main()** => void : 값을 반환하지 않음을 의미

**public static int adder()** => return값의 반환을 명령







public class One {

	public static void main(String[] args) {
	
		int num = add(3, 7);
		System.out.println("두개의 합은: " + num);
	
		num = sub(3, 7);
		System.out.println("두개의 뺄셈은: " + num);
	
		num = mul(6, 7);
		System.out.println("두개의 곱은: " + num);
	
		num = div(6, 0);
		System.out.println("두개의 나눗셈은: " + num);
	
		starPrint(5);
		System.out.println("");
		starPrint(6);
		
		double area=getCircleArea(10);
		System.out.println(area);
		
		double width=100;
		double height =100;
		
		area=getRectArea(width, height);
				System.out.println(area);
	}
	
	public static double getRectArea(double width, double height) { //사각형 넓이
		double area= height*width;
		return area;
	}
	
	public static double getCircleArea(double r) { //원 넓이
		final double PI=3.14;
		double area = r*r*PI;
		
		return area;
	}
	
	public static void starPrint(int num1) { //return 값이 필요없으므로 void 사용
		for (int i = 0; i < num1; i++) {
			for (int j = 0; j <= i ; j++) {
					System.out.print("*"); 
			}
			System.out.println();
		}
	}
	
	public static int div(int num1, int num2) {
		int result;
	
		if (num2 == 0) {
			result = 0;
			System.out.println("0이 입력되었네요. 잘못입력하셨답니당");
		} else {
			result = num1 / num2;
		}
		return result;
	}
	
	public static int mul(int num1, int num2) {
		int mul = num1 * num2;
		return mul;
	}
	
	private static int sub(int num1, int num2) {
		int sub = num1 - num2;
		return sub;
	}
	
	private static int add(int num1, int num2) {
	
		return num1 + num2;
	}
}





public class One {

	public static void main(String[] args) {
	
		char grade;
		double avg =80;
		grade =getGrade(95);
		//우 입니다.
		
		System.out.println(grade +"입니다.");
	}
	
	public static char getGrade(double avg) {
		
		char grade ='가';
		if(avg>=90) {
			grade ='수';
		}
		else if(avg>=80) {
			grade='우';
		}
		else {
			grade ='미';
		}
		return grade;
	}
}



public class One {

	public static void main(String[] args) {
	
		char grade;
		double avg =80;
		grade =getGrade(95);
		//우 입니다.
	
		System.out.println(grade +"입니다.");
		
		int sum =getHap(1,100); //5050
		System.out.println(sum);
	}
	
	public static int getHap(int num1, int num2) {
	
		int sum = 0;  
		
			for(int i = num1; i<=num2; i++ ) {
				sum+=i;
			}
		return sum;
	}
	
	public static char getGrade(double avg) {
		
		char grade ='가';
		if(avg>=90) {
			grade ='수';
		}
		else if(avg>=80) {
			grade='우';
		}
		else {
			grade ='미';
		}
		return grade;
	}
}



### 학습 정리

1. 함수는 어떻게 알아볼 수 있는가?

   ()를 통해 알아본다. 

   

2. 함수 호출 하는 법은?

   정의한 함수를 main함수에 호출한다. 

   ex) hiEveryone();

   

3. 함수 만드는 법은?

   public static void mai()

   public static int adder(int i , int j)

   void가 오면 return값은 존재하지 않게 만들어준다. 

   return값이 있으면 형을 정하고 return값을 정해줌.

   

4. 리턴 타입 void는 어떠한 경우에 쓰는가?

   return 값이 존재하지 않을 때 사용함.

   

5. 아래를 함수로 만드시오.

   

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211011165209056.png" alt="image-20211011165209056" style="zoom:80%;" />

public class One2 {

	public static void main(String[] args) {
	
		starPrint2(5);
	}
	
	public static void starPrint2(int num) {
	
		for (int i = 1; i <= num; i++) {
			for (int j = 0; i <= j; j++) {
				System.out.print(" ");
			}
			for(int j=num; j>=i; j--) {
				System.out.print("*");
			}
			System.out.println();
		}
	}
}

6. 아래를 함수로 만드시오.

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211011170242969.png" alt="image-20211011170242969" style="zoom:80%;" />

public class One2 {

	public static void main(String[] args) {
	
		starPrint3(5);
	}
	
	public static void starPrint3(int num) {
	
		for(int i=0; i<num; i++){ 
	        for(int j=0; j<num-i; j++){ //공백 
	            System.out.print(" ");
	        }
	        for(int j=0; j<2*i+1; j++) { //별출력 
	            System.out.print("*");
	        }
	        System.out.println();
	    }
	}
}



7. 아래의 함수를 만드시오.

char grade;

double avg =80;

grade=getGrade(avg);

//우 입니다.

System.out.println(grade+"입니다.");



public class One2 {

	public static void main(String[] args) {
	
		char grade;
		double avg=80;
		grade=getGrade(avg);
		//우입니다.
		System.out.println(grade+"입니다.");
	}
	
	public static char getGrade(double avg) {
		
		char grade='우';
		if(avg>=90) {
			grade ='수';
		}
		else if (avg>80) {
			grade='우';
		}
		else if(avg>70) {
			grade='미';
		}
		else
			grade='양';
		return grade;
	}
}

8. 아래의 함수를 만드시오.

int sum =getHap(1,100);

//5050

System.out.println(sum);

public class One2 {

	public static void main(String[] args) {
	
		int sum =getHap(1,100);
		System.out.println(sum);
		//5050;
	}
	
	public static int getHap(int num1, int num2) {
		int sum=0;
		for(int i=num1; i<=num2; i++) {
			sum+=i;
		}
		return sum;
	}
}

9. 아래의 함수를 만드시오.

   int count = get57(1,100);
   //count 는 1부터 100 까지의 숫자 중 5의 배수 이자 7의 배수인 수의 갯수
   System.out.println(count );



public class One2 {

	public static void main(String[] args) {
	
		int count =get57(1,100);
		//count는 1부터 100까지의 숫자 중 5의 배수이자 7의 배수인 수의 갯수.
		System.out.println(count);
	}
	
	public static int get57(int num1, int num2) {
		
		int count =0; 
		for(int i=num1; i<=num2; i++) {
			if((i%5==0)&&(i%7==0)) {
				count++;
			}
		}return count;
	}	
}



10. 아래의 함수를 만드시오

printGuGudan(3)// 3단 출력
printGuGudan(4)// 4단 출력

public class One2 {

	public static void main(String[] args) {
	
		printGuGudan(3);
		System.out.println();
		printGuGudan(4);
	}
	
	public static void printGuGudan(int dan) {
		
		for(int i = 1; i<=9; i++) {
			System.out.print(dan+"X"+i+"="+dan*i+"\n");
		}
	}	
}





11. 아래의 함수를 만드시오.

    getRecArea(3,5) //삼각형 넓이
    getRecCirlce(5) //원넓이
    getTriangleArea(4 , 5) //삼각형 넓이

public class One2 {

	public static void main(String[] args) {
		
		int result;
		double result2;
		double result1;
		result= getRecArea(3,5); //사각형넓이
		System.out.println("사각형 넓이는:"+result);
		result1= getRecCircle(5); //원넓이
		System.out.println("원 넓이는:"+result1);
		result2= getTriangleArea(4,5);//삼각형 넓이
		System.out.println("삼각형 넓이는:"+result2);
		
	}
	
	public static int getRecArea(int w, int h) {
	
		return w*h;
	}
	
	public static double getRecCircle(int r) {
	
		final double PI=3.14;
		double circle = PI*r*r;
		return circle;
	}
	
	public static double getTriangleArea(int d, int h) {
		
		return (d*h)/2.0;
		
	}


}

12. 함수로 만들면 좋은 점은?

- 같은 작업을 (중복)하지 않기 위해
- 기능이 2번 이상 중복되면 반드시 함수로 만들 것.

13. 아래의 함수를 만드시오.

int month =4;

getSeason(3) //봄입니다 출력

printGuGudan(12) //겨울입니다 출력



public class One2 {

	public static void main(String[] args) {
		
		int month =4;
		getSeason(3);//봄입니다 출력
		getSeason(12); //겨울 출력
		
	}
	
	public static void getSeason(int month) { 
		switch (month) {
		case 1,2,3,4:
			System.out.println("봄입니다.");
			break;
		case 5,6,7,8:
			System.out.println("여름입니다.");
			break;
		case 9,10,11,12:
			System.out.println("겨울입니다.");
			break;
		default:
			System.out.println("입력이 바르지 않소이다.");
			break;
		}
	}
}
# 2021.10.12 윤정아

#### 32비트 시스템의 메모리양은 8기가 =  더 달아도 쓸모가 없음. 

**Why?** 메모리 주소 때문.



#### 형 변환 #####

##### 1. 리터럴에 대한 이해 #####

- 리터럴 - 자료형을 기반으로 표현이 되는 상수를 의미. 
- 소수점이 있는 실수형은 d를 적지 않아도 알아서defalt값을 double형으로 올린다.
- 실수형 상수의 e표기법
  - e => 10

- 이스케이프 시퀀스 (escape sequences)

![image-20211005115147750](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005115147750.png)

자료형 변환의 의미와 필요한 이유는?

- 두 피연산자의 자료형이 일치해야 동일한 방법을 적용하여 연산을 진행할 수 있다. 
- 피연산자의 자료형이 일치하지 않을 때 형의 변환을 통해 일치시켜야 한다.



#### 자동 형 변환 

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005123157983.png" alt="image-20211005123157983" style="zoom:50%;" />



#### 명시적 형 변환 (=강제적 형 변환)

**int를 short에는 집어넣지 못 한다. **

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005130350516.png" alt="image-20211005130350516" style="zoom:50%;" />

**총합과 평균 구하기 EX** 

public class Pr4 {

	public static void main(String[] args) {
		
		int Korea=52;
		int English=73;
		int math=98;             
		int total=Korea+English+math;
		double average = (double)total/3;
		//== double average = total/3.0;
		System.out.println("과목의 총점은 "+total+"\n평균은 "+average);
		
	}

}



**연산자의 우선 순위**

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005195406793.png" alt="image-20211005195406793" style="zoom:100%;" />



### 10/5 정리 문제 

1. 리터럴이란? 

   - 자료형을 기반으로 표현이 되는 상수를 의미.

2. System.out.println(3147483647+3147483648); 

   =====>ERROR발생 

   System.out.println(3147483647L + 3147483648L); 

   long형 상수임을 표기  

    

3. 자동 형 변환과 명시적 형 변환에 대하여 설명하시오. 

   - 자동 형 변환 : 자료형의 크기가 큰 방향으로 형 변환이 일어난다. 

     ​						자료형의 크기에 상관없이 정수 자료형보다 실수 자료형을 우선.

   - 명시적 형 변환 : 형 변환이 필요한 상황일 때 강제적으로 형 변환을 진행한다.

     ​					EX) int result = num1 / (double) num2;

4. 프로그래밍 문제

''' 수정 전 결과 값 0.0

public class ArithOp {

	public static void main(String[] args) {
	
		int a=3;
		int b=4;
		
		double result =a/b;
		
		System.out.println(result);
		
	}

}

-----> 수정 후 결과 값 0.75

public class ArithOp {

	public static void main(String[] args) {
	
		int a=3;
		int b=4;
		
		double result = (double)a/b;
		
		System.out.println(result);
		
	}

}

5. 이스케이프 시퀀스 종류를 나열하고 기능을 설명하시오. //위에 프로그래밍 해둠. 

   ![image-20211005200852540](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005200852540.png)

6. 아래의 출력 결과를 확인하고, 130이 나오는 이유를 설명하시오.

7. 결합 방향, 우선순위에 대해 설명하시오.

   - 우선순위는 연산자의 우선순위로 정하며, 결합 방향은 = 를 제외하고, 왼쪽에서 오른쪽

8. 프로그래밍 문제 +9. 프로그래밍 문제 => 논리연산자 예제 

   - 1초과 100미만 나타내기

   - 2의 배수 또는 3의 배수 나타내기 

     

     public class Pr5 {

     	public static void main(String[] args) {
     		
     		int num1=11;
     		int num2=22;
     		boolean result;
     		
     		//변수 num1에 저장된 값이 1과 100사이의 수인가?
     		result =(1<num1) && (num1<100); //둘 다 참이면 참 and
     		System.out.println("1 초과 100 미만인가? "+ result);
     		
     		//변수 num2에 저장된 값이 2 또는 3의 배수인가?
     		result =((num2%2)==0||(num2%3)==0); //둘 중 하나만 참이면 참 or
     		System.out.println("2또는 3의 배수인가? "+result);


     ​		
     	}

     }

     

10. 아래의 프린트 결과를 예측해보고, 코딩 후 결과를 나타내시오.

public class Pr {

	public static void main(String[] args) {
		int num1=0;
		int num2=0;
		boolean result;
		
		result =((num1+=10)<0)&&((num2 +=10)>0); //and연산
		System.out.println("result= "+ result );
		System.out.println("num1= "+num1);
		System.out.println("num2= "+num2); //false일때는 적용안되나봄?
		
		result =((num1+=10)>0)||((num2 +=10)>0);//or연산
		System.out.println("result= "+result);
		System.out.println("num1= "+num1);
		System.out.println("num2= "+num2);
	}

}

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005204829477.png" alt="image-20211005204829477" style="zoom:50%;" />



11. 프로그래밍 문제

- 국어: 50점, 영어: 70점, 수학: 95점 의 총점(total)과 평균(avr)값을 구하라. 

  (단, 평균은 소수점까지 나타내시오.)

public class Pr4 {

	public static void main(String[] args) {
		
		int Korea=50;
		int English=70;
		int math=95;             
		int total=Korea+English+math;
		double average = (double)total/3;
		//== double average = total/3.0;
		System.out.println("과목의 총점은 "+total+"\n평균은 "+average);
		
	}

}

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211005203730761.png" alt="image-20211005203730761" style="zoom:50%;" />
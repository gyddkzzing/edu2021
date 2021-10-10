# 2020.09.01 윤정아

'''

//세수중 가장 큰수 구하기
    	
    	int a = 80;
    	int b = 90;
    	int c = 100;
    	
    	int max;
    	//1.첫번째 방법 
    	if(a > b) {
    		
    		if( a > c) {
    			max = a;
    		}else {
    			max = c;
    		}
    		
    	}else {
    		if( b > c) {
    			max = b;
    		}else {
    			max = c;
    		}    		
    	}
    	
    	System.out.println(max);
    	
    	//2번째 방법
    	if( (a > b) && (a > c)) {
    		max = a;
    	}else if((b > a) && (b > c)) {
    		max = b;
    	}else {
    		max =c;
    	}
    	
    	System.out.println(max);
    	
    	//3.좀더 코딩을 줄이기
    	max = a;
    	
    	if(b > max) {
    		max = b;
    	}
    	
    	if(c > max) {
    		max = c;
    	}
    	
    	System.out.println(max);
    	
    	max = (a > b) ? (a > c ? a : c) : (b > c ? b : c);



//4번

max=(a>b)?(a>c?a:c):(b>c?b:c);

System.out.println(max);

'





달(1,2,3--월을 담는)변수 선언



1,2,3,4 봄입니다 출력

5,6,7,8 여름입니다 출력

9, 10 ,11, 12 겨울 출력

import java.util.Scanner;

public class Weather {

	public static void main(String[] args) {
		
		int num =0;
		Scanner sc = new Scanner(System.in);
		System.out.print("조회를 원하는 숫자를 입력해주세요..." );
		num =sc.nextInt();
		switch (num) {
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
			System.out.println("그는 시공간을 넘나드는군요 부러워요.");
			break;
		}
	
	}
}

#### while문과 do while 

**while문과 do while문의 차이점은 무엇인가?**

- while은 조건문에 해당하지 않으면 실행하지 않을 수 있으나 do-while문은 무조건 한번은 실행한다. 



#### for문 

구구단

public static void main(String[] args) {
		
		int dan=5;
		
		for (int i=1; i<=9; i++) {
			//System.out.println(i+" * 9 = "+i*9);
			System.out.println(i+"*"+dan+"="+(i*dan));
		}
	}
1~100까지 수를 더하라

	public static void main(String[] args) {
	
		int result = 0;
		for (int i = 1; i <= 100; i++) {
			result = result + i;
	
			System.out.printf("%d\n", result);
		}
	
	}
public class ForEx {

	public static void main(String[] args) {
	
		int result = 0;
		for (int i = 1; i <= 1000; i++) {
			if(i%2==0 && i%3==0) {
			result = result + i;
			//System.out.println(i+":"+ result);
			}
		}
		System.out.println(result);
	}

}



#### break와 continue 

break:

continue:



public class ContinueEx {

	public static void main(String[] args) {
	
		int num = 0;
		int count = 0;
	
		while ((num++) < 100) {
			
			if (((num % 5) != 0) || ((num % 7) != 0))
				continue;
			
			count++;
			System.out.println(num);
		}
		System.out.println("count: " + count);
	}
}

#### 이중 for문

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 2; i < 10; i++) {
			for (int j = 1; j < 10; j++)
				System.out.println(i + "x" + j + "=" + (i * j));
		}
	
	}

}

//짝수 구구단 출력

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 2; i < 10; i++) {
			if(i%2==0)
			for (int j = 1; j < 10; j++)
				System.out.println(i + "x" + j + "=" + (i * j));
		}
	
	}

}

//결과값이 홀수 인 것만 출력

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 2; i < 10; i++) {
			for (int j = 1; j < 10; j++) {
				int result = i * j;
				if (result % 2 == 0) {
					System.out.println(i + "x" + j + "=" + (i * j));
				}
			}
	
		}
	
	}

}



public static void main(String[] args) {
		

		int count =0;
	
		for (int i = 2; i < 10; i++) {
			for (int j = 1; j < 10; j++) {
				int result = i * j;
				
				if ((result % 2 == 0)&&(result%3==0)) {
					count++;
					System.out.println(i + "*" + j + "=" + result+"갯수는"+count);
				}
			}
			System.out.println();
		}
		System.out.println("갯수는"+count);
	}

별찍기

/*
		for(int i=1; i<=5; i++) {
			System.out.println("*****");
			*/
		/*
		for (int i=1; i<=5; i++) {
			for (int j=1; j<=5; j++) {
				System.out.print("*");
			}
			System.out.println();
		}
		*/



public class gugudan2 {

	public static void main(String[] args) {
		
		for(int i=1; i<=5; i++) {
			for(int j=i; j<=5; j++) {
				
				System.out.print("*");
			}
			
		System.out.println();
		}
	}

}

![image-20211008150241640](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008150241640.png)

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 1; i <= 5; i++) {
			for (int j = 5; j > 0; j--) {
				if (i < j) {
					System.out.print(" ");
				} else {
					System.out.print("*");
				}
			}System.out.println("");
		}
	}

}

![image-20211008162710401](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008162710401.png)

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 1; i <= 5; i++) {
			for (int j = 5; j > 0; j--) {
				if (i < j) {
					System.out.print("_");
				} else {
					System.out.print("*");
				}
			}System.out.println("");
		}
	}

}
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
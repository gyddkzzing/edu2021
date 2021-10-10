# 2021.10.08 윤정아

#### 학습정리

1. 반복문 무한루프 만드는 세가지 방법은?

   - while 
   - do - while 
   - 이중 for문

2. 아래와 같이 출력 되도록 프로그래밍 하시오.(반복문 사용 할 필요 없음.)

   126500 의 금액을 한국 화폐로 바꾸었을 때 각각 몇 개의 화폐가 필요한지 계산해서 출력하기
   예) int 126500;
   오만원 : 2장	
   만원:    2장
   오천원 :1장
   천원: 1
   오백원: 1개
   백원: 0개

   

3. 구구단 출력을 하시오. 

   	public static void main(String[] args) {
   	
   		for (int i = 1; i <= 9; i++) {
   			for (int j = 1; j <= 9; j++) {
   				System.out.println(i + "*" + j + "=" + (i * j));
   			}	
   		}	
   	}

4. 구구단 짝수 출력을 하시오.

   public static void main(String[] args) {

   		for (int i = 1; i <= 9; i++) {
   			for (int j = 1; j <= 9; j++) {
   				if((i*j)%2==0)
   				System.out.println(i + "*" + j + "=" + (i * j));
   			}	
   		}	
   	}

5. 구구단 3의 배수 단(3,6,9)만 출력 하시오.

   public static void main(String[] args) {

   		for (int i = 1; i <= 9; i++) {
   			if(i%3==0)
   			for (int j = 1; j <= 9; j++) {
   				System.out.println(i + "*" + j + "=" + (i * j));
   			}	
   		}	
   	}

6. 아래 별을 찍으시오.

- <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008165947792.png" alt="image-20211008165947792" style="zoom:80%;" />

public static void main(String[] args) {

		for (int i = 1; i <=4; i++) {
			for (int j = 1; j <= 5; j++) {
					System.out.print("*"); //j의 출력문?
			}
			System.out.println(); //i의 출력문
		}
	}
7. 아래의 별을 찍으시오.

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008170422475.png" alt="image-20211008170422475" style="zoom:80%;" />

public static void main(String[] args) {

		for (int i = 1; i <=5; i++) {
			for (int j = 1; j <= i; j++) {
					System.out.print("*"); 
			}
			System.out.println();
		}
	}
8. 아래의 별을 찍으시오.

   

<img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008172542396.png" alt="image-20211008172542396" style="zoom:80%;" />

	public static void main(String[] args) {
	
		for (int i = 1; i <=5; i++) {
			for (int j = i; j <= 5; j++) {
					System.out.print("*"); 
			}
			System.out.println();
		}
	}
9. 아래의 별을 찍으시오.

   <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211008172619977.png" alt="image-20211008172619977" style="zoom:80%;" />

public class Hak {

	public static void main(String[] args) {
		for (int i = 0; i < 5; i++) { 
			for (int j = 4; j >= 0; j--) {
				if (i < j) { //공백 출력
					System.out.print(" ");
				} else { //별 출력
					System.out.print("*");
				}
			}
			System.out.println();
		}
	
	}
}

10. 아래의 별을 찍으시오.

    <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211010192258538.png" alt="image-20211010192258538" style="zoom:80%;" />

public class Hak {

	public static void main(String[] args) {
		for (int i = 0; i <5; i++) {  // 5줄 생성
	        for (int j = 0; j < i; j++) {
	            System.out.print(" "); //공백 출력
	        }		
	        for (int j = 4; j >=i; j--){ 
	            System.out.print("*"); //별 출력
	        }
	        System.out.println();
	    }
	
	}
}



11. 아래의 별을 찍으시오.

    <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211010192234064.png" alt="image-20211010192234064" style="zoom:80%;" />

    public class Hak {

    ```
    public static void main(String[] args) {
    
    	for(int i=0; i<5; i++){ //5줄 생성 
            for(int j=0; j<4-i; j++){ //공백 
                System.out.print(" ");
            }
            for(int j=0; j<2*i+1; j++) { //별출력 
                System.out.print("*");
            }
            System.out.println();
        }
    }
    ```
    }

12. 구구단에서 2의 배수이자 3의 배수인 수의 갯수는?  29? 52?

    public static void main(String[] args) {
    		
    		int count =0;
    		
    		for (int i=1; i<=9; i++) { 
    			for (int j = 1; j <=9; j++) {
    				int result = i*j;
    				if((result%2==0)&&(result%3==0))
    					continue;	
    				count++;
    			}
    		}System.out.println("count:"+count);
    	}

13. 다음과 같이 출력하시오.

    <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211010192501223.png" alt="image-20211010192501223" style="zoom:50%;" />

    public class gugudan2 {

    	public static void main(String[] args) {
    	
    		for (int i = 1; i <= 5; i++) {
    			System.out.println(i+". Hi");
    		}
    	}

14. 아래와 같이 출력하시오.

    <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211010192522048.png" alt="image-20211010192522048" style="zoom:50%;" />

    public class gugudan2 {

    	public static void main(String[] args) {
    	
    		for (int i = 1; i <= 5; i++) {
    			for(int j=1; j<=5; j++) {
    				System.out.print(i);
    			}
    			System.out.println();
    		}
    	}
    }

    

15. 아래와 같이 출력하시오.

    

    <img src="C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211010192532081.png" alt="image-20211010192532081" style="zoom:50%;" />

    

public class gugudan2 {

	public static void main(String[] args) {
	
		for (int i = 1; i <= 5; i++) {
			for(int j=1; j<=5; j++) {
				System.out.print(i+j);
			}
			System.out.println();
		}
	}
# 2021.10.01 윤정아

#### 1. 오늘 강의의 주요 주제들은?

#### - 메모리엔 주소가 있다.

#### - JVM은 32 비트.

#### - 32 비트 운영체제에는 메모리 얼마까지 사용 가능?

#### - javac와 java명령어는 뭐하는건가요?

컴파일 / 실행





 웹 프로그래밍 JSP (Java Server Page)

-Javascript + CSS + HTML + Jquery

- reacte or ##vue## or angular or 벨로시티



Hello.class 를 메모리에 올린다.

cpu와 통신을 하면서...



##### 터미널로 가는 방법 

- 오른쪽 마우스 Show in -> Terminal

자바는 Jvm(JRE) 위에서 돌아감.

그보다 높은 버전의 JDK를 사용하면 낮은 버전의 JRE가 알아들을 수 없음 -> 절대경로로 호출.

JVM은 32 비트다.



##### javac -> jvm이 알아듣는 실행파일을 만드는 것 

##### java -> 만들어진 .class 파일을 jvm이 메모리로 올리면서 우리 눈에 실행되는 것처럼 보임.

자바 컴파일러란? (Javac.exe)

자바런처란? (Java.exe)

JVM이 만들어진 파일을 메모리로 올리는 과정을 말함. 



![image-20211001124035742](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211001124035742.png)





**주석** : 컴파일에서 제외  //설명을 나타냄

**변수**: 메모리 공간의 할당과 접근을 위해 필요한 도구 





#### 면접 족보 #####

**1. 주석이란 무엇이며, 종류는?**

- 주석 : 코드에서 내가 하고 싶은 설명을 나타내며 컴파일에서는 제외된다. 

- 종류 : **//** 한 줄만 컴파일에서 제외 

  ​			**/* */**  여러 문장이 컴파일에서 제외 

**2. 주석은 컴파일 시 어떻게 되는가?**

주석은 컴파일 시 제외되며 결과에는 나타나지 않는다.

**3. 들여쓰기는 왜 해야 하는가?**

코드의 가독성을 위해서 하는 것이 깔끔하다. 

**4. 변수란 무엇인가?**

변할 수 있는 수 , 메모리 공간의 할당과 접근을 위해 필요한 도구

**5. 변수 선언의 의미는? **

메모리 할당 

**6. Java의 자료형 작성 (8 형제)에 대해 설명하시오.**

![image-20211001170416319](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211001170416319.png)



**7. int 형 범위는?**

-21억 ~ +21억

**8. int num; 을 메모리에 그리고 설명해보시오.**

![image-20211001171102833](C:\Users\JungAh\AppData\Roaming\Typora\typora-user-images\image-20211001171102833.png)

**9. java 언어를 창시한 사람은? **

제임스 고슬링

**10. JDK란 무엇이며, 어디서 다운로드 받으며, OS별로 버전이 있는 까닭은?**

- JDK는 개발자들이 JVM과 JRE에 의해 실행되고 구동 될 수 있는 자바 프로그램을 생성할 수 있게 해준다.
- 오라클에서 다운 받을 수 있다.
- OS별로 존재하는 윈도우, 리눅스 버전이 있고 똑같은 자바 소스코드로 가능? 

**11. JVM은 무엇의 약자? JVM이란 무엇인가?**

- Java Virtual Machine 자바 가상 머신으로 프로그램이 Jvm위에서 돌아간다. 

**12. WORA(Write Once, Run Averywhere)에 대해 설명하시오.**

- 플랫폼 종속성과 관련이 있다. 

- WORA를 가능하게 하는 것은 JAVA의 JRE => JRE을 한번만 컴퓨터에 세팅해주면 된다. 
- 기종(플랫폼)에 상관없이 독립적으로 하나의 자바소스와 하나의 자바 컴파일러를 통해 코드를 실행시킬 수 있게 되었음 

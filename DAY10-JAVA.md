///////////////////////////////////////////

class A {
	

	int num;
	
	void setNum(int n) {
		num=n;
	}
	
	int getNum() {
		return num;
	}
	
	void printNum(){
		System.out.println(num);
	}
}

public class ObjTest {

	public static void main(String[] args) {
	
		A a;
		a=new A();
		
		a.setNum(10);
		a.setNum(20);
		
		int num= a.getNum();
		System.out.println(num);
		a.printNum();//num은 10을 나타냄.


​		
​		//a.num=20;
​		
		//System.out.println(a.num);
	}

}

///////////////////////////////////////////////////////



class Circle{
	double r;
	
	public double getR() {
		return r;
	}
	
	public void setR(double rad) { //값을 세팅하니까 보이드? 아닌 듯
		r=rad; //원래 있는 값에 세팅만 해주는 것 위에 r이 있음.
	}
	
	public double getArea() {
		return r*r*Math.PI;
	}
}

class Rectangle{
	
	int width;
	int height;
	
	public int getWidth() {
		return width;
	}
	public void setWidth(int width) {
		this.width = width;
	}
	public int getHeight() {
		return height;
	}
	public void setHeight(int height) {
		this.height = height;
	}
	
	public int getArea() {
		return height*width;
	}
}

public class ObjTest {

	public static void main(String[] args) {
		
		Rectangle rec= new Rectangle();
		
		rec.setHeight(10);
		rec.setWidth(10);//안에 있는 인스턴스 변수를 집어넣는 것
	
		System.out.println(rec.getArea());
		
		rec.setHeight(20);
		rec.setWidth(20);//안에 있는 인스턴스 변수를 집어넣는 것
	
		System.out.println(rec.getArea());
		
		rec.setHeight(30);
		rec.setWidth(30);//안에 있는 인스턴스 변수를 집어넣는 것
	
		System.out.println(rec.getArea());
		/*
		Circle circle =new Circle();
		
		circle.setR(10);
		
		double area=circle.getArea();
		System.out.println(area);
		
		circle.setR(20);
		
		System.out.println(circle.getArea());
		*/
	}
}



////////////////////////////////////////





class Grade {
	int math, science, english;
	Grade(int math, int science, int english) {
		this.math=math;
		this.science=science;
		this.english=english;
	}

	public double average() {
		double avg=(math+science+english)/3.0;
		return avg;
	}
	
	public String getGrade() {
		double avg=average();
		String str;
		if(avg>=90){
			str="수 입니다.";
		}else if(avg>=80) {
			str="우 입니다.";
		}else {
			str="나가리 입니다.";
		}
		return str;
	}
}

public class ObOb {

	public static void main(String[] args) {
	
		int math, science, english;
		math=90;
		science=100;
		english=80;
		
		Grade me =new Grade(math,science,english);
		System.out.println("평균은 "+me.average());
		System.out.println(me.getGrade());
	}

}



### 학습 정리

1. 아래의 BankAccount(소스 PPT 참고) 에 대하여 메모리 그림을 그리시오.

   BankAccount ref1 = new BankAccount();
   BankAccount ref2 = ref1;





2. 생성자란 무엇인가요?

   - **생성자란 new 연산자로 호출되는 특별한 중괄호 { }블록이다.**

   - 생성자는 메소드와 비슷하게 생겼지만, **클래스 이름**으로 되어있고, **리턴타입이 없다.**
   - 만약 생성자가 성공적으로 실행되지 않고 예외가 발생됐다면 객체는 생성되지 않는다. 

3. 디폴트 생성자에 대해 설명하시오.

   클래스 내부에 생성자 선언을 생략했다면 컴파일러는 다음과 같이 중괄호 { } 블록 내용이 비어있는 Defalt Constrictor를 바이트 코드에 자동 추가 시킨다. 

4. 생성자의 용도는? 

   객체 생성 시 초기화를 담당 => 필드를 초기화하거나, 메소드를 호출해서 객체를 사용할 준비를 한다.

5. Null에 대하여 설명하시오.

   값이 없다는 뜻.

6. 아래의 TV클래스를 만드시오. 

class TV{
	String brand;
	int year;
	int inch;
	
	TV(String brand, int year, int inch){
		this.brand =brand;
		this.year=year;
		this.inch= inch;
	}
	
	public void show() {
		
		System.out.println(brand+"에서 만든 "+year+"년 "+inch+"인치 TV");
		
	}

}

public class TvEx1 {
	public static void main(String[] args) {
		TV myTV = new TV("LG", 2017, 32);
	}

}



7. 아래의 Grade 를 만드시오. 

class Grade{
	int math, science, english;
	
	Grade(int math, int science,int english){
		this.math=math;
		this.science=science;
		this.english=english;
	}
	
	public double average() {
		double avg=(math+science+english)/3.0;
		return avg;
	}
	
	public String getGrade() {
		double avg = average();
		String str;
		if(avg>=90) {
		str="수 입니다.";
		}else if(avg>=80) {
		str="우 입니다.";
		}else if(avg>=70) {
		str="미 입니다.";
		}else {
		str="양가 입니다.";
		}
		return str;
	}


​	
}

public class GradeEx1 {
	public static void main(String[] args) {
		int math, science, english;
		math = 90;
		science = 80; 
		english = 80;

		Grade me = new Grade(math, science, english);
		System.out.println("평균은 " + me.average());
		System.out.println(me.getGrade()); //우 입니다.
	}

}



8. 노래 한 곡을 나태내는 song 클래스를 작성하라 >> song 은 다음 필드로 구성된다. 

   - 노래의 제목을 나타내는 title
   - 가수를 나타내는 artist
   - 노래가 발표된 연도를 나타내는 year
   - 국적을 나타내는 country

   또한 Song 클래스에 다음 생성자와 메소드를 작성하라.

   - 생성자 2개: 기본 생성자와 매개변수로 모든 필드를 초기화하는 생성자
   - 노래 정보를 출력하는 show() 메소드
   - main() 메소드에서는 

   Song 객체로 생성하고 
   show()를 이용하여 노래의 정보를 다음과 같이 출력하라.

   출력:
   1978년, 스웨덴 국적의 ABBA가 부른 "Dancing Queen"



class Song{
	String title; //노래 제목
	String artist; // 가수
	int year; //노래 발표 연도
	String country; //국적
	
	Song(){ //defalt 생성자
		
	}
	Song(String title, String artist, int year, String country){
		//모든 필드를 초기화하는 생성자
		this.title=title;
		this.artist=artist;
		this.year=year;
		this.country=country;
	}
	public void show() {
		System.out.println(year+"년, "+country+" 국적의 "+artist+"가 부른 "+title);
	}
}

public class SongEx1 {
	public static void main(String[] args) {
		String title; //노래 제목
		String artist; // 가수
		int year; //노래 발표 연도
		String country; //국적
		
		Song song=new Song("\"Dancing Queen\"","ABBA", 1987,"스웨덴");
		song.show();
	}

}
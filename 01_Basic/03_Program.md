# 자바 프로그램

## 간단한 형식
- 한 개 이상의 클래스로 구성
- 클래스 -> 한 개 이상의 필드나 메소드로 구성

<br><br>

```java
class 클래스이름 {
	필드의 선언
	필드의 선언
	...
	메소드의 선언
	메소드의 선언
	...
}
```

<br><br>

```java
class Test {
	int	field1;
	String	field2;

	public void method1() {
		System.out.println("자바");
	}
}
```

<br><br>

## main() 메소드
- 자바 프로그램의 실행
- -> main() 메소드 찾음
- -> 그 안의 모든 명령문 차례로 실행
- 따라서 하나의 자바 프로그램, **main() 메소드 클래스 1개 이상 존재**해야
- **반드시 public static void로 선언**
- **public 클래스 단 1개**
- public 클래스가 존재 -> **파일 이름 == public 클래스 이름**


<br><br>

```java
public static void main(String[] args) {
	...
}
```

<br><br>

## 명령문
- 자바 프로그램의 동작을 명시
- 명시 == 컴퓨터에게 동작을 알려준다
- 세미콜론으로 끝

<br><br>

## 주석
- 코드에 대한 이해를 돕는 설명을 적음
- 디버깅을 위해 작성함
- 자바 컴파일러 -> 주석은 무시하고 컴파일
- 실제 실행 결과에 영향 X
- 한 줄 주석, 여러 줄 주석(여러줄 끼리 중첩X)

<br><br>

```java
//한줄 주석
/*
* 여러 줄 주석
*/
```

<br><br>

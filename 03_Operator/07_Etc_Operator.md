# 기타 연산자

## 삼항 연산자

- 삼항 연산자는 자바에서 유일하게 피연산자를 세 개 가지는 조건 연산자입니다.
- 삼항 연산자의 문법은 다음과 같습니다.

<br>

```html
조건식 ? 반환값1 : 반환값2
```

<br>

- 물음표 앞의 조건식에 따라 결과값이 참이면 반환값1을 반환하고, 결과값이 거짓이면 반환값2를 반환합니다.

<br>

```java
int	num1;
int	num2;
int	result;

num1 = 5;
num2 = 7;
result = (num1 - num2 > 0) ? num1 : num2;
System.out.println("두 정수 중 더 큰 수는 " + result + "입니다."); //7
```

<br>

---

<br>

## instance of 연산자

- instance of 연산자는 참조 변수가 참조하고 있는 인스턴스의 실제 타입을 반환해줍니다.
- 해당 객체가 `어떤 클래스나 인터페이스로부터 생성되었는지를 판별해주는 역할`을 합니다.
- 문법은 다음과 같습니다

<br>

```html
인스턴스이름 instanceof 클래스 또는 인터페이스 이름
```

<br>
- instanceof 연산자는 왼쪽 피연산자인 인스턴스가 오른쪽 피연산자인 클래스나 인터페이스로부터 생성되었으면 true를 반환하고, 그렇지 않으면 false를 반환합니다.

<br>

```java
class	A {}
class	B extends A {}
public static void main(String[] args) {
	A a = new A();
	B b = new B();
	System.out.println(a instanceof A); //true
	System.out.println(b instanceof A); //true
	System.out.println(a instanceof B); //false
	System.out.println(b instanceof B); //false
```

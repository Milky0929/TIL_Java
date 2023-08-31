# 논리 연산자

## 논리 연산자

- 논리 연산자는 주어진 논리식을 판단하여,참과 거짓을 결정하는 연산자입니다
- And 연산과 Or 연산은, 두 개의 피연산자를 가지는 이항연산자입니다.
	- 피연산자들의 결합방향은 왼쪽 -> 오른족입니다.
- Not 연산자는 피연산자가 단 하나뿐인 단항 연산자입니다
	- 피연산자의 결합 방향은 오른쪽 -> 왼쪽입니다.

<br>

|논리 연산자|설명|
|-----------|----|
|\&\&|논리식이 모두 참이면 참을 반환함. (논리 AND 연산)|
|\|\||논리식 중에서 하나라도 참이면 참을 반환함. (논리 OR 연산)|
|\!|논리식의 결과가 참이면 거짓을, 거짓이면 참을 반환함. (논리 NOT 연산)|

<br>

- 아래는 논리 연산자의 모든 동작의 결과를 보여주는 진리표입니다.

<br>

|A|B|A \&\& B|A \|\| B|	\!A|
|-|-|--------|--------|----|
|true|true|true|true|false|
|true|false|false|true|false|
|false|true|false|true|true|
|false|false|false|false|true|

<br>

```java
char	ch1;
char	ch2;
boolean	result1;
boolean	result2;

ch1 = 'b';
ch2 = 'B';
result1 = (ch1 > 'a') && (ch1 < 'z');
result2 = (ch2 < 'A') || (ch2 < 'Z');

System.out.println("&& 연산자에 의한 결과:" + result1); //true;
System.out.println("|| 연산자에 의한 결과:" + result2); //true;
System.out.println("! 연산자에 의한 결과:" + !result2); //false;
```

<br>

- 위의 예제처럼 자바는 char형 문자끼리도 그 크기를 비교할 수 있습니다. 



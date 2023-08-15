#Java8 변경 사항

##주요 변경사항
- Java SE 8 버전부터 많은 사항 변경 및 추가
- 람다 표현식 : 함수형 프로그래밍
- 스트림 API : 데이터의 추상화
- java.time 패키지 : Joda-Time을 이용한 새로운 날짜와 시간 API
- 나즈혼 : 자바스크립트의 새로운 엔진

<br><br>

##람다 표현식
- 메소드를 하나의 식으로 표현한 것
- 식별자 없이 실행할 수 있는 함수 표현식
- == 익명함수
- 클래스를 만들고 객체를 생성하지 않아도 메소드 사용OK
- 람다표현식 -> 매소드의 매개변수로 전달 OK
- 람다표현식 -> 메소드의 결괏값으로 반환 OK
- 기존의 불필요한 코드 Down
- 작성된 코드의 가독성 Up

<br><br>

```java
new Thread(new Runnable() {
	public void run() {
		System.out.println("전통적인 방식의 일회용 스레드 생성");
	}
}).start();
```

<br><br>

```java
new Thread(()->{
	System.out.println("람다 표현식을 사용한 일회용 스레드 생성");
}).start();
```

<br><br>

##스트림 API
- 문제점
- 기존의 자바 -> 많은 양의 데이터를 배열,컬렉션을 사용해 저장
- 기존의 자바 -> 반복문, 반복자를 사용하여 매번 코드 작성을 통해 데이터 접근
- 가독성 Down, 재사용성 Down, 정형화된 데이터 처리 패턴 X
- 해결
- 스트림 API -> 데이터를 추상화, 데이터를 읽고 쓰기 위한 공통 방법 제공
- 스트림 API -> 배열 + 컬렉션 + 파일에 저장된 데이터 -> 모두 같은 방법처리

<br><br>

```java
String[] arr = new String[]{"하나", "둘", "셋", "넷"};

//배열에서 스트림 생성

Stream<String> stream1 = Arrays.stream(arr);
stream1.forEach(e -> System.out.print(e + " "));
System.out.println();

//배열의 특정 부분만을 이용한 스트림 생성
Stream<String> stream2 = Arrays.stream(arr, 1, 3);
stream2.forEach(e -> System.out.print(e + " "));
```

<br><br>

##java.time 패키지
- JDK 1.0 : Date 클래스 -> 날짜에 관한 처리 수행
	- 문제점
	- Date 클래스는 대부분의 메소드가 사용권장 X 상태
- JDK 1.1 : Calendar 클래스 -> 날짜와 시간 정보 제공
	- 문제점
	- Calendar 인스턴스 != 불변 객체 -> 값 수정 가능성 O
	- 윤초와 같은 특별한 상황 고려 X
	- Calendar 클래스 -> 1월 ~ 12월을 0에서 11로 표현
	- 임시방편 -> Joda-Time
- Java SE 8 : java.time 패키지 -> 문제점 모두 해결, 다양한 기능 지원

<br><br>

```java
LocalDate today = LocalDate.now();
System.out.println("올해는 " + today.getYear() + "년입니다.");

LocalDate otherDay = today.withYear(1982);
System.out.println("올해는" + otherDay.getYear() + "년입니다.");
```
<br><br>

##니즈혼
- 모질라 리노 : 지금까지의 자바스크립트 기본 엔진
	- 문제
	- 노후화 발생
- 나즈혼 : 자바스크립트의 새로운 엔진으로 도입
	- 해결
	- 성능과 메모리 개선

<br><br>



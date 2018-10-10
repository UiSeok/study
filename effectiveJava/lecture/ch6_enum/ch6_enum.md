# 열거형(enum)과 어노테이션


<br>
<br>

```
public static final int APPLE_JUICE = 1;
public static final int ORANGE_JUICE = 1;

APPLE_JUICE == ORANGE_JUICE ?
```

이 패턴은 문자열 반환으로도 확인하기 힘들다(정수만 반환됨)

변종 패턴인 String enum패턴이 있는데 이는 더 나쁘다.(하드코딩, 오타)

<br>
<br>



## enum의 특징

- Java 의 enum은 여타 언어의 enum과는 다르다(다른 언어들은 단순 int형인 경우가 많다. 대표적으로 C++)

- Java의 enum은 완전한 클래스로 컴파일 시점의 형 안전성(type safety)을 제공한다.

- enum 상수에 데이터를 넣으려면 객체 필드를 선언하고 생성자를 통해 받은 데이터를 그 필드에 저장하면 된다(enum은 immutable 하므로 모든 필드는 final로 선언된다.)

- 데이터 접근은 public 으로 지정해도 되지만 접근자(getter)를 두는게 더 좋다.

- enum이 제공하는 기본 메서드(toString, values)들은 각 type별로 override될 수 있고 abstract method를 정의하면 각각 type별로 메소드를 별도로 구성할 수 있다.



<br>
<br>


## enum의 기본제공 method

- toString : 문자열화
- values : enum내부의 데이터 전체
- valueOf : 상수 이름을 상수 그 자체로 변환


<br>
<br>

## ordinal 쓰지마라

- ordinal이란 함수는 해당 enum의 위치를 정수값으로 반환하는 함수이다. 쓰지마라


<br>
<br>

## bit field 대신 enumSet을 사용하라

<br>
<br>

## ordinal 배열첨자를 쓰지 말고 enumMap을 써라

<br>
<br>

## 확장 가능한 enum을 만들어야 하면 인터페이스를 활용하라

계승 가능한 enum은 만들 수 없지만 인터페이스를 만들고 그 기본 인터페이스를 구현하는 enum을 만들면 비슷하게 흉내낼 수 있다.

<br>
<br>


## 어노테이션이 있으므로 더이상 작명 패턴에 기대지마라

## 대부분의 프로그래머는 어노테이션 자료형을 정의할 필요가 없다


<br>
<br>


## Override 어노테이션 잘 써라





<br>
<br>
<br>
<br>

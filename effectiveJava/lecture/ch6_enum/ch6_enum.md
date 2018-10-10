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

- 



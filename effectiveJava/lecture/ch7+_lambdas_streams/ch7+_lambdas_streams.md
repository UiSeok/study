# Lambdas and Streams

<br>
<br>


## 익명 클래스 대신에 람다를 사용해라

- 구체적인 parameter type 이 프로그램을 명확하게 해주지 않는 이상 람다 parameter type 은 생략해라
- 타입 지정 시 String::length 와 같은 DoubleBinaryOperator 인터페이스를 사용하자
- 람다는 문서나 이름이 없기 때문에 몇 줄을 초과하는 로직이나 계산이 명확하지 않은 경우는 람다에 넣지 마라(1줄이 이상적, 3줄이 최대)
- 람다는 아주 드물게 직렬화를 해야할 때가 있다
- 함수 인터페이스가 아닌 유형의 인스턴스를 만들지 않는 경우에는 함수 객체에 익명 클래스를 사용하지 마라


<br>
<br>


## 람다보단 메소드 레퍼 호출을 사용해라
```
1. map.merge(key, 1, (count, incr) -> count + incr);
2. map.merge(key, 1, Integer::sum);
```
1번 보다는 2번으로


<br>
<br>

## 표준함수가 있다면 사용해라
```
ex1) String::toLowerCase
ex2) Arrays::asList
```
- boxing 된 함수 인터페이스에 유혹되지 마라 primitive 있음 그거 써라
- 항상 함수 인터페이스에는 @FunctionalInterface 어노테이션을 달아라


<br>
<br>

## 스트림은 현명하게 사용하라

스트림은 자바 8에 추가된 bulk 처리에 용이한 기능이다(선형 또는 병렬처리).
스트림은 크게 2가지 핵심 기능을 제공한다.
1. stream : 유한 또는 무한한 데이터의 흐름 그 자체
2. stream pipe line : 이 데이터 흐름에 대한 멀티처리





<br>
<br>
<br>

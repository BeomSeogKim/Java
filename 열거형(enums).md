# 열거형(enums)
### 열거형이란?
열거형은 서로 관련된 상수를 편리하게 선언하기 위하여 사용되는 것으로 여러 상수를 정의 할 때 사용하면 유용하다
열거형을 쓴 class와 쓰지 않은 class를 비교하면 다음과 같다.  
enum을 사용하지 않을 경우 
```java
class Card {
  static final int CLOVER = 0;
  static final int HEART = 1;
  static final int DIAMOND = 2;
  static final int SPADE = 3;
  
  static final int TWO = 0;
  static final int THREE = 1;
  static final int FOUR = 2;
  
  final int kind;
  final int num;
}

```
enum을 사용할 경우 
```java
class Card{
  enum Kind {CLOVER, HEART, DIAMOND, SPADE}
  enum Value {TWO, THREE, FOUR}
  
  final Kind kind;
  final Value value;
}
```
기존 언어들과는 달리 자바의 열거형은 '타입에 안전한 열거형'이다.   
'타입에 안전한 열거형' 이란 실제 값이 같더라도 타입이 다르면 에러를 발생시키는 것을 말한다. 
___
### 열거형의 정의와 사용
열거형을 정의하는 방법은 간단하다. 
```java
enum 열거형이름 {상수명1, 상수명2, ***}
```
열거형 상수간의 비교는 equal() method 가 아닌 ==을 사용한다.  대신 < , > 와 같은 연산자는 사용할 수 없다.  
추가적으로 열거형의 상수값을 명시해주고자 할 떄에는 열거형 상수 이름 옆에 원하는 값을 ()와 함께 적어주면 된다.
```java
enum Direction { EAST(1), SOUTH(2) , WEST(-1) , NORTH(10) }
```

참고문헌: Java의 정석

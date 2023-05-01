# Object Oriented Programming1

## 목차

[상속](#상속)

<br>

## 상속

객체지향 프로그래밍의 꽃 상속이다.

상속은 기존 클래스를 재사용하여 새 클래스를 작성하는 것이다.

```java
class Parent {
}

class Child extends Parent{
}
```

조상 클래스는 Parent고, 자식 클래스는 Child다.

<br>

상속에서 생성자와 초기화 블록은 상속되지 않고, 멤버(멤버변수, 멤버메소드)만 상속된다.

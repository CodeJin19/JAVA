# Object Oriented Programming1

## 목차

[다형성](#다형성)

[추상클래스](#추상클래스)

[추상메서드](#추상메서드)

[인터페이스](#인터페이스)

<br>

## 다형성

객체지향 프로그래밍을 대표하는 또 다른 특징인 다형성이다.

상속을 통해 조상 클래스를 더 구체화하는 자손 클래스를 생성하였다면,

다형성은 조상 클래스의 참조변수에 자손 클래스의 인스턴스를 대입하는 것을 뜻한다.

하지만 반대로 자손 클래스의 참조변수에 조상 클래스의 인스턴스를 대입할 수는 없다.

```java
class Parent {
}

class Child extends Parent{
}

public static void main (String[] args) {
   Parent p = new Child(); //다형성
   Child c = new Parent(); //에러
}
```

<br>

## 추상클래스

추상 클래스는 추상 메서드를 한 개 이상 갖고 있는 클래스다.

추상 클래스를 선언하기 위해서는 클래스 앞에 추상 키워드인 `abstract`를 추가하면 된다.

<br>

## 추상메서드

추상 메서드는 구현부 없이 선언부만 존재하는 메서드다.

추상 메서드의 구현부는 추상 클래스를 상속받은 자손 클래스에서 오버라이딩하여 사용한다.

추상 메서드는 다음과 같이 선언한다.

```java
abstract class AbstractClass {
   abstract void abstractMethod();
}
```

<br>

그리고 추상 메서드는 다음과 같이 사용할 수 있다.

```java
abstract class AbstractClass {
   abstract void abstractMethod();
}

class someClass extends AbstractClass{
   @Override
   void abstractMethod() {
      //내용
   }
}
```

<br>

## 인터페이스

인터페이스는 **추상메서드와 상수로만 이루어진 추상클래스**다.

추상클래스와 같이 온전한 메서드나 멤버변수를 가질 수 없다.

인터페이스는 Interface로 선언할 수 있으며 사용 방법은 다음과 같다.

```java
Interface someInterface{
   public abstract abstractMethod();
}
```

<br>

인터페이스의 모든 멤버변수는 `public static final`이며, 모든 메서드는 `public abstrat`인데, 생략 가능하다.

<br>

추상메서드를 구현하기 위해서는 자손 클래스에서 구현해야 하듯이, 인터페이스의 추상 메서드를 구현하기 위해서는 인터페이스를 상속받는 자손 클래스를 생성 후, 구현해야한다.

```java
Interface someInterface{
   public abstract void abstractMethod();
}

class someClass implements someInterface {
   @Override
   public void abstractMethod() {
      //구현부
   }
}
```
 
<br>

클래스가 인터페이스를 상속할 때는 implements 키워드를 사용한다.

인터페이스를 상속받은 클래스는 인터페이스의 모든 추상 메서드를 구현해야 한다.

그렇지 않을 경우, 해당 클래스에 abstract를 붙여 추상클래스로 선언해야 한다.

또한, 인터페이스는 인터페이스로부터 상속 가능하다.

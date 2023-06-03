# Exception1

## 목차

[프로그램 오류](#프로그램-오류)

[try catch](#try-catch)

<br>

## 프로그램 오류

프로그램 오류에는 다음 세 가지가 있다.

컴파일 에러 - 컴파일 시에 발생하는 에러
런타임 에러 - 런타임 시에 발생하는 에러
논리적 에러 - 실행은 되지만, 의도와는 다르게 동작하는 에러

<br>

자바에서는 런타임 에러를 다음 두 가지 클래스로 분류했다.

에러 (error) - 프로그램 코드에 의해서 수습될 수 없는 심각한 오류
예외 (exception) - 프로그램 코드에 의해서 수습될 수 있는 다소 미약한 오류

<br>

에러 클래스와 예외 클래스 모두 클래스이므로 Object의 자손 클래스다.

<br>

exception은 크게 두 가지로 나눌 수 있는데, 프로그래머의 실수로 발생하는 runtime exception 클래스와 사용자의 실수로 발생하는 exception이다.

<br>

## try catch

예외는 크게 두 가지 방식으로 처리할 수 있는데, 직접 처리하는 것과 간접 처리하는 것이다.

직접 처리는 try-catch문을 사용한다.

```java
public static void main (String[] args) {
   try {
      //예외가 발생할 수 있는 로직
   } catch(Exception e) {
      //예외 처리 로직
   }
}
```

<br>

예외가 발생할 수 있는 로직을 try 블럭에 작성한 후, catch 블럭에서 예외를 처리한다.

다음과 같이 여러 예외를 처리할 수도 있다.

```java
public static void main (String[] args) {
   try {
      //예외가 발생할 수 있는 로직
   } catch(Exception1 e1) {
      //예외 처리 로직
   } catch(Exception2 e2) {
      //예외 처리 로직
   }
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

<br>

## 익명클래스

익명클래스는 이름이 없는 클래스다.

이름이 없기 때문에 지칭할 수 없으며, 따라서 단 한 번만 사용될 수 있는, 단 하나의 객체만을 생성할 수 있는 일회용 클래스다.

익명클래스의 사용 방법은 다음과 같다

```java
new 조상클래스이름() {
   //구현부
}

new 인터페이스이름() {
   //구현부
}
```

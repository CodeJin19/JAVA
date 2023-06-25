# java.lang Package

## 목차

[Obejct](#Object)

[equals](#equals)

<br>

## Object

Object 클래스에는 유용한 클래스 메서드가 여럿 있다.

특히 Object 클래스는 모든 객체의 조상인만큼, 모든 객체에서 활용가능하니 유용한 클래스 메서드를 정리해보자.

<br>


## equals

equals는 두 객체의 참조변수를 비교하여 같으면 true를, 다르면 false를 반환한다.

여기서 중요한 점은 두 객체의 값이 아니라, 참조변수를 비교한다는 점이다.

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

예외 클래스에는 해당 예외에 대한 정보가 담겨 있는데, 이는 getMessage()와 printStackTrace()를 사용하여 확인할 수 있다.

```java
public static void main (String[] args) {
   try {
      //예외가 발생할 수 있는 로직
   } catch(Exception1 e1) {
      //예외 처리 로직
      e1.printStackTrace();
      System.out.println(e1.getMessage());
   } catch(Exception2 e2) {
      //예외 처리 로직
      e2.printStackTrace();
      System.out.println(e2.getMessage());
   }
}
```

<br>

## 예외 발생 방법

인위적으로 예외 발생 방법은 간단하다.

예외 인스턴스를 생성한 후, throw 키워드를 이용하면 된다.

```java
public static void main (String[] args) {
   Exceptione e = new Exception("테스트");

   throw e; //에러 발생
}
```

<br>

## throw

예외를 직접적으로 처리하는 방법이 try-catch 구문이라면, 간접적으로 처리하는 방법은 throw다.

메서드 선언부 뒤에 throw와 간접적으로 처리할 예외 클래스를 적으면 된다.

```java
public static void main (String[] args) {
   try {
      func1();
   } catch(Exception1 e1) {
      //예외 처리 로직
   } catch(Exception2 e2) {
      //예외 처리 로직
   }
}

public static void func1() throws Exception1, Exception2 {
   /*
   //이 예제에서는 throws를 통해 간접적으로 예외를 처리하기 때문에
   //아래 코드는 예외를 직접 처리하는 로직은 필요없다.
   try {
      //예외가 발생할 수 있는 로직
   } catch(Exception1 e1) {
      //예외 처리 로직
   } catch(Exception2 e2) {
      //예외 처리 로직
   }
   */
}
```

<br>

throws가 붙은 메서드는 예외 발생 시, 예외를 호출한 메서드에서 직접 처리하게 던지는 방법이다.
# java.lang Package

## 목차

[Obejct](#Object)

<br>

## Object

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

<br>

## finally

finally는 try catch문 뒤에 오는 블럭으로 예외가 발생하던, 발생하지 않던 항상 실행되는 블럭이다.

**심지어, 중간에 return문을 만나더라도 finally구문은 항상 실행된다.**

```java
public static void main (String[] args) {
   try {
      //예외가 발생할 수 있는 로직
   } catch(Exception e) {
      //예외 처리 로직
   } finally {
      //항상 실행될 로직
   }
}
```

<br>

try catch finally의 진행 순서는 try > finally (예외가 발생하지 않는 경우)거나, try > catch > finally (예외가 발생하는 경우)다.

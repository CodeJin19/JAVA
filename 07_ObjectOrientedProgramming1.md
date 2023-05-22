# Object Oriented Programming1

## 목차

[상속](#상속)

[오버라이딩](#오버라이딩)

[조상 클래스 생성자](#조상-클래스-생성자)

[조상 클래스 기본 생성자](#조상-클래스-기본-생성자)

[패키지](#패키지)

[제어자](#제어자)

[final](#final)

[abstract](#abstract)

[접근 제어자](#접근-제어자)

[Singleton](#singleton)

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

<br>

두 클래스 간의 관계는 아래 두 가지로 나눌 수 있다.

1. is-a
   - 상속관계
   - a는 b다
2. has-a
   - 포함관계
   - a는 b를 갖고 있다

<br>

다중상속이 가능한 C++과는 달리 JAVA에서는 단일상속만 가능하다.

<br>

JAVA의 모든 클래스는 Object 클래스의 자손이다.

<br>

## 오버라이딩

오버라이딩이란 부모 클래스에 정의된 메서드를 자식 클래스에서 재정의하는 것이다.

오버라이딩은 다음 세 가지 조건이 충족되어야 한다.

1. 메서드의 이름이 같아야 한다
2. 매개변수가 같아야 한다
3. 반환타입이 같아야 한다

<br>

## 조상 클래스 생성자

조상 클래스 생성자는 자손 인스턴스를 생성하기 위해 조상 클래스를 생성할 때 호출되는 조상 인스턴스를 초기화하는 메서드다.

조상 클래스 생성자는 super()로 호출한다.

<br>

## 조상 클래스 기본 생성자

생성자가 정의되어 있지 않는 경우에는 컴파일러가 기본 생성자를 추가하듯이,

Object를 제외한 모든 클래스의 생성자 첫 줄에는 생성자, this() 또는 super()를 호출해야 한다. 그렇지 않으면 컴파일러가 super()를 생성자의 첫 줄에 추가한다.

<br>

## 패키지

패키지는 클래스의 묶음으로, 다수의 클래스를 효율적으로 관리하기 위해 사용된다.

클래스의 정식 이름은 (패키지).(클래스)다.

예컨대, Math 클래스의 정식 이름은 java.lang.Math다.

이름에서 알 수 있듯이 각 클래스 파일들은 해당 패키지에 대응되는 디렉토리에 존재한다.

같은 이름의 파일이 서로 다른 디렉토리에 존재할 수 있듯이, 같은 이름의 클래스 파일도 서로 다른 패키지 내부에 존재할 수 있다.

<br>

패키지는 다음과 같이 선언할 수 있다.

```java
package com.example.java;

class PackageSample {
   public static void main (String[] args) {
      System.out.println("Hello, world!");
   }
}
```

패키지 선언은 모든 소스 파일에서 주석과 공백을 제외한 첫 문장이어야 한다.

또한, 패키지는 하나의 소스 파일에 한 번만 선언될 수 있다.

패키지 선언문이 없는 경우, 자바에서 기본적으로 이름없는 패키지(unnamed package)에 넣어준다.

<br>

프로그래밍을 할 때 다른 패키지의 클래스를 사용하려면 다음과 같이 해당 클래스의 정식이름을 사용해야한다.

```java
class PackageSample {
   public static void main (String[] args) {
      int y = 5;
      int x = 3;
      int big = java.util.Math.max(x, y);
   }
}
```

<br>

하지만 import문을 사용하여 사용할 클래스의 패키지를 미리 명시하면 다음과 같이 작성할 수 있다.

```java
import java.util.Math;

class PackageSample {
   public static void main (String[] args) {
      int y = 5;
      int x = 3;
      int big = Math.max(x, y);
   }
}
```

<br>

## 제어자

제어자란 클래스, 메서드, 변수 등에 사용되는 옵션이다.

특히, public, protected, default, private 이 4개는 접근 제어자로 한 번에 한 가지만 사용할 수 있다.

<br>

### final

final은 말 그대로 최종적이라는 뜻으로 더 이상 수정하지 못한다는 의미다.

final 클래스는 확장될 수 없는 클래스

final 메서드는 변경될 수 없는 메서드 <-> 오버라이딩 될 수 없음

<br>

### abstract

abstract 메서드는 추상 메서드, abstract 클래스는 추상 클래스라고 한다.

abstract 메서드는 선언부만 작성하고 구현부는 작성되지 않은 메서드다.

abstract 클래스는 abstract 메서드를 포함하고 있는 클래스다.

<br>

## 접근 제어자

접근 제어자는 멤버변수나 클래스에 사용되어, 각 멤버변수나 클래스의 접근을 제어하는 키워드다.

접근 제어자는 다음 네 가지가 있다.

1. private
   - 같은 클래스 내에서만 접근 가능
2. default
   - 같은 패키지 내에서만 접근 가능
3. protected
   - 같은 패키지와 타 패키지의 자손 클래스에서 접근 가능
4. public
   - 접근 제한 없음

<br>

## Singleton

싱글톤은 객체의 인스턴스를 단 하나만 생성하게 하는 디자인 패턴이다.

싱글톤은 다음과 같이 개발할 수 있다.

```java
class Singleton{
   private static Singleton s = new Singleton();

   private Singleton() {
      //...
   }

   public static Singleton getSingleton() {
      return s;
   }
}
```

<br>

간단히 요약하자면,

1. 생성자를 private으로 만들어서, 외부에서 2개 이상의 인스턴스를 만들지 못하게 한다

2. 멤버변수로 인스턴스를 정의하고, static으로 생성한다

   1. 생성자가 private이기 때문에 내부에서 호출해야함
   2. 내부에서 단 한 번 생성해야 하기 때문에 static으로 선언함

3. static으로 생성한 인스턴스에 접근하기 위해 get 메서드를 선언한다

<br>

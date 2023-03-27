# Object Oriented Programming

## 목차

[객체지향언어](#객체지향언어)

[클래스와 객체와 인스턴스](#클래스와-객체와-인스턴스)

[객체의 구성요소](#객체의-구성요소)

[변수와 메서드](#변수와-메서드)

[변수의 종류](#변수의-종류)

[메서드](#메서드)

<br>

## 객체지향언어

다음은 객체 지향의 대표적 특징이다.

> 1. 코드의 재사용성이 높다
>    - 새로운 코드를 작성할 때 기존의 코드를 이용하여 쉽게 작성할 수 있다.
> 2. 코드의 관리가 용이하다.
>    - 코드간의 관계를 이용해서 적은 노력으로 쉽게 코드를 변경할 수 있다.
> 3. 신뢰성이 높은 프로그래밍을 가능하게 한다.
>    - 제어자와 메서드를 이용해서 데이터를 보호하고 올바른 값을 유지하도록 하며, 코드의 중복을 제거하여 코드의 불일치로 인한 오동작을 방지할 수 있다.

<br>

## 클래스와 객체와 인스턴스

클래스란 객체를 정의해 놓은 것으로 객체를 만드는데 사용된다.

객체란 클래스를 통해 만들어진 실제하는 객체(물건)다.

클래스에서 객체를 만드는 것을 인스턴스화라고 하며, 이 때 만들어진 객체를 인스턴스라고 부른다.

<br>

### 인스턴스와 객체의 차이

넓은 의미로 보면 인스턴스와 객체, 모두 생성된 물체를 지칭하는 말이다.

객체는 포괄적인 의미에서 쓰이며, 인스턴스는 클래스와 객체의 연관성에 초점을 맞춰 쓰인다.

<br>

## 객체의 구성요소

객체는 멤버변수와 메서드로 이루어져있다.

멤버변수와 메서드, 모두 객체의 필수요소는 아니며, 한 객체에 여러 개의 멤버변수와 메서드가 있을 수 있다.

<br>

## 인스턴스의 생성과 사용

다음은 간단한 객체 예제이다.

```java
class Car {
    //클래스 car의 멤버변수
    int speed;
    int weight;
    static int totalCars;
    String model;

    //클래스 car의 메서드
    void getInfo() {
        System.out.println("model : " + model);
        System.out.println("weight : " + weight);
        System.out.println("current speed : " + speed);
    }
}

class carSample{
    public static void main(String args[]) {
        Car myCar;
        myCar = new Car();
        myCar.speed = 60;
        myCar.getInfo();
    }
}
```

객체 Car는 3개의 멤버변수와 1개의 메서드로 이루어져있다.

먼저, Car 객체를 생성하기에 앞서 클래스의 참조변수를 선언한다.

```java
Car myCar;
```

그리고 new를 사용하여 Car 객체를 인스턴스화 하고, 생성된 인스턴스의 객체 주소를 참조변수에 저장한다

```java
myCar = new Car();
```

<br>

## 변수와 메서드

### 변수의 종류

변수는 클래스 변수, 인스턴스 변수, 지역변수 세 가지가 있다.

아래 예제에서 클래스 변수는 totalCars이며, 인스턴스 변수는 speed, weight, model이다.

지역변수는 getInfo 등의 메서드에서 사용하는 변수로 아래 예제에는 지역변수 예시가 없다.

```java
class Car {
    //클래스 car의 멤버변수
    int speed;
    int weight;
    static int totalCars;
    String model;

    //클래스 car의 메서드
    void getInfo() {
        System.out.println("model : " + model);
        System.out.println("weight : " + weight);
        System.out.println("current speed : " + speed);
    }
}

class carSample{
    public static void main(String args[]) {
        Car myCar;
        myCar = new Car();
        myCar.speed = 60;
        myCar.getInfo();
    }
}
```

| 변수의 종류   | 선언 위치               | 생성 시기                   |
| ------------- | ----------------------- | --------------------------- |
| 클래스 변수   | 클래스 영역             | 클래스가 메모리에 올라갈 때 |
| 인스턴스 변수 | 클래스 영역             | 인스턴스가 생성되었을 때    |
| 지역 변수     | 클래스 영역 이외의 영역 | 변수 선언문이 수행되었을 때 |

<br>

### 메서드

메서드는 프로그램에서 반복적으로 사용되는 기능을 구현해놓은 것으로, 다른 언어에서 "함수"라고 한다.

다음음 메서드를 사용하는 이유다.

1. 높은 재사용성
2. 중복된 코드의 제거
3. 프로그램의 구조화

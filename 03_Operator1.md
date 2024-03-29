# Operator1

## 목차

[연산자](#연산자)

<br>

## 연산자

연산자란 연산기호를 뜻하고, 대표적으로 +, -, \*(곱하기), /(나누기) 등이 있다.

연산자는 크게 아래 네 가지로 묶을 수 있으며, 연산의 우선 순위는 다음과 같다.

<br>

- JAVA의 연산자

  1 산술

  2 비교

  3 논리

  4 대입

<br>

연산에는 가장 중요한 규칙이 있는데, 피연산자의 데이터 타입이 같아야 한다는 점이다.

예를 들어, 정수 3과 실수 2.2는 원칙적으로 더할 수 없다.

3과 2.2를 더하기 위해서는 형변환을 하여 같은 데이터 타입으로 일치시켜야 한다.

<br>

이 때 값의 오차를 줄이기 위해서는 더 큰 데이터형으로 변환해야 한다.

위 예제의 경우 메모리가 작은 정수형을 메모리가 더 큰 실수형으로 변환해야 값의 오차, 즉 손실이 없다.

```java
int a = 3;
double b = 2.2;
double x = (double) a + b; //3.0 + 2.2가 되어 5.2
```

만약 반대로, 실수형을 정수형으로 변환할 경우 아래와 같이 오차가 발생한다.

```java
int a = 3;
double b = 2.2;
int x = a + (int) b; //3 + 2가 되어 5
```

# JAVA Prologue1

## 목차

[JAVA의 특징](#JAVA의-특징)

[JVM](#JVM)

[JDK](#JDK)

[편집기](#편집기)

[JAVA의 실행 순서](#JAVA의-실행-순서)

[JAVA 기초](#JAVA-기초)

[main 메소드가 두 개 이상 있으면?](#main-메소드가-두-개-이상-있으면?)

[주석](#주석)

## JAVA의 특징

1. 운영체제에 독립적

   기존의 언어는 각 운영체제에 맞춰 개발됐기 때문에 다른 운영체제에서는 환경 이슈가 많았다

   특히, 언어가 운영체제나 하드웨어와 직접 통신하면서 다양한 환경 이슈 등으로 충돌이 잦았다

   하지만 자바는 자바가상머신(VJM, java virtual machine)하고만 통신한다

   즉, 자바가 운영체제나 하드웨어와 직접 통신하지 않기 때문에 앞서 설명한 충돌이 일어나지 않는다

   대신, 운영체제나 하드웨어와 직접 통신하는 JVM의 경우 이런 환경 이슈가 발생할 수 있다

<br>

2. Garbage Collection

   자바에는 가비지 콜렉터(garbage collector)가 자동으로 메모리를 관리해준다

   따라서 개발자들이 프로그래밍에 조금 더 집중할 수 있다

<br>

3. Muli-thread

   자바는 멀티쓰레드 기능을 지원한다

<br>

4. Daynamic Loading

   자바는 동적 로딩을 지원한다

   따라서 자바는 모든 클래스가 실행 시간에 로딩되지 않고, 필요한 시간에 필요한 클래스만 로딩할 수 있다

<br>

## JVM

JVM은 Java Virtual Machine 즉, 자바 가상 머신(컴퓨터)으로 자바가 실행되는 환경이다.

마치 어느 하드웨어든 윈도우를 설치하면 윈도우를 사용할 수 있듯이,

어느 운영체제든 운영체제에 맞는 JVM을 설치하면 JVM 환경에서 JAVA를 실행할 수 있게 해준다.

<br>

따라서 JVM만 설치되어 있으면, 어디서든 JAVA를 실행할 수 있다.

<br>

## JDK

JDK는 JAVA Development Kit로 JAVA를 개발하기 위한 도구 모음이라고 볼 수 있다.

JDK를 설치하면 JAVA를 비롯한 JVM, JAVA API 등의 JAVA 개발에 필요한 프로그램들이 설치된다.

<br>

## 편집기

JAVA를 개발하기 위해서는 JDK뿐만 아니라 편집기가 추가로 필요하다.

대표적인 편집기로는 Eclipse와 InteliJ가 있다.

<br>

## JAVA의 실행 순서

1. HelloWorld.java 소스 파일 작성
2. javac.exe (컴파일러)로 HelloWorld.class 생성
3. java.exe (인터프리터)로 실행

<br>

## JAVA 기초

- JAVA 애플리케이션(프로그램)은 많은 클래스로 이루어져있다

- JAVA 애플리케이션은 main 메소드를 호출하면서 시작한다

- 따라서 실행하는 애플리케이션의 여러 클래스 중 적어도 하나의 클래스에는 main 메소드가 있어야 한다

- 한 소스파일(.java 파일)에는 한 클래스가 원칙이다 (다만, 여러 클래스를 정의하는 것은 가능하다)

- 소스파일의 이름은 파일 내 정의된 public class 이름과 동일해야 한다 (없으면 어떤 이름이든 상관없다)

- 컴파일로 생성되는 클래스파일(.class 파일)은 클래스마다 만들어진다

  - 즉, 한 소스파일에 여러 클래스가 정의되어 있는 경우, 컴파일 시 다수의 클래스 파일이 생성된다

  - 따라서 한 소스파일에 한 클래스를 정의하는 것이 관리하기 편하다

### main 메소드가 두 개 이상 있으면?

JAVA는 오버로딩을 지원하기 때문에 하나의 클래스에 두 개 이상의 main메소드를 생성할 수 있다.

하지만, 정해진 규칙에 따라 java.exe는 **public static void main(Strings[] args)**를 실행한다.

<br>

## 주석

주석은 프로그램을 실행할 때 아무런 영향을 미치지 않는 부분으로, 개발을 하면서 필요한 것들을 메모할 때 사용한다.

예를 들어 소스 파일 별, 생성자, 생성 날짜 및 목적 등을 적거나, 수정 사항에 대해 기록할 수 있다.

```JAVA
/*
Date : 2022-03-06
Author : CodeJin19
*/

class HelloWorld {
    public static void main (Strings[] args) {
        System.out.println("안녕하세요"); //Hello, World에서 한글로 수정 22.03.06
    }
}
```

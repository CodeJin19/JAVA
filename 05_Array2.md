# Array2

## 목차

[String 배열](#String-배열)

[char 배열과 String 클래스](#char-배열과-String-클래스)

[다차원 배열](#다차원-배열)

[다차원 배열의 초기화](#다차원-배열의-초기화)

<br>

## String 배열

String 배열의 선언, 생성 역시, 기존 배열의 선언, 생성과 동일하게 할 수 있다.

```java
//String 배열의 선언
String[] 배열이름;
String 배열이름[];
```

```java
//String 배열의 생성
String[] 배열이름 = new String[5];
String 배열이름[] = new String[5];
```

<br>

## char 배열과 String 클래스

문자열, 즉 char 배열은 자주 쓰이다 보니, 각종 기능(메서드)을 추가한 클래스가 String이다.

> 클래스란, 데이터와 데이터를 다루는 각종 함수(매서드)를 묶은 객체다.

> 매서드란, 클래스 데이터를 다루기 위해 구현한 함수로, JAVA에서는 매서드라고 부른다.

<br>

다름은 String의 주요 매서드다.

| 매서드                     | 설명                                                            |
| -------------------------- | --------------------------------------------------------------- |
| char charAt(int index)     | String(즉, char 배열)의 index 위치에 있는 문자(char)를 반환한다 |
| int length()               | String(즉, char 배열)의 길이를 반환한다                         |
| boolean equals(Object obj) | String(즉, char 배열)과 obj를 비교한다                          |

<br>

## 다차원 배열

다차원 배열을 생성하는 방법은 간단하다.

[]를 추가하면 배열의 차원이 늘어난다.

```java
int[][] arr2 = new int[5][5]; //5x5 2차원 배열 생성
int[][][] arr3 = new int[3][3][3]; //3x3x3 3차원 배열 생성
```

<br>

## 다차원 배열의 초기화

다차원 배열의 초기화는 다음과 같다.

```java
int[][] arr2 = new int[][] {{1, 2, 3}, {4, 5, 6}};
```

혹은 다음과 같이 작성할 수 있다.

```java
int[][] arr2 = new int[][] {
                                {1, 2, 3},
                                {4, 5, 6}
                            };
```

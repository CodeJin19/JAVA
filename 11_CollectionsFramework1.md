# Collections Framework1

## 목차

[Collections Framework](#Collections-Framework)

[ArrayList](#ArrayList)

[LinkedList](#LinkedList)

<br>

## Collections Framework

JAVA에는 다량의 데이터를 다루는 표준화된 클래스들가 제공된다.

이들은 collections framework에 있으며, 크게 List, Set, Map 3가지로 분류할 수 있다.

1. List

   - 순서가 있는 데이터 집합, 중복 허용
   - ArrayList, LinkedList, Stack 등

2. Set

   - 순서가 없는 데이터 집합, 중복 허용 X
   - HashSet 등

3. Map
   - Key와 Value로 이루어진 데이터 집합, Key는 중복 허용 X, Value는 중복 허용
   - HashMap 등

<br>

## ArrayList

ArrayList는 배열(Array)보다 좀 더 유연한, 확장된, 클래스다.

사이즈가 고정적인 배열과 달리, 데이터 추가가 가능하며, 배열과 마찬가지로 순서를 저장하고, 중복이 허용된다.

대신, 데이터의 추가는 배열의 마지막에만 가능하다.

<br>

## LinkedList

항상 마지막에 데이터를 추가할 수 있는 ArrayList와는 달리, 가운데에 데이터를 삽입할 수 있는 클래스다.

정리하자면 아래와 같다.

<br>

| 컬렉션     | 순차적 데이터 추가/삭제 | 임의의 위치 데이터 추가 삭제 | 임의의 위치 데이터 접근 속도 |
| ---------- | ----------------------- | ---------------------------- | ---------------------------- |
| ArrayList  | 빠름                    | 느림                         | 빠름                         |
| LinkedList | 느림                    | 빠름                         | 느림                         |

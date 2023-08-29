# Collections Framework1

## 목차

[Collections Framework](#Collections-Framework)

[ArrayList](#ArrayList)

[LinkedList](#LinkedList)

[Deque](#Deque)

[Iterator](#Iterator)

[Arrays](#Arrays)

[Comparator and Comparable](#Comparator-and-Comparable)

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

<br>

## Deque

Deque는 Double-Ended Queue로,

head로 데이터를 삽입하고, tail로 데이터를 제거하는 queue와는 달리,

head와 tail, 양 끝에서 데이터의 삽입과 제거가 가능한 queue다.

<br>

| Stack | Queue | Deque     |
| ----- | ----- | --------- |
| push  | offer | offerLast |
| pop   | -     | pollLast  |
| -     | poll  | pollFirst |
| -     | peek  | peekFirst |
| peek  | -     | peekLast  |

<br>

<br>

## Iterator

Iterator는 collection에 저장된 요소에 접근하는데 사용하는 인터페이스다.

아래와 같이 collection 인터페이스에는 Iterator를 반환하는 iterator()가 정의되어 있다.

```JAVA
public interface Iterator {
   boolean hasNext();
   Object next();
   void remove();
}

public interface Collection {
   ...
   public Iterator iterator();
   ...
}
```

iterator 메서드는 collection 인터페이스에 정의되어 있으므로, collection의 자손 클래스에 구현되어있다.

따라서 collection의 모든 자손 클래스에서 iterator 메서드로 적절한 Iterator 인스턴스를 만들어 각 collection의 요소에 접근할 수 있다.

<br>

## Arrays

<br>

### fill()

배열을 특정 값으로 채운다.

```JAVA
int[] arr = new int[5];
Arrays.fill(arr, 1); //arr = [1, 1, 1, 1, 1]
```

<br>

### sort()

배열을 오름차순으로 정렬한다.

```JAVA
int[] arr = {4, 2, 3, 1, 5}
Arrays.sort(arr) //arr = [1, 2, 3, 4, 5]
```

<br>

### toString()

배열의 내용을 문자열로 변환한다.

1차원 배열에만 사용할 수 있다.

```JAVA
int[] arr = {4, 2, 3, 1, 5}
System.out.println(Arrays.toString(arr)) // [4, 2, 3, 1, 5]
```

<br>

### equals()

두 배열이 같은지 비교한다.

마찬가지로 1차원 배열에만 사용할 수 있다.

```JAVA
int[] arr1 = {4, 2, 3, 1, 5}
int[] arr2 = {1, 2, 3, 4, 5}

System.out.println(Arrays.equals(arr1, arr2)) // true
```

<br>

## Comparator and Comparable

배열을 오름차순으로 정렬할 때 Arrays.sort()를 사용하였지만, sort 메서드를 사용하기 위해서는 Comparator 또는 Comparable 인터페이스에 필요한 메서드가 정의되어야 한다.

```JAVA
public interface Comparator {
   int compare(Object o1, Object o2)
}

public interface Comparable {
   public int CompareTo(Object o);
}
```

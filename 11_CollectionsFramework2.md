# Collections Framework2

## 목차

[Iterator](#Iterator)

[Arrays](#Arrays)

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

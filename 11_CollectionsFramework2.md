# Collections Framework2

## 목차

[Iterator](#Iterator)

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

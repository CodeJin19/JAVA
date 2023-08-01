# Format Class1

## 목차

[Decimal Format](#Decimal-Format)

<br>

## Decimal Format

숫자를 일정한 형식의 String으로 변환해주는 클래스로, java.text패키지에 있다.

```java
import java.text.*;

class FormatClass{
    public static void main(String args[]) {
        double n = 123456.789;
        DecimalFormat df = new DecimalFormat("#.##");
        System.out.printf("%s", df.format(n)); //123456.79
    }
}
```

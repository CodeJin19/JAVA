# java.lang Package

## 목차

[Obejct](#Object)

[equals](#equals)

[toString](#toString)

<br>

## Object

Object 클래스에는 유용한 클래스 메서드가 여럿 있다.

특히 Object 클래스는 모든 객체의 조상인만큼, 모든 객체에서 활용가능하니 유용한 클래스 메서드를 정리해보자.

<br>

## equals

equals는 두 객체의 참조변수를 비교하여 같으면 true를, 다르면 false를 반환한다.

여기서 중요한 점은 두 객체의 값이 아니라, 참조변수를 비교한다는 점이다.

바꿔말하면, 객체의 값이 같다고 해서 equals가 참이다는 보장이 없다.

<br>

_하지만, String클래스의 경우 equals 메서드를 오버라이딩하여 String 객체의 문자열을 비교하게끔 변경했다._

<br>

## toString

toString은 인스턴스에 대한 정보를 출력하는 메서드다.

기본적으로는 클래스 이름과 해시값이 출력되지만, String, Date 등의 클래스에서는 오버라이딩을 통해 보다 유용한 정보만 출력되게끔 되어있다.

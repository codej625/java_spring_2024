# 자바에서 equals() 메서드와 == 연산자의 차이

<br /><br />

* 비교 연산자(와 메서드)
---

1. equals()
```
equals() 메서드는 객체의 내용(데이터)를 비교한다.

equals() 메서드가 상속되어 오버라이드되지 않는다면,
기본적으로 ==와 같은 참조(레퍼런스) 비교를 수행한다.
보통 클래스에서 equals() 메서드를 오버라이드하여 두 객체의 내용을 비교하도록 재정의한다.
```

<br />

2. ==
```
== 연산자는 객체의 레퍼런스(메모리 위치)를 비교한다.

두 객체가 동일한 메모리 위치를 가리키는 경우에만 true를 반환한다.
기본 자료형의 경우에는 값을 비교한다.
```

<br /><br /><br />

* 예시
---

```
객체의 내용이 동일한지를 비교하고자 할 때는 equals() 메서드를 사용하는 것이 일반적으로 바람직하다.
== 연산자는 두 객체가 정확히 같은 객체를 참조하는지를 확인할 때 사용된다.
예를 들어, 문자열 비교에는 equals() 메서드를 사용하는 것이 권장된다.
```

<br />

```java
String str1 = new String("hello");
String str2 = new String("hello");

/* equals 메서드를 사용한 문자열 비교 */
if (str1.equals(str2)) {
  System.out.println("같은 문자열");
}

/* == 연산자를 사용한 레퍼런스 비교 */
if (str1 == str2) {
  System.out.println("같은 레퍼런스");
}
```
```
위 예제에서 equals() 메서드는 두 문자열의 내용을 비교하므로 "같은 문자열"을 출력한다.
반면에 == 연산자는 두 문자열이 서로 다른 객체를 참조하므로 "같은 레퍼런스"를 출력하지 않는다.
```

<br /><br />

```
* Tip

"call by value"와 "call by reference"는 메서드 호출 시 매개변수를 전달하는 방식을 나타내는데,
이 두 용어는 프로그래밍 언어에서 주로 사용되며, 자바에서는 메서드 호출 시 "call by value"가 사용된다.

메서드에 매개변수로 전달되는 것은 값의 복사본이다.
따라서 메서드 내에서 매개변수의 값이 변경되어도 호출자에게는 영향을 주지 않는다.

자바에서는 모든 기본 자료형과 객체의 레퍼런스가 전달될 때 값에 의한 호출(call by value)이 발생한다.
이때 객체의 레퍼런스를 값으로 복사하여 메서드에 전달하게 되는데,
이는 객체의 실제 인스턴스가 복사되는 것이 아니라 참조 값만 복사되는 것을 의미한다.
```

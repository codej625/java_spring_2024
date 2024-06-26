# 접근 제한자에 대해 알아보자.

<br /><br />

* 접근 제한자(Access Modifier).
---

```
접근 제한자는 클래스, 인터페이스, 메서드, 변수 등의 멤버에 대한 접근 권한을 제어하는 데 사용.
코드의 가시성과 보안을 강화하고,
클래스와 메서드를 캡슐화하여 잘못된 사용을 방지한다.
주로 적절한 접근 제한자를 선택하여 코드를 보호하고 외부로부터 의도하지 않은 접근을 차단하는 데 사용된다.
```

<br /><br /><br />

* 종류
---

| 접근 제한자        | 설명                                            |
|-------------------|-------------------------------------------------|
| public            | 해당 멤버에 대한 접근이 제한되지 않는다. 어떤 패키지에 속한 클래스든 사용할 수 있다. |
| protected         | 같은 패키지에 속한 클래스 또는 해당 클래스를 상속받은 클래스에서만 접근할 수 있다. |
| default           | 접근 제한자를 명시하지 않은 경우의 기본값. 같은 패키지에 속한 클래스에서만 접근할 수 있다. |
| private           | 해당 클래스 내에서만 접근할 수 있다. 다른 클래스에서는 접근할 수 없다. |

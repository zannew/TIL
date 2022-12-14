# static 블럭

## 👀️ static 블럭이란?

- 초기화 블럭(Initialization Block)이라고도 불린다.
- 작성 형식은 다음과 같다.

```java
public class ExampleClass {

		/* 클래스 초기화 블럭 */
		static {
				//실행할 코드
		}

}
```

- 클래스가 스태틱 영역에서 공간을 할당받을 때 실행된다. 이 말인즉슨 해당 클래스 또는 패키지가 처음으로 사용될 때 로딩될 때 실행된다는 것을 의미한다.
- 프로그램 실행 시 모든 클래스의 정보가 로드되지 않는 이유는 스태틱 영역도 메모리의 일부이기 때문이다.
  - 메모리를 최대한 늦게 사용하고 최대한 빠르게 반납하는 것이 정석이다.
- 클래스가 가장 처음 사용될 때의 케이스를 정리하자면 다음과 같다.
  1. 클래스의 정적 속성을 사용할 때
  2. 클래스의 정적 메서드를 사용할 때
  3. 클래스의 인스턴스를 생성할 때
- `ExamplaClass.java` 로 여러 인스턴스를 생성하더라도 static 블럭은 한 번만 실행된다.
- `ExamplaClass.java` 의 생성자를 호출하지 않더라도 클래스에 대한 참조가 발생하면 실행된다.
- static 블럭은 작성된 순서를 따라서 실행된다.
  - static 블럭 내에서 또는 여러 static 블럭이 존재하더라도 작성된 순서를 따른다.
- 클래스 변수의 초기화가 복잡한 경우 주로 사용된다.

<br>

## 👀️ (번외) 인스턴스 초기화 블럭

- 인스턴스 초기화 블럭은 잘 사용되지 않는다.
- 대신 인스턴스 변수 초기화는 주로 생성자를 이용한다.
- 모든 생성자에서 공통으로 실행되어야하는 코드가 있다면 생성자에 넣지 않고 인스턴스 초기화 쁠럭에 넣어 코드의 중복을 줄인다.
- 작성 형식은 다음과 같다.

```java
public class ExampleClass {

		/* 인스턴스 초기화 블럭 */
		{
				// 생성자 호출 시 공통으로 실행할 코드
		}

}
```

- 인스턴스 초기화 블럭 내 코드는 인스턴스가 생성될 때마다 실행된다.

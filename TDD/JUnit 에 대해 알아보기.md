# JUnit 에 대해 알아보기

<br>

# 👀️ JUnit 이란?

- Java에서 독립된 단위테스트(Unit Test)를 지원하는 테스트용 프레임워크이다.
- assert 메서드로 테스트 케이스의 수행 결과를 판별한다.
- JUnit4부터 테스트를 지원하는 여러 어노테이션을 제공하기 시작했다.
- @Test 메서드가 호출될 때마다 새로운 인스턴스를 생성하고 독립적인 테스트를 수행한다.
- 테스트 결과 외에 최적화된 코드를 유추해내는 기능도 제공한다.
- 문서를 대체할만한 히스토리를 소스상에서 표현할 수 있다.

<br><br>

# 👀️ 지원하는 어노테이션

### @Test

- 이 어노테이션이 선언된 메서드는 테스트를 수행하는 메서드가 된다.
- JUnit은 각각 테스트가 서로 영향을 주지 않고 독립적으로 실행되게 한다.
- @Test 어노테이션 마다 객체를 생성한다.

### @**Ignore**

- 이 어노테이션이 선언된 메서드는 실행하지 않는다.

### @**Before**

- @Test 메서드가 실행되기 전에 반드시 실행된다.
- @Test 메서드에서 공통으로 사용하는 코드를 @Before 메서드에 선언하여 사용한다.

### @**After**

- @After가 선언된 메서드는 @Test 메서드 실행된 후 수행한다.

### @**BeforeClass**

- @BeforeClass 어노테이션은 @Test 메서드보다 먼저 한번만 수행되어야할 경우에 사용한다.

### @**AfterClass**

- @AfterClass 어노테이션은 @Test 메서드보다 나중에 한번만 수행되어야할 경우에 사용한다.

### @**Disabled**

- 해당 테스트는 무시된다.

### @**BeforeEach**

- 모든 테스트 메서드가 수행되기 이전에 실행하는 메서드이다.

### @**AfterEach**

- 모든 테스트 메서드가 수행된 후 실행하는 메서드이다.

### @**BeforeAll**

- 모든 테스트 클래스를 초기화할 때 딱 한번만 수행하는 메서드이다.
- 이 어노테이션을 포함한 메서드는 `static`으로 선언해야 한다.

### @**AfterAll**

- 테스트 클래스 내 모든 메서드를 실행시킨 후 딱 한번 수행하게 된다.

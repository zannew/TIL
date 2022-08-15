# 어댑터 패턴 (Adapter Pattern)



- 기존 코드를 클라이언트가 사용하는 인터페이스의 구현체로 바꿔주는 패턴
- 가장 좋은 예시는 110v → 220v 로의 변환
- 패턴의 구성  요소
    - 타겟이 되는 인터페이스만을 사용하는 클라이언트
    - Adaptee에 해당하는 구현체 클래스
    - 클라이언트와 구현체를 연결해주는 Adapter 클래스

- 장점
    - 기존 코드 변경 없이  인터페이스 구현체를 만들어 재사용할 수 있다.
    - 기존 코드가 하던 일과 특정 인터페이스 구현체로 변환하는 작업을 각기 다른 클래스(어댑터)로 분리하여 관리할 수 있다.
- 단점
    - 새로운 클래스가 생겨 복잡도가 증가할 수 있다.
    - 기존 코드에서 해당 인터페이스를 구현하도록 수정하는 것이 좋은 선택일 수 있다.

- 사용된 예시
    - 자바
        - java.util.Arrays#asList(T...)
        - java.util.Collections#list(Enumeration), java.util.Collections#enumeration()
        - java.io.InputStreamReader(InputStream)
        - java.io.OutputStreamWriter(OutputStream)
    - 스프링
        - HandlerAdapter : 우리가 작성하는 다양한 형태의 핸들러 코드를 스프링 MVC가 실행할 수 있
          는 형태로 변환해주는 어댑터용 인터페이스.
        ****

```java
참고
- 코딩으로 학습하는 GoF의 디자인 패턴 by 백기선
```
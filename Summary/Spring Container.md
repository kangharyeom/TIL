# Summary 2022.11.14

# 스프링 컨테이너(Spring Container)는 무엇일까?

스프링 컨테이너(Spring Container)는 Spring Framework의 핵심 컴포넌트입니다.
내부에 또 다른 컴포넌트를 가지고 있는 어떤 컴포넌트를 의미합니다.
또한, Spring Container는 내부에 존재하는 Application Bean의 생명주기를 관리합니다.

Spring Container는 XML, 애너테이션 기반의 자바 클래스로 만들 수 있으며,
Bean의 인스턴스화, 구성, 전체 생명주기 및 제거까지 처리합니다.
또한, 의존성 주입을 통해 애플리케이션의 컴포넌트를 관리합니다.
 - Spring Container는 서로다른 Bean을 연결하는 역할을 합니다. 

Spring Container를 사용하는 이유
1. 객체 의존도를 낮추기 위해서
2. Spring Container를 통해서 구현클래스의 의존을 제거하고 인터페이스에만 의존하도록 설계할 수 있습니다.


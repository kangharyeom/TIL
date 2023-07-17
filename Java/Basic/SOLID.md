# SOLID (객체 지향 설계)란 무엇일까?!

SOLID란 로버트 마틴이 제시한 OOP설계의 다섯가지 기본 원칙이다.
프로그래머가 유지 보수 확장이 쉬운 프로그래밍을 할 때 이 원칙을 적용할 수 있다.
읽기 쉬운 소스코드를 위하여 리팩토링 할 때 고려하는 중요한 원칙이기도 하다.

# SRP (Single Responsibility Principle)
단일 책임 원칙
- 한 클래스는 하나의 책임만 갖는다.

# OCP (Open-Close Principle)
개방-폐쇄 원칙
- 소프트웨어 요소는 확장에는 열려있으나, 변경에는 닫혀있어야 한다.

# LSP (Liskov Substitution Principle)
리스코프 치환 원칙
- 프로그램의 객체는 프로그램의 정확성을 깨뜨리지 않으면서
  하위 타입의 인스턴스로 바꿀 수 있어야 한다.

# ISP (Interface Segregation Principle)
인터페이스 분리 원칙
- 특정 클라이언트를 위한 인터페이스 여러개가
  범용 인터페이스 하나보다 낫다.

# DIP (Dependency Inversion Principle)
의존관계 역전 원칙
- 프로그래머는 추상화에 의존해야지 구체화에 의존하면 안된다.
# JPA (Java Persistence API)란 무엇일까?
JPA는 영속성을 가지는 자바 애플리 케이션이다. 
즉, JPA는 인메모리에 저장하여 종료하면 사라지는 데이터가 아닌, 
종료가 되어도 계속해서 저장되어 있는 데이터이다.

JPA는 기술 명세서다.
JPA는 왜 EntityManager를 활용한 기술이라고 하면서 정작 Repository 인터페이스를 주로 사용하는 것인가?
막상 JPA를 열어보면 JPA는 interface, enum, Exception을 비롯한 Annotation으로 이루어져있다는 것을 알 수 있다.
특히, EntityManager는 javax.persistence.EntityManager에 interface로 정의되어 있다.

# Hibernate와의 연관성
Hibernate는 JPA의 구현체이다. 구현체는 "인터페이스를 구현한 클래스"라는 뜻이니, HIbernate는 JPA의 구현 클래스가 되는 것이다. 
물론 구현체는 Hibernate외 에도 DataNucleus, EclipseLink 등 다양하게 있다. 

![img.png](../images/JPA/JPA에%20대한%20고찰/img.png)

Hibernate에서는 interface들을 상속받고 Impl로 구현하고 있다.

![img_1.png](../images/JPA/JPA에%20대한%20고찰/img_1.png)
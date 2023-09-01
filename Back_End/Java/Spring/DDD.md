# DDD(Domain Driven Design)란? 

도메인 위주의 설계 기법을 의미한다.

도메인(Domain)이란?
- 비즈니스적인 어떤 업무 영역을 의미한다.
ex)배달앱의 업무 도메인은 => 회원, 주문, 음식, 배달, 결제 등이 있을 수 있다.

애그리거트(Aggregate)란?
- 비슷한 범주의 연관된 업무들을 하나로 그룹화 해놓은 그룹을 의미한다.
- 따라서 주문 시스템 도메인의 배달 주문자 정보, 배달 음식 정보, 주문 정보, 배달 주소정보 등의 정보들을 모두 모아 주문 애그리거트라고 부른다. 

애그리거트 루트(Aggregate Root)란?
-  애그리거트를 대표하는 도메인을 DDD에서는 애그리거트 루트(Aggregate Root)라고 한다.
- 즉, 집단의 대표 / ex) 주문 애그리거트의 애그리거트 루트는 '주문 정보'이다.  
- 애그리거트 루트는 부모 테이블이 되고, 나머지는 자식 테이블이 되는 것이다.
- 부모 테이블의 기본키를 자식 테이블이 가지고 있다면 그것을 외래키라고 부른다.
# @Column

1. name 
- 필드와 매핑할 테이블의 컬럼 이름 객체의 필드 이름

2. insertable, updatable 
- 등록, 변경 가능 여부 TRUE

3. nullable(DDL) 
- null 값의 허용 여부를 설정한다. false로 설정하면 DDL 생성 시에 not null 제약조건이 붙는다.

4. unique(DDL) 
- @Table의 uniqueConstraints와 같지만 한 컬럼에 간단히 유니크 제약조건을 걸 때 사용한다.

5. columnDefinition(DDL)
- 데이터베이스 컬럼 정보를 직접 줄 수 있다. ex) varchar(100) default ‘EMPTY' / 필드의 자바 타입과 방언 정보를 사용해서 적절한 컬럼 타입 

6. length(DDL) 
- 문자 길이 제약조건, String 타입에만 사용한다. 255

7. precision, scale(DDL)
- BigDecimal 타입에서 사용한다(BigInteger도 사용할 수 있다). precision은 소수점을 포함한 전체 자 릿수를, scale은 소수의 자릿수다. 참고로 double, float 타입에는 적용되지 않는다. 아주 큰 숫자나 정밀한 소수를 다루어야 할 때만 사용한다.
precision=19, scale=2 

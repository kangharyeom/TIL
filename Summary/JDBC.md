# Summary 2022.11.22 update

# JDBC(Java Database Connectivity)란 무엇일까?

JDBC(Java Database Connectivity)는 Java 기반 애플리케이션의 코드 레벨에서 사용하는 데이터를 데이터베이스에 저장 및 업데이트 하거나
반대로 데이터베이스에 저장된 데이터를 Java 코드 레벨에서 사용할 수 있도록 해주는 Java에서 제공하는 표준 사양(또는 명세, Specification)이다.

Java 개발자는 JDBC API를 사용해서 다양한 벤더(Oracle, MS SQL, MySQL 등)의 데이터베이스와 연동할 수 있다.

# JDBC의 동작 흐름

Java 애플리케이션 => JDBC API => JDBC드라이버 => 데이터베이스에 액세스

JDBC드라이버란?
- JDBC 드라이버는 데이터베이스와의 통신을 담당하는 인터페이스이다.
- Oracle이나 MS SQL, MySQL 같은 벤더가 해당 벤더에 맞는 JDBC 드라이버를 구현해서 제공한다.
- JDBC 드라이버의 구현체를 이용해서 특정 벤더의 데이터베이스에 액세스 할 수 있다.

# JDBC API 사용 흐름

1. JDBC 드라이버 로딩
- JDBC 드라이버는 DriverManager라는 클래스를 통해서 로딩된다.

2. Connection 객체 생성
- JDBC 드라이버가 정상적으로 로딩되면 DriverManager를 통해 데이터베이스와 연결되는 세션(Session)인 Connection 객체를 생성한다.

3. Statement 객체 생성
- Statement 객체는 작성된 SQL 쿼리문을 실행하기 위한 객체로써 객체 생성 후에 정적인 SQL 쿼리 문자열을 입력으로 가진다.

4. Query 실행
- 생성된 Statement 객체를 이용해서 입력한 SQL 쿼리를 실행한다.

5. ResultSet 객체로부터 데이터 조회
- 실행된 SQL 쿼리문에 대한 결과 데이터 셋

6. ResultSet 객체 Close, Statement 객체 Close, Connection 객체 Close
- JDBC API를 통해 사용된 객체들은 사용 이후에 사용한 순서의 역순으로 차례로 Close를 해준다.

# Connection Pool이란?

JDBC API를 사용해서 데이터베이스와의 연결을 위한 Connection 객체를 생성하는 작업은 비용이 많이 드는 작업이기 때문이다.

그러므로,
애플리케이션 로딩 시점에 Connection 객체를 미리 생성해두고 애플리케이션에서 데이터베이스에 연결이 필요한 경우
Connection 객체를 새로 생성하는 것이 아니라 미리 만들어 둔 Connection 객체를 사용하여 애플리케이션의 성능을 향상 시킬 수 있다.

따라서, 데이터베이스 Connection을 미리 만들어서 보관하고 애플리케이션이 필요할 때 이 Connection을 제공해주는 역할을 하는 Connection 관리자를 바로 Connection Pool이라고 한다.
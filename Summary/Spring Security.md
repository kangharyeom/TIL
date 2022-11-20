# Summary 2022.11.18

Spring Security란 무엇일까요?!


Spring Security는 Spring MVC 기반 애플리케이션의 인증(Authentication)과 인가(Authorization or 권한 부여) 기능을 지원하는 보안 프레임워크입니다.

스프링에서는 자체적으로 Interceptor나 Servlet Filter 통해 보안 기능을 구현할 수 있지만 웹 애플리케이션 보안의 대부분 기능을 Spring Security에서 안정적으로 지원하고 있습니다.



Spring Security의 기능은 다음과 같습니다.

폼 로그인 인증, 토큰 기반 인증, OAuth 2 기반 인증, LDAP 인증의 사용자 인증 기능 적용
애플리케이션 사용자의 역할(Role)에 따른 권한 레벨 적용
애플리케이션에서 제공하는 리소스에 대한 접근 제어
민감한 정보에 대한 데이터 암호화
SSL 적용 및 웹 보안 공격 차단


Spring Security 용어정리


Principal(주체)
애플리케이션에서 작업을 수행하는 사용자, 디바이스 또는 시스템 등을 뜻하며, 일반적으로 인증 프로세스가 성공적으로 수행된 사용자의 계정 정보를 의미합니다.
Authentication(인증)
애플리케이션 사용자가 본인이 맞음을 인증하는 절차
Credential = 신원 증명 정보 => 사용자 식별을 위한 정보 (ex: 주민등록증, 로그인의 비밀번호)
Authorization(인가 또는 권한 부여)
Authentication이 수행된 사용자에게 하나 이상의 권한(authority)을 부여하여 특정 애플리케이션의 특정 리소스에 접근할 수 있게 허가하는 과정을 의미합니다.
권한은 일반적으로 역할(Role)형태로 부여됩니다.
Access Control(접근 제어)
사용자가 애플리케이션의 리소스에 접근하는 행위를 제어하는 것을 의미합니다.

Deprecated의 의미 // 중요도가 떨어져 앞으로 사라지게 될 것이라는 의미
 - withDefaultPasswordEncoder() 메서드의 Deprecated는 특이하게도 향후 버전에서 제거됨을 의미하기 보다는 Production 환경에서 인증을 위한 사용자 정보를 고정해서 사용하지 말라는 경고의 의미를 나타내고 있습니다. 
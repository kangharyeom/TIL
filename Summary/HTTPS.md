# Summary 2022.11.17

# HTTPS란 무엇일까?

HTTP + S (secure)
(Hyper Text Transfer Protocol Secure Socket layer)
= HTTP over SSL(TLS) 
= HTTP over Secure
=> 클라이언트와 서버사이의 정보를 인증하는 단계를 거침

1. HTTPS 프로토콜의 특징
비대칭키 암호화 => 전혀 다른키 한쌍으로 암호화 및 복호화를 한다. (하나는 비밀로 숨겨두고 다른 하나는 클라이언트에 공개)

2. HTTPS연결 성립 과정
- 클라이언트 -> 서버(공개키, 인증서 정보 전달) // handshake 
- 키 제작용 랜덤 스트링 전송(to Server) -> 키 제작용 랜덤 스트링 전송(to Client) // 비밀 키 생성 
- 세션 키로 암호화 된 메세지 전달 (to Server) -> 세션 키로 암호화 된 메세지 전달 (to Client) // 상호 키 검증

3. CA(Certificate Authority) // 공인 인증서 발급 기관

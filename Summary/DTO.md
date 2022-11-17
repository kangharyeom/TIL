# Summary 2022.11.17

DTO(Data Transfer Object)란 무엇일까요?


DTO는 엔터프라이즈 애플리케이션 아키텍처 패턴의 하나로써 데이터를 전송하기 위한 용도쓰이는 객체입니다.

DTO를 사용하게 된다면 코드를 보다 더 간결하게 구성할 수 있으며 
데이터 유효성 검증을 단순화 할 수 있습니다.

즉, 서비스가 커질수록 다양해지고 복잡해지는 클라이언트의 요청 데이터를 하나의 객체로 모두 전달받아 
코드를 간결하게 해주는 역할이 DTO클래스의 역할입니다.

@RestController
@RequestMapping("/v1/members")
public class MemberController {
    @PostMapping
    public ResponseEntity postMember(MemberDto memberDto) {
        return new ResponseEntity<MemberDto>(memberDto, HttpStatus.CREATED);
    }

		...
		...
}

DTO는 @RequestParm을 대신하여 사용하게 됩니다.

또한 DTO 클래스에 유효성 검증 로직을 작성하여 핸들러 메서드의 간결성을 유지할 수 있습니다.
만약 email 변수에 @email 애너테이션을 추가한다면 
클라이언트 요청 데이터에 유효한 이메일 주소가 없는 경우 reject됩니다.

DTO 클래스를 사용하는 가장 큰 목적은 비용이 많이드는 HTTP 요청수를 줄이기 위함입니다.
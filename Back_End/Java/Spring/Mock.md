# Mock이란 무엇일까요?

Mock이란 모조품 또는 흉내내는 것을 뜻합니다.
즉, 프로그래밍에 있어서의 Mock은 테스트를 하기 위한 가짜 객체를 뜻합니다.
이러한 Mock을 단위 테스트나 슬라이스 테스트 등에 사용하는 것을 Mocking이라고 합니다.



1. Mock 객체를 사용하는 이유는 무엇일까?
테스트 단위는 가급적이면 작을수록 좋습니다.
만약 테스트를 내가 만든 프로그램 전체 단위로 진행하게 된다면 매우 비효율적일 것입니다.
따라서, Mock 객체를 활용하여 내가 테스트 하고자 하는 구간만 제한적으로 테스팅 할 수 있습니다.

2. Mockito란 무엇일까요?!
Mockito는 앞선 Mock 객체를 생성하고 동작하게 Mocking해주는 라이브러리 입니다.
Mokito의 기능을 통해 테스트 대상에만 집중하여 테스트를 할 수 있습니다.

3. 애너테이션 소개
@Mockbean
- Mockito를 사용하고 Mock 객체를 생성하고 주입할 수 있습니다.

@Mock 
- 해당 필드의 객체를 Mock 객체로 생성합니다. 
  (@InjectMocks 애너테이션을 추가한 필드에 생성한 Mock객체를 주입한다.)









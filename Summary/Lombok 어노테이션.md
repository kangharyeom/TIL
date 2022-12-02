# lombok 어노테이션 모음

@Getter
접근자를 자동으로 만들어 준다. (get(조회) 기능)

@Setter
설정자를 자동으로 만들어 준다. (post, update(설정, 변경) 기능)

# 생성자 자동 생성

@NoArgsConstructor
- 파라미터가 없는 기본 생성자를 생성

@AllArgsConstructor
-모든 필드 값을 파라미터로 받는 생성자를 만든다. 

@RequiredArgsConstructor
final이나 @NonNull인 필드 값만 파라미터로 받는 생성자를 만든다.

# ToString 메소드 자동 생성

@ToString
- toString()메소드를 자동으로 생성해준다. 

# equals, hashCode 자동 생성

@EqualsAndHashCode 
- 자바 빈을 만들 때 equals와 hashCode 메소드를 자주 오버라이딩 하는데, @EqualsAndHashCode 어노테이션을 사용하면 자동으로 이 메소드를 생성할 수 있다.

@Data
- @Getter, @Setter, @RequiredArgsConstructor, @ToString, @EqualsAndHashCode을 한꺼번에 설정해주는 매우 유용한 어노테이션이다.


1. 문제 인식
![img.png](../images/detached%20persist에러/img.png)
JPA를 활용하여 Coffee 클래스의 엔티티값을 persist하려고 하였는데 다음과 같은 문제 발생하였다.

2. 문제 해결
이유는 CoffeeId의 @GeneratedValue 어노테이션이 Id 값을 생성하는데 
![img_1.png](../images/detached%20persist에러/img_1.png)

다음과 같이 config클래스에서 coffeeId 값을 임의로 설정해주어 발생하게 된 오류다.

따라서 CoffeeId값과 Coffee클래스의 Construct한 CoffeeId를 삭제하면 해결된다.
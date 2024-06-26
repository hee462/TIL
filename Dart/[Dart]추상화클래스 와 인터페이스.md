
> ### 추상클래스
1. 상속의 재료로 사용 되는 클래스  
2. 상세 부분이 미정의 된 클래스
추상클래스는 클래스키워드 앞에서 abstract 를 기술 한다
```dart
abstract class Character{
  String name;
	void attack(Slime slime); //추상메서드 -> 함수의 몸체가 없다.
}
```
추상클래스는 객체 생성이 직접되지 않는다.
다만 `추상메소드를 상속받은 클래스는 객체 생성가능`
그리고 또한 추상메서드는 추상메서드를 `override`해서 실제내용을 구현해야한다.
추상 클래스도 일반적인 클래스처럼 `extends`를 통해 상속하는 것이 일반적입니다.
올바르게 사용했는지 알아보기 위해 is-a 원칙을 사용할 수 있습니다.
`자식 클래스 is a 부모 클래스`가 어색하지 않아야 합니다.

> ###   Interface
1. 모든 메소드는 추상 메소드 여야 한다
2. 필드를 가지지 않는다
기능의 구현이 필요한 것을 묶은 것으로 해당 인터페이스에 대해서
일반클래스에 `implements` 하여 구현하도록 강제하는 것이다.
```dart
abstract interface class Human { //인터페이스의 해당예 class앞에 abstract interface 붙임
	void speak();
}
```
인터페이스의 추상 메소드를 구현하려면 implements를 사용합니다.
extends는 한 클래스, implements는 여러 인터페이스를 받을 수 있습니다.
`자식 클래스 has a 부모 클래스`가 어색하지 않아야 합니다.

> ### 인터페이스의 효과
1. 같은 인터페이스를 구현한 클래스들은 공통 메소드를 구현하고 있음을 보장
2. 어떤 클래스가 인터페이스를 구현하고 있다면, 
적어도 그 인터페이스에 정의된 메소드를 가지고 있다는 것이 보증된다
 단 특징적으로 일반클래스에서 여러 인터페이스를 다중으로 받아서 구현할 수 있다.
extends와 implements 를 동시에 사용 가능
```dart
class Dancer extends Character implements Human
```
![](https://velog.velcdn.com/images/hee462/post/87248aea-3a75-4ca3-abc6-646d67a356c6/image.png)


#### ⭐️한장정리

> ##### 추상클래스
* 자식클래스의 공통적인 속성을 일반화, 추상화 하기 위해 만들어진 클래스
* 추상클래스의 사용을 통해 자식클래스는 부모클래스를 구체화 하고 기능을 확장
* 상속`extends` 키워드를 통해 사용
* 추상 클래스는 `필드와 메소드 모두` 가지고 있음
* 추상클래스가 가진 메소드 중 정의만 존재하고 구현이 되지 않은 메소드를 추상 메소드라고 부른다.
*   @override
ex) void make();{요기에 설명 없음}
* 자식클래스에서 추상클래스를 상속할 때, 추상 메소드를 반드시 구현해야 한다.
* 다중상속 X
> #####  인터페이스
* 일반화, 추상화 가능한 클래스 집합에서 공통적으로 수행 가능한 동작들을 한데 묶은 것
* 인터페이스를 통해 구현체 (구현 클래스) 에서 구현할 동작들을 강제함
* 구현 `implements` 키워드를 통해 사용
* 인터페이스는 `추상메소드`만 가지고 있음, 필드 X
* 추상클래스와 마찬가지로 구현클래스는 추상메소드를 반드시 구현해야함

- 소프트웨어 설계에서 **자주 발생하는 문제를 해결하기 위해 재사용 가능한 해결책을 제공**하는 일종의 템플릿이다. 
- 주로 클래스나 객체 간의 관게를 정의하고, 코드를 구조화하는 방법에 집중한다.

---
### 중요성
- 자주 발생하는 문제에 대한 검증된 해결책을 적용해 코드의 재사용성이 높아진다.
- 디자인 패턴을 사용해 코드를 구조화하면 변경이나 확장이 쉬워져 유지보수성을 향상시킨다.
- 개발자들 간 커뮤니키이션에서 특정 문제와 해결책을 빠르게 이해하고 논의할 수 있어 협업을 촉진시킨다.
- 검증된 해결책이므로 소프트웨어의 안정성과 확장성을 높이는데 도움이 된다.

### 한계
- 디자인 패턴을 남용하면 코드가 지나치게 복잡해지므로 간단한 해결책을 우선 고려하고 필요한 경우에만 디자인 패턴을 사용하는 것이 좋다.
- 단순한 문제를 해결하기 위해 과도한 디자인 패턴을 적용하면 오히려 소프트웨어가 복잡해지고 유지보수가 어려워질 수 있다.

---
### 종류
1. 생성 패턴(Creational Patterns)
	- 싱글톤 패턴(Singleton Pattern)
	- [[팩토리 메소드 패턴(Factory Method Pattern)]]
	- [[추상 팩토리 패턴(Abstract Factory Pattern)]]
	- 빌더 패턴(Builder Pattern)
	- 프로토타입 패턴(Prototype Pattern)
2. 구조 패턴(Structural Patterns)
	- 어댑터 패턴(Adapter Pattern)
	- 데코레이터 패턴(Decorator Pattern)
	- 프록시 패턴(Proxy Pattern)
	- 퍼사드 패턴(Facade Pattern)
	- 컴포지트 패턴(Composite Pattern)
3. 행위 패턴(Behavioral Patterns)
	- 옵저버 패턴(Observer Pattern)
	- 전략 패턴(Strategy Pattern)
	- 상태 패턴(State Pattern)
	- 템플릿 메소드 패턴(Template Method Pattern)
	- 커맨드 패턴(Command Pattern)
	- 메디에이터 패턴(Mediator Pattern)
관련된 **객체 패밀리를 생성하기 위한 인터페이스를 제공**하는 방식으로, 서로 관련된 여러 종류의 객체를 함께 생성하는 경우에 유용하며, 각각 객체 생성 로직을 캡슐화하여 관리한다.

```js
// 기본 팩토리 인터페이스
const AbstractFactory = {
	createUser: () => {
		throw new Error('메소드가 존재하지 않습니다.');
	},
	createPost: () => {
		throw new Error('메소드가 존재하지 않습니다.');
	}
};

// 팩토리 구현
const ConcreateFactory = Object.create(AbstractFactory);
ConcreateFactory.createUser = (data) => ({
	type: 'user',
	id: data.id,
	name: data.name,
});

// 사용처
const user1 = ConcreateFactory.createUser({id: 1, name: 'uha'});
console.log(user1); // {type: 'user', id: 1, name: 'uha'}
```
기본 클래스에서는 객체 생성 메소드를 정의하고, **객체 생성 책임은 서브클래스에 위임해 메소드를 구현해 객체를 생성**하는 방식이다. 생성 방식을 서브클래스에서 커스터마이징할 수 있다는 장점을 가진다.

```js
// 기본 클래스에서 메소드를 정의
const EntityFactory = {
	createUser: () => {
		throw new Error('메소드가 존재하지 않습니다.');
	},
	createPost: () => {
		throw new Error('메소드가 존재하지 않습니다.')
	}
};

// 서브 클래스 구현
const UserFactory = Object.create(EntityFactory);
UserFactory.createUser = (data) => ({
	type: 'user',
	id: data.id,
	name: data.name,
});

const user1 = UserFactory.cerateUser({id: 1, name: 'uha'});
console.log(user1); // {type: 'user', id: 1, name: 'uha'}
```
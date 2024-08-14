**하나의 팩토리 함수(객체 생성 함수)가 여러 종류의 객체를 생성하는 패턴**으로, 팩토리 클래스 또는 함수가 클라이언트 요청에 따라 다양한 타입의 객체를 생성한다.

```js
const createEntity = (type, data) => {
	switch(type) {
		case 'user':
			return {
				type: 'user',
				id: data.id,
				name: data.name,
			};
		case 'post':
			return {
				type: 'post',
				id: data.id,
				title: data.title,
				content: data.content,
			};
		dafault:
			throw new Error('정해지지 않은 타입입니다.')
	}
};

// 사용처
const user1 = createEntity(
	'user',
	{
		id: 1,
		name: 'uha',
	}
);
console.log(user1); // {type: 'user', id: 1, name: 'uha'}
```
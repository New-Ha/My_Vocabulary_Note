> **Controlled** : 세심히 관리(통제/조정)된, 관리하는 | 특정 규칙, 지침 또는 절차에 따라 수행되거나 조작된 경우

외부 상태에 의해 제어 되는 컴포넌트로, 자신의 상태를 직접 관리하지 않고 부모나 외부 상태 관리 라이브러리에서 전달된 값을 사용해 렌더링 되는 컴포넌트를 말한다.

---

예를 들면, `<input>`과 같은 form filed component가 대표적인 제어 컴포넌트인데 외부에서 전달된 값(value), 이벤트 핸들러(onChange, onBlur 등)로 상태를 외부에서 관리하고 조정한다.
- value 속성을 통해 외부에서 입력된 값을 전달 받는다.
- onChange event handler를 통해 입력 값이 변경될 때 부모 컴포넌트로 변경사항을 전달한다.
```js
const [value, setValue] = useState('');

const onChangeHandler = (e) => {
	setValue(e.target.value);
}

return (
	<input
		type="text"
		value={value} // 외부에서 전달된 값으로 상태 제어
		onChange={onChangeHandler} // 외부의 핸들러로 변경 처리
	/>
)
```


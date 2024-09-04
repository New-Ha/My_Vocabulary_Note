특정 동작(이벤트)이 발생했을 때, 그 동작을 처리하는 어떤 함수나 메서드를 호출하도록 연결하는 것을 의미한다.

---
### Ex.
```js
<button onClick={handleClick}>클릭</button>
```
- `onClick={handleClick}` : 이벤트가 발생하면 해당 이벤트가 바인딩된 핸들러 함수가 실행된다.
	- `onClic` : 클릭 이벤트 발생했을 때 실행될 함수를 바인딩하는 속성
	- `handleClikc` : 클릭되면 호출될 핸들러 함수

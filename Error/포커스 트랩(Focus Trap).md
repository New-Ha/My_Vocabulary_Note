🚨 포커스가 특정 영역에 갇혀서 벗어나지 못하는 상황을 말한다.
- 예 ) 모달 창 내부에 포커스가 갇혀 모달을 벗어날 수 없는 상황

📍 인터페이스가 활성화 되었을 때 내부 영역에서만 사용자가 포커스를 이동할 수 있도록 의도적으로 제어하는 데 쓰일 수 있다.

---
### 필요성
1. 모달 창, 대화 상자 같은 요소가 활성화될 때, 사용자가 트랩된 영역 밖으로 나가지 않도록 해 불필요하게 다른 영역으로 포커스를 이동하지 않도록 하여 해당 요소와의 상호작용을 보장
2. 사용자가 인터페이스의 특정 부분에 집중할 수 있도록 하여, 해당 요소와 상호작용을 완료할 때 까지 이동하지 않도록 하여 사용자 경험을 높임
3. 접근성 가이드라인(WCAG) 기준을 준수하기 위해 사용

### 구현시 주의사항
1. 모든 포커스 가능한 요소가 트랩 내에 포함되어 상호작용을 완료할 수 있도록 하여야 한다.
2. 트랩에서 벗어나는 추가적인 상호작용을 고려할 수 있다.
3. 스크린 리더 사용자에게 제대로 작성하는 지 ARIA속성(`aria-modal`, `aria-labelledby` 등)을 사용해 접근성을 보장해야 한다.

---
### Example
```js
// 포커스가 모달 내에서만 순환하도록 하는 함수
function trapFocus(event) {
	if (event.key === 'Tab') {
	    if (event.shiftKey) { 
		    if (document.activeElement === firstFocusableElement) {
			     event.preventDefault();
			    lastFocusableElement.focus();
			} 
		} else { 
			if (document.activeElement === lastFocusableElement) {
				 event.preventDefault();
				 firstFocusableElement.focus(); 
			} 
		} 
	} 
} 

modal.addEventListener('keydown', trapFocus);
```

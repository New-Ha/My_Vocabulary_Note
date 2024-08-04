Layout shift 측정 지표로 웸 페이지의 전체적인 레이아웃 이동을 측정하는 지표이다.

Google의 web vitals 중 하나로, 페이지가 로딩되는 동안 발생하는 레이아웃 이동의 총량을 나타낸다.

---
### 계산
CLS = Σ (impact fraction × distance fraction)
	- Impact Fraction : 레이아웃이 변경된 영역의 화면 비율
	- Distance Fraction : 이동된 거리의 비율

콘텐츠가 이동한 거리와 영향받게 된 화면의 비율을 곱한 값으로 나타낸다.
> CORS(Cross-Origin Resource Sharing)


웹 브라우저 기본 정책은 자바스크립트 코드를 받아온 곳(프론트엔드 서버)에서만 자바스크립트로 추가적인 리소스를 요청할 수 있다.([[SOP(Same-Origin Policy) 정책]])
이때 다른 곳(백엔드 서버)에서 리소스를 받아오려고 할 때, CORS를 설정하지 않으면 발생하는 오류가 CORS Error이다.(SOP 위반으로 인한 오류)

### 해결
다른 Origin에서 리소스를 받아오려면 리소스를 제공하는 서버에서 CORS를 허용하면 된다.


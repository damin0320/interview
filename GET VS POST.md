# GET VS POST

### 1. 공통점 : HTTP 메서드

### 2. 차이점

### 1. GET : 단순 브라우징(제품상세, 필터링, 솔팅 등), R
- Path / Query Prameter로 정보를 전달(얘들은 데이터가 URI에 저장) -> 얘가 HTTP Header에 저장. -> 중간 탈취 가능
- 길이 제한
- 멱등성 : 항상 같은 결과를 내어 줌
- 안정성 : 리소스 데이터 변경하지 않는다.
> GET 백 날 해도 데이터 똑같음

- 캐싱 가능
- 브라우저 저장
- 북마크 설정 가능(즐겨찾기 추가) 

---

### 2. POST : 로그인, 회원가입, 댓글 등... , CUD
- HTTP Body에 저장 -> Json object로
- 길이 제한 없음, 숨길 정보 쓰이는게 좋음.
- 멱등, 안정 모두 할 수 없다.(리소스 변경 가능)
> 한 번 할 때마다 데이터, 결과가 계속 바뀜

- 캐싱 안 됨
- 브라우징 안 됨
- 북마크 안 됨 

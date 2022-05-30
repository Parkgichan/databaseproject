# databaseproject


데이터 베이스 수업 프로젝트

코로나 이슈가 있는 만큼 마스크를 판매하는 프로젝트를 만들어 볼 것이다.
이번에 코로나 확진을 받으면서 너무 힘들었던 만큼 인상에 남아 코로나 관련 물품 상점을 만들도록 하겠습니다.

원래 코로나가 심했어서 하려고했는데 5월부터 거리두기가 아예 사라진 관계로 숙박업소예약시스템으로 변경하도록 하겠습니다!


개체는 고객, 회사, 업주, 숙박시설, 이벤트가 있다.
고객과 회사는 1:n관계
회사와 업주도 1:n관계
업주와 숙박시설도 1:n관계
고객과 숙박시설은 n:m관계
고객과 이벤트는 1:1관계이다.

고객개체에 고객이름, 고객번호, 주소, 이메일, 비밀번호, 주민등록번호, 핸드폰번호 속성이 있다.
이 중 단일 값 속성은 고객이름이 될 수 있고, 다중 값 속성은 핸드폰번호가 될 수 있다.
복합 속성은 주민등록번호에 생년월일이 있다.
이벤트 개체에는 가격 할인율 판매가격이 있다. 이 중 유도속성은 할인율로 인하여 판매가격이 달라지니 판매가격이 유도속성이 된다.





E-R 다이어그램
![화면 캡처 2022-05-23 213515](https://user-images.githubusercontent.com/81346175/169839178-4f17c826-9d13-492f-8e2b-a0c3e8bbada2.png)

릴레이션 스키마
![화면 캡처 2022-05-23 231528](https://user-images.githubusercontent.com/81346175/169839625-75295d65-781c-4b65-90d7-b9d8a3af6b3d.png)

구현
![123](https://user-images.githubusercontent.com/81346175/169840910-18f86964-9ea1-4e5b-9e54-e63d77230b56.png)
![1234](https://user-images.githubusercontent.com/81346175/169840915-6b8522e3-114c-4481-a553-5737bfda940f.png)

![사업장테이블](https://user-images.githubusercontent.com/81346175/170982676-06a3c028-8f22-48aa-8d61-ac823fcd52ac.png)























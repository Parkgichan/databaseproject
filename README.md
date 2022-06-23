# databaseproject


데이터 베이스 수업 프로젝트

코로나 이슈가 있는 만큼 마스크를 판매하는 프로젝트를 만들어 볼 것이다.
이번에 코로나 확진을 받으면서 너무 힘들었던 만큼 인상에 남아 코로나 관련 물품 상점을 만들도록 하겠습니다.

원래 코로나가 심했어서 하려고했는데 5월부터 거리두기가 아예 사라진 관계로 숙박업소예약시스템으로 변경하도록 하겠습니다!


개체는 고객, 회사, 업주, 사업장, 이벤트가 있다.
고객과 회사는 1:n관계
회사와 업주도 1:n관계
업주와 사업장도 1:n관계
고객과 사업장은 n:m관계
고객과 이벤트는 1:1관계이다.

고객개체에 고객이름, 고객번호, 주소, 이메일, 비밀번호, 주민등록번호, 핸드폰번호 속성이 있다.
이 중 단일 값 속성은 고객이름이 될 수 있고, 다중 값 속성은 핸드폰번호가 될 수 있다.
복합 속성은 주민등록번호에 생년월일이 있다.
이벤트 개체에는 가격 할인율 판매가격이 있다. 이 중 유도속성은 할인율로 인하여 판매가격이 달라지니 판매가격이 유도속성이 된다.





E-R 다이어그램 
-----------------------------------------------------------

![화면 캡처 2022-05-23 213515](https://user-images.githubusercontent.com/81346175/169839178-4f17c826-9d13-492f-8e2b-a0c3e8bbada2.png)

릴레이션 스키마 
--------------------------------------------------------
![화면 캡처 2022-05-23 231528](https://user-images.githubusercontent.com/81346175/169839625-75295d65-781c-4b65-90d7-b9d8a3af6b3d.png)

구현 
-------------------------------------------
![123](https://user-images.githubusercontent.com/81346175/169840910-18f86964-9ea1-4e5b-9e54-e63d77230b56.png)
![1234](https://user-images.githubusercontent.com/81346175/169840915-6b8522e3-114c-4481-a553-5737bfda940f.png)

정규화 수행 
------------------------------------------
![정규화개념](https://user-images.githubusercontent.com/81346175/175246435-59607646-5c49-4586-a761-e7bde82f0bc0.png)


사업장 테이블
사업장(사업장이름, 주소,방타입, 방개수,업주번호(FK),요금)
![사업장테이블](https://user-images.githubusercontent.com/81346175/170985509-1c12cdf7-a2d3-4b0e-9439-41c83e8709f7.png)

사업장 테이블 제 1정규형

사업장(사업장이름, 주소,방타입, 방개수,업주번호(FK),요금)
![사업장 테이블 제 1정규형](https://user-images.githubusercontent.com/81346175/170984482-423ee364-f8c5-4d75-aefd-68edbcf77b1b.png)
사업장 테이블에 방타입과 방 개수 요금이 3가지씩 있기때문에 제 1정규화가 안되서 다 나누어 주어서 제 1정규화 만족

사업장 테이블 제 2정규형

사업장(일련번호 사업장 이름, 주소,방타입, 방개수,업주번호(FK),요금)
![사업장 테이블 제 2정규형](https://user-images.githubusercontent.com/81346175/170983141-ea7937fc-dec6-4d7c-a9a8-e9fa036a2637.png)

사업장 테이블 제 3정규형

사업장 정보 (일련번호, 주소,방타입, 방개수, 요금)

![사업장 테이블 제 3정규형](https://user-images.githubusercontent.com/81346175/170984618-0c2799fd-0f9d-4ec7-948d-1e1a5bf5c795.png)

사업장 테이블 제 3정규형

사업장_이름과 위치 (주소, 사업장 이름, 업주번호(FK))

![사업장 테이블 제 3정규형2](https://user-images.githubusercontent.com/81346175/170984171-42eb3e8c-1675-4100-bcf0-045c0e6da374.png)

TABLE 작성 및 DATA 입력
--------------------------------------------------------------
1) 회사

![회사모음](https://user-images.githubusercontent.com/81346175/175235679-7f7c09cf-b291-451f-9463-69c6f2d67637.png)

2) 고객

![고객모음](https://user-images.githubusercontent.com/81346175/175235752-9efea5ae-fd33-40ad-a61f-5aa1221f335f.png)

3) 업주

![업주모음](https://user-images.githubusercontent.com/81346175/175235768-78c25d79-f9eb-4635-b5de-f25a97315c92.png)

4) 사업장 이름과위치

![사업장이름과위치모음](https://user-images.githubusercontent.com/81346175/175235759-0e417aed-3fb2-4ec6-89a0-36469013353d.png)

5) 사업장 정보

![사업장정보모음](https://user-images.githubusercontent.com/81346175/175235760-07c173c3-d980-4774-8889-46599cd1e2cd.png)

6) 이벤트

![이벤트모음](https://user-images.githubusercontent.com/81346175/175235777-41c19e57-b8a4-4119-bfb7-3f91811897ed.png)


7) 예약

![예약모음](https://user-images.githubusercontent.com/81346175/175235772-868e4c87-2838-482c-ab6c-97ac302b7c86.png)

---------------------------------------------------------------------------------------------------
DATA 수정 및 삭제 
------------------------------------------------------------------------------------------------
1) UPDATE문


허나영 고객님의 비밀번호 변경
![화면 캡처 2022-06-23 170755](https://user-images.githubusercontent.com/81346175/175249275-0847b705-3c03-4183-a738-51978337b7e4.png)


2) DELETE문

업주 탈퇴 : 해당 업주가 탈퇴하여 삭제

![delete](https://user-images.githubusercontent.com/81346175/175242190-2f7491e6-b178-4d62-aaa9-b456f9da8050.png)


SQL문을 통한 DATA 검색

- 대전에 있는 업장의 이름과 주소 보여주기
![11](https://user-images.githubusercontent.com/81346175/175242665-37b88a4e-149f-4242-af4b-6af5bd815eab.png)

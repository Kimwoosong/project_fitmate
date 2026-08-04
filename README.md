# 팀 프로젝트 결과물 (핏메이트)
### [AWS EC2 서버 바로가기](http://ec2-54-116-91-111.ap-northeast-2.compute.amazonaws.com/)


### 이 프로젝트는 팀프로젝트에서 개인별 github로 옮긴 프로젝트입니다.
- 팀프로젝트 github : [FitMate(팀)](https://github.com/ydshin727/DDStore](https://github.com/Drag-93/project_fitmate)
</details>

## 팀 프로젝트 개요
- 코로나19 이후 건강 및 자기관리 관심증가
- 운동 인구 증가, 하지만 운동 지속률은 낮음
- 초보자의 정보 부족 및 동기부여 문제
- 헬스장의 회원 관리 및 운영의 어려움

## 프로젝트 주요 기능
- 운동 정보 공유 및 커뮤니티 제공
- 운동 루틴 기록 및 개인 운동 관리
- PT, 헬스장 상품 비교 및 예약, 결제
- FitMate Plus 구독 서비스를 통한 회원 혜택 제공
- 운동과 회원 관리를 통합한 올인원 플랫폼 구축

## 벤치마킹 사이트
- [DASHIN](https://www.dietshin.com/) : 쇼핑몰과 커뮤니티로 나눠져 있는 구조 참고
- [Burn Fit](https://routine.burnfit.io/) : 루틴 생성 구조 참고
- [다짐](https://www.da-gym.co.kr/) : PT, 트레이너 카드 UX, UI 참고
- [짐박스](https://gymboxx.com/) : 헬스장 이용권 UX, UI 참고

<details>
<summary><h2>사용한 기술 스택 & 개발 툴 & API</h2></summary>

<div markdown="1">

<br>

<p align="center">
  <img width="800" alt="기술 스택 1" src="https://github.com/user-attachments/assets/f0a49fed-80b4-4156-ae55-5b4352be4513" />
</p>

<br>

<p align="center">
  <img width="800" alt="기술 스택 2" src="https://github.com/user-attachments/assets/2525ee08-45e8-4ea7-b690-924221c19733" />
</p>

<br>

<p align="center">
  <img width="800" alt="기술 스택 3" src="https://github.com/user-attachments/assets/73c90804-8b9a-40c9-86a7-2223565de1c8" />
</p>

</div>

</details>

## 프로젝트 팀 내 역할
- 회원기능 : Spring Security 및 JWT 기반 인증·인가 구현
- 챗봇기능 : Chatbot FAQ 기능(Komoran 형태소 분석기 활용)
- 파일 저장 기능 공통화 : 공통 파일 DB 관리 & 공통 파일 함수 작성

## 일정표
<img width="1538" height="664" alt="image" src="https://github.com/user-attachments/assets/6a7ad519-6434-4b59-8587-be9d3de3d66a" />

<img width="1540" height="723" alt="image" src="https://github.com/user-attachments/assets/40d0e9a4-4bdb-43f1-b049-536b2ccd2da0" />

## 프로젝트 수행경과 - 김우송(개인)
<img width="1690" height="321" alt="image" src="https://github.com/user-attachments/assets/a31fe014-6f02-491b-a66c-cd618acbbaff" />



## DB 구조
<img width="1706" height="945" alt="image" src="https://github.com/user-attachments/assets/8de32302-be89-4dc5-95e1-ec294afbebb5" />

# 담당 기능
<details><summary>로그인</summary>
<img width="1642" height="711" alt="image" src="https://github.com/user-attachments/assets/6ad629b1-0c9d-4caa-ac0b-1d1f346dc609" />
</details>

<details><summary>회원가입</summary>

- 정규식으로 이메일/비밀번호 형식 검증
- member DB 조회 -> 이메일 중복 체크
- 이메일 중복 체크, 비밀번호 확인기능 실시간 체크
- 조건 통과 시 DB에 회원 정보 저장, 로그인 화면 이동

</details>

<details><summary>로그인</summary>

- member DB 조회 -> 이메일 / 비밀번호 정보 일치 확인
- 일치 시 로그인 진행
- authSlice에 계정 정보 저장
- localStorage에 계정 정보 저장해서 로그인 유지

</details>

<details><summary>개인 페이지</summary>

- 개인정보 조회, 수정, 삭제
- 이메일 수정 시 member DB 조회 -> 이메일 중복 확인
- 이메일 / 비밀번호 변경 시 로그인 화면 이동

</details>

<details><summary>관리자페이지</summary>

- 페이지 접근 시 관리자 권한 없으면 Index페이지로 이동(접근제한)
- 관리자 페이지에 필요한 데이터 전부 미리 불러옴 -> 각 기능 담당자의 slice에서 호출, 데이터를 저장
- 리스트 체크 후 선택 삭제(회원,물품,지점관리) D
- 상세보기 -> 정보 수정, 삭제(회원, 물품) R, U, D
- 이메일정보 수정 시 memberDB 조회 -> 이메일 중복 체크(회원)
- 물품의 이름 정보 수정 시 itemsDB 조회 -> 이름 중복 체크(물품)
- 물품 추가 시 items DB 조회 -> 상품 이름 중복 체크 후 물품 추가(물품추가) C
- 주문관리쪽만 필터링 2개로 분류(주문상태, 배송방법)
- 주문상품(수량) 클릭 -> 상세정보

</details>

# 팀 프로젝트 결과물 (핏메이트)
### [AWS EC2 서버 바로가기](http://ec2-54-116-91-111.ap-northeast-2.compute.amazonaws.com/)


### 이 프로젝트는 팀프로젝트에서 개인별 github로 옮긴 프로젝트입니다.
- 팀프로젝트 github : [FitMate(팀)](https://github.com/Drag-93/project_fitmate)

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

<details>
<summary><h2>일정표</h2></summary>

<div markdown="1">

<br>

<p align="center">
  <img width="800" alt="일정표 이미지 1" src="https://github.com/user-attachments/assets/6a7ad519-6434-4b59-8587-be9d3de3d66a" />
</p>

<br>

<p align="center">
  <img width="800" alt="일정표 이미지 2" src="https://github.com/user-attachments/assets/40d0e9a4-4bdb-43f1-b049-536b2ccd2da0" />
</p>

</div>

</details>

<details>
<summary><h2>개인 일정</h2></summary>

<div markdown="1">

<br>

<p align="center">
  <img width="800" alt="개인 일정 이미지" src="https://github.com/user-attachments/assets/a31fe014-6f02-491b-a66c-cd618acbbaff" />
</p>

</div>

</details>

## DB 구조
<img width="1706" height="945" alt="image" src="https://github.com/user-attachments/assets/8de32302-be89-4dc5-95e1-ec294afbebb5" />
<details>
<summary><h1>담당기능</h1></summary>
<br><br>
<details><summary>로그인</summary>
<img width="1642" height="711" alt="image" src="https://github.com/user-attachments/assets/6ad629b1-0c9d-4caa-ac0b-1d1f346dc609" />
</details>

<details><summary>회원가입</summary>
<img width="1363" height="765" alt="image" src="https://github.com/user-attachments/assets/6f55d244-3ac2-49b0-9ed9-8e24c46f95d2" />

- 정규식으로 이메일/비밀번호 형식 검증
- member DB 조회 -> 이메일 중복 체크
- 이메일 중복 체크, 비밀번호 확인기능 실시간 체크
- 주소찾기 시 팀장님이 만들어두신 KakaoMap 활용 팝업을 이용해 주소를 넣음
- 조건 통과 시 DB에 회원 정보 저장, 로그인 화면 이동

</details>
<details><summary>개인페이지</summary><br>
<details><summary>개인 페이지(서비스 바로가기)</summary>
<img width="1500" height="779" alt="image" src="https://github.com/user-attachments/assets/864a0d42-8623-4022-a56e-07478a9b93ac" />

- 일반 회원 / 트레이너의 페이지를 다르게 설정
- 일반 회원은 <b>/ 주문내역 / FitMate Plus+(구독상품) / PT 관리(회원이 등록한 PT 조회) / 이용권 관리(구독상품 제외 이용권) / 스케줄</b>
- 트레이너는 <b>/ PT예약관리(등록되어있는 회원 조회) / 프로필 관리(PT상품 조회 시 트레이너의 프로필 관리) / 수업일정(등록된 회원들의 예약된 일정 관리)</b>

</details>

<details><summary>개인 페이지-> PT관리 -> 트레이너 정보</summary>
<img width="3552" height="1377" alt="image" src="https://github.com/user-attachments/assets/5aaeebe1-50c3-49fe-aa6e-e6f8e226f9cd" />

- 일반 회원이 PT관리 -> 내 예약내역 중 하나를 클릭할 시 해당 트레이너의 정보 조회 가능
  
</details>

<details><summary>개인 페이지-> PT관리 -> 트레이너 정보</summary>
<img width="3417" height="1443" alt="image" src="https://github.com/user-attachments/assets/93889f45-7c35-4e82-98cc-6678f637e94f" />


- 트레이너가 PT 예역관리 -> PT 수업관리 리스트 중 하나를 클릭할 시 해당 일반 회원의 정보 조회 가능
  
</details>
<details><summary>개인 페이지(상세 프로필 정보)->개인정보 수정(공통)</summary>
<img width="3325" height="1466" alt="image" src="https://github.com/user-attachments/assets/25517cd5-5b82-4cec-8ae4-5868b02ae9d1" />


- 계정 상세정보 조회 가능
- 계정 정보 수정 가능
- 비밀번호 변경은 passwordEncoder를 이용했기에 수정 시 개별 변경 페이지 사용
  
</details>




</details>
<br>
<details><summary>관리자페이지</summary><br>
<details><summary>회원 관리 페이지</summary>
<img width="3038" height="1497" alt="image" src="https://github.com/user-attachments/assets/7a43b29e-956e-40ef-9fe2-25235e6bcf38" />


- 계정 상세정보 조회 가능
- 계정 정보 수정 가능
- 비밀번호 변경은 passwordEncoder를 이용했기에 수정 시 개별 변경 페이지 사용
  
</details>
<details><summary>회원 관리 페이지</summary>
<img width="3650" height="1442" alt="image" src="https://github.com/user-attachments/assets/ba779048-8d16-4b71-b23b-d73d96362000" />


- 계정 상세정보 조회 가능
- 계정 정보 수정 가능
- 비밀번호 변경은 passwordEncoder를 이용했기에 수정 시 개별 변경 페이지 사용
  
</details>


</details>
<br>
</details>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

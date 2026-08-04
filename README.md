# 팀 프로젝트 결과물 (핏메이트)
# [AWS EC2 서버 바로가기](http://ec2-54-116-91-111.ap-northeast-2.compute.amazonaws.com/)


### 이 프로젝트는 팀프로젝트에서 개인별 github로 옮긴 프로젝트입니다.
- 팀프로젝트 github : [FitMate(팀)](https://github.com/ydshin727/DDStore](https://github.com/Drag-93/project_fitmate)
</details>

## 팀 프로젝트 개요
- 국내 펫 푸드 시장을 겨냥한 **반려견** 유저만을 위한 쇼핑몰 사이트

## 활용 장비 및 기술 스택
- Frontend : <img src="https://img.shields.io/badge/react-%2361DAFB.svg?&style=for-the-badge&logo=react&logoColor=black" /> <img src="https://img.shields.io/badge/redux-%23764ABC.svg?&style=for-the-badge&logo=redux&logoColor=white" /> <img src="https://img.shields.io/badge/react%20router-%23CA4245.svg?&style=for-the-badge&logo=react%20router&logoColor=white" />
- Network : <img src="https://img.shields.io/badge/axios-5A29E4.svg?&style=for-the-badge&logo=axios&logoColor=white" />
- Languages : <img src="https://img.shields.io/badge/javascript-%23F7DF1E.svg?&style=for-the-badge&logo=javascript&logoColor=black" /> <img src="https://img.shields.io/badge/html5-%23E34F26.svg?&style=for-the-badge&logo=html5&logoColor=white" /> <img src="https://img.shields.io/badge/css3-%231572B6.svg?&style=for-the-badge&logo=css3&logoColor=white" />
- Manage Tools : <img src="https://img.shields.io/badge/github-%23181717.svg?&style=for-the-badge&logo=github&logoColor=white" /> <img src="https://img.shields.io/badge/git-%23F05032.svg?&style=for-the-badge&logo=git&logoColor=white" /> <img src="https://img.shields.io/badge/figma-%23F24E1E.svg?&style=for-the-badge&logo=figma&logoColor=white" />

## 프로젝트 팀 내 역할
로그인, 회원가입, 개인페이지, 관리자페이지 작성

## 프로젝트 수행 절차
![수행절차](수행절차.png)

## 전체 구조([Figma](https://www.figma.com/design/87rr6KYZyRzEv6WKVzVbQh/DDStore--Copy-?node-id=0-1&t=Oibo53IWqsAGzNp2-1))
![figma](figma.png)

# 담당 기능
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

# KT “소동물 펫케어” 개인 프로젝트 기획서

## [1. 프로젝트 소개]

## 👀 개요

- 동물을 기르는 사람들을 위한 펫케어 프로젝트(KT 소동물 팻캐어 관리 플랫폼)입니다.
- 간단하게 대쉬보드를 통해 반려동물 항목을 추가하고 관리하는 웹 플랫폼으로 구성돼있습니다.
- 자세히
  | **비전** | 모든 소동물들이 행복한 삶을 살고, 주인들은 동물관계 관계에서 행복을 느끼는 것.
  (케이지안에서 기를 수 있는 동물들은 모두 소동물로 정의한다. 단, 이 프로젝트는 우선 파충류로 한정짓는다.) |
  | --- | --- |
  | **미션** | 사용자가 반려 뱀을 효율적으로 관리할 수 있도록 데이터 기반의 맞춤형 솔루션을 제공하고, 언제 어디서나 반려 뱀의 상태를 확인할 수 있는 플랫폼을 구축하는 것. |
  | **핵심가치** | 1. 사용자 중심: 사용자의 요구와 편의를 최우선으로 고려한 기능 설계. 2. 정확성: 정확하고 신뢰할 수 있는 데이터 제공. 3. 접근성: 누구나 쉽게 접근하고 사용할 수 있는 간단하고 직관적인 인터페이스. 4. 지속 가능성: 장기적인 반려 뱀 관리 솔루션을 제공하여 사용자와 반려 동물의 지속적인 관계 유지. 5. 혁신성: 최신 기술을 활용하여 지속적으로 기능을 개선하고 새로운 기능을 도입. |

## 🗂️기능 목록

- JWT 토큰 기반 회원 가입 및 로그인 인증기능
- 새로운 친구 추가하기, 삭제하기 (사진 저장 가능)
- 개체별 먹이기록 추가하기, 불러오기
- 통계기능
  - 날짜별 몸무게 추이 그래프
  - 5가지 성격 평균값 산출 (강인함, 먹성, 귀여움, 신속함, 똑똑함)
  - 달력에 먹이기록 별 표시하기

## 🚨 주의사항

- 추후 storage를 이용할 예정이어서 키값 들은 .env에 별도 보관중입니다.

  - 참조 사용한 브랜치 및 커밋 전략

  ```yaml
  **[브랜치 전략]**
  <커밋_타입>(<영향_범위>): <수정사항_한줄_요약>
    │       │             │
    │       │             └─⫸ 수정사항 한줄 요약
    │       │
    │       └─⫸ 영향받은 서비스: transfer|my-insurance|business-ledger|...
    │
    └─⫸ 수정 종류: feat|fix|perf|refactor|test|ci|docs|build|chore

  브랜치명은 "/"로 구분한다.
  예시) feat/bambam/login

  **[커밋 전략]**
  <커밋_타입>(<영향_범위>): <수정사항_한줄_요약>
    │       │             │
    │       │             └─⫸ 수정사항 한줄 요약
    │       │
    │       └─⫸ 영향받은 서비스: transfer|my-insurance|business-ledger|...
    │
    └─⫸ 수정 종류: feat|fix|perf|refactor|test|ci|docs|build|chore

  setting: 라이브러리 등 초기 환경설정
  feat: 기능 추가
  fix: 버그 수정
  refact: 리팩토링(기능변경x)
  docs: 주석 및 마크다운

  커밋메세지는 " "로 구분한다.
  예시) feat bambam: login validation
  ```

- 이벤트 스토밍

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/e411f5e1-0435-47b2-824f-b1d57e8f6cf8/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/ad2474bd-0ffd-442a-aee1-bc4c2ea60277/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/67d85d37-7514-4b84-976b-8006c6ff5829/image.png)

---

## [1. 프로젝트 소개]

## 👀 개요

- 동물을 기르는 사람들을 위한 펫케어 프로젝트입니다.
- 간단하게 대쉬보드를 통해 반려동물 항목을 추가하고 관리하는 웹 플랫폼으로 구성돼있습니다.
  ![스크린샷 2024-09-11 오전 10.41.41.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/5458091f-b633-4f68-bfe0-85a7a74af22a/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.41.41.png)
  ![스크린샷 2024-09-11 오전 10.44.28.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/d1676ded-5dda-49bc-94f5-80c9414012ce/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.44.28.png)

---

## ✅ 개발 환경

---

### 📝언어

- JAVA, HTML5, CSS3, ES6, SQL

### 🗄️데이터베이스

- postgresql

### 📘 프레임 워크 및 라이브러리

- Sprint boot3 (백앤드) + intelliJ
  - Spring security
  - lombok
  - jwt token
  - modelmapper
- Vue3, Vite (프론트) + vscode
  - pinia (상태관리 라이브러리)
  - Axios (비동기 통신 라이브러리)
  - Tailwind, styled-components (css 라이브러리)
- Azure data stidio

---

## 🗂️기능 목록

- JWT 토큰 기반 회원 가입 및 로그인 인증기능
- 새로운 친구 추가하기, 삭제하기 (사진 저장 가능)
- 개체별 먹이기록 추가하기, 불러오기
- 통계기능
  - 날짜별 몸무게 추이 그래프
  - 5가지 성격 평균값 산출 (강인함, 먹성, 귀여움, 신속함, 똑똑함)
  - 달력에 먹이기록 별 표시하기

## 🚨 주의사항

- 추후 storage를 이용할 예정이어서 키값 들은 .env에 별도 보관중입니다.
  - 참조 사용한 브랜치 및 커밋 전략 (https://github.com/simyeen/bambam_front, https://github.com/simyeen/bambam_back)
  ```yaml
  **[브랜치 전략]**
  <커밋_타입>(<영향_범위>): <수정사항_한줄_요약>
    │       │             │
    │       │             └─⫸ 수정사항 한줄 요약
    │       │
    │       └─⫸ 영향받은 서비스: transfer|my-insurance|business-ledger|...
    │
    └─⫸ 수정 종류: feat|fix|perf|refactor|test|ci|docs|build|chore

  브랜치명은 "/"로 구분한다.
  예시) feat/bambam/login

  **[커밋 전략]**
  <커밋_타입>(<영향_범위>): <수정사항_한줄_요약>
    │       │             │
    │       │             └─⫸ 수정사항 한줄 요약
    │       │
    │       └─⫸ 영향받은 서비스: transfer|my-insurance|business-ledger|...
    │
    └─⫸ 수정 종류: feat|fix|perf|refactor|test|ci|docs|build|chore

  setting: 라이브러리 등 초기 환경설정
  feat: 기능 추가
  fix: 버그 수정
  refact: 리팩토링(기능변경x)
  docs: 주석 및 마크다운

  커밋메세지는 " "로 구분한다.
  예시) feat bambam: login validation
  ```

## [2. 기술적 구현]

### 백앤드

- **JWT 폴더**
  - **LoginFilter: 로그인 성공 시, JWT 토큰을 발급**
    ![스크린샷 2024-09-11 오후 1.38.10.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/22f35466-c586-47b2-ace2-deb74137b1ba/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.38.10.png)
  - **JWTFilter: 올바른 JWT인지 요청이 Controller에 가기 전 검증한다.**
    ![스크린샷 2024-09-11 오후 1.37.05.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/600f8dfd-31a8-49a7-8add-886e7598ba66/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.37.05.png)
  - **JWTUtil: JWT 관련 함수들이 정의돼있다. (만료기한 등등)**
    ![스크린샷 2024-09-11 오후 1.38.00.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/e139b48f-e856-4c20-bbc6-3aa70fed8aef/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.38.00.png)
- **Config 폴더**
  - **SecurityConfig**: JWT 토큰 및 Role 기반 접근 URL 설정파일
    ![스크린샷 2024-09-11 오후 1.34.08.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/89dbc413-52a9-4eee-b242-4fed7757fc8d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.34.08.png)
    ![스크린샷 2024-09-11 오후 1.34.19.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/15e22a52-2531-42ae-8fd9-f745cdf00884/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.34.19.png)
  - WebConfirarion: CORS 에러 해결을 위한 설정파일
    ![스크린샷 2024-09-11 오후 1.34.53.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/85545963-a4c2-44a1-9595-8e3b515956ea/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.34.53.png)
- **Controller 폴더**
  - API 요청을 받으며, Swagger에 대한 어노테이션 존재
    ![스크린샷 2024-09-11 오후 1.30.28.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/5f5f3952-30c6-4284-a5d2-ec78451258dc/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.30.28.png)
- **Service 폴더**
  - 실질적인 비지니스 로직 처리들이 존재
    ![스크린샷 2024-09-11 오후 1.30.52.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/fadf9114-5ac4-49b9-821c-52b6d6ec8173/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.30.52.png)
- **DTO 폴더**
  - 로직을 처리할 때 사용하는 객체
    ![스크린샷 2024-09-11 오후 1.27.56.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/60c8add3-78e5-4df6-9b4a-baeadf998411/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.27.56.png)
- **Entity**
  - 디비에 저장되는 형태의 객체
    ![스크린샷 2024-09-11 오후 1.29.28.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/75b7f840-f57f-41d6-a37d-8aa8e6e9002c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.29.28.png)
- **Repository**
  - JPA를 사용하였고, Join 필요 시 @Query 어노테이션을 활용
    ![스크린샷 2024-09-11 오후 1.29.48.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/0751cf1b-de1c-4eff-bd6c-9cf0168450b1/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.29.48.png)

### 프론트앤드

- **App.js**
  - 클라이언트 접속 시, JWT 토큰을 확인하여 로그인 여부를 판단
  - 로그인 시, pinia을 활용해 토큰을 전역적으로 저장한다.
    ![스크린샷 2024-09-11 오후 1.40.19.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/eed4f46e-e1b6-467a-a8cf-0568d29cceae/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.40.19.png)
- **API 폴더**
  - **index.js 를 통해 아래와 같이 해당 API들을 호출한다. (호출 시, headers에 인증토큰 첨부)**
    ![스크린샷 2024-09-11 오후 1.44.11.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/fbe47f51-8291-4a82-a0d5-c2dc5ffb544e/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.44.11.png)
    ![스크린샷 2024-09-11 오후 1.44.44.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/91290623-1334-430b-ac07-1afaa9fc0d3c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.44.44.png)
- **Container-Presenter 디자인 패턴**
  - **Container 파일:** 자바스크립트 관련 로직 존재(API, 데이터 전처리 등등)
    ![스크린샷 2024-09-11 오후 1.54.57.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/9525404a-83f5-4006-9ca2-399067041e27/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.54.57.png)
  - **Presenter 파일:** Tailwind 기반 html + css 파일 존재
    ![스크린샷 2024-09-11 오후 1.55.16.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/2af4da21-0fbe-4e8b-bca5-445af56fd131/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.55.16.png)
- **폴더구조**
  - atoms: API 로직을 다루지 않는 간단한 형태(재사용 O)
  - block: 팝업 등 페이지는 아니지만 컴포넌트(재사용 O)
  - page: atom과 block들로 이루어진 큰 단위의 컴포넌트(재사용 X)
- **데브옵스**
  - **백로그 활용**
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/e052cf0e-8c1c-4515-a45d-c0f05ddec671/image.png)
  - 깃헙 - main/develop/feat 브랜치활용
    ![스크린샷 2024-09-11 오후 2.09.22.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/04fa051c-1d57-4077-83b9-f185275eb5e1/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.09.22.png)

---

## [3. 아키텍쳐 설계]

### **시스템 아키텍쳐**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/1bcd5550-da0c-4ead-83e6-0eceab5df6c2/image.png)

### **ERD**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/3aaef673-6db0-415c-a02d-0b731435e288/image.png)

- User(breeder)
  ![스크린샷 2024-09-11 오후 2.15.51.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/295ef6c6-94ba-4659-ad4b-7e76946d1294/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.15.51.png)
- species
  ![스크린샷 2024-09-11 오후 2.16.02.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/f486730b-fd1c-4c37-8f91-d20b929c61fd/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.16.02.png)
- Reptile
  ![스크린샷 2024-09-11 오후 2.16.14.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/fca59010-e9e8-4370-b9fc-fbaae543c574/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.16.14.png)
- Feeding
  ![스크린샷 2024-09-11 오후 2.16.40.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/a185c364-d517-45a5-a362-d1dcb984aa05/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.16.40.png)

## [4. 기능 구현]

1. 로그인 페이지 및 회원가입 팝업

   ![스크린샷 2024-09-11 오전 10.40.27.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/8a02b58d-2735-4120-9a12-6fdbe998524b/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.40.27.png)

   ![스크린샷 2024-09-11 오전 10.41.23.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/740ab9b8-e5ee-47a5-bc2c-395869b5d112/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.41.23.png)

   ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/b716d37e-1f27-4b20-beeb-58074b674d83/image.png)

   - 사용한 API
     - GET /api/users/info, GET /api/users/id
     - POST /api/users/join
     - PUT /api/users/id
     - DELETE /api/users/id

2. 새로운 친구 추가 페이지

   ![스크린샷 2024-09-11 오전 10.42.14.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/54a04c17-480a-406b-9a85-d5f0219d3cee/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.42.14.png)

   ![스크린샷 2024-09-11 오후 2.06.54.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/726b8526-80d0-4bb5-bce1-403a026b1b84/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.06.54.png)

3. 홈 페이지

   ![스크린샷 2024-09-11 오전 10.41.41.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/789a9a93-dc4b-459d-97bd-449af9b27c09/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.41.41.png)

   ![스크린샷 2024-09-11 오후 1.52.49.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/0e4ff76b-ceb7-4f01-bf31-f1186039517a/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.52.49.png)

4. 반려동물 페이지

   ![스크린샷 2024-09-10 오후 5.36.49.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/a51e6d79-3a43-49d8-8ad4-17ee3579e20a/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-10_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_5.36.49.png)

   ![스크린샷 2024-09-11 오후 1.45.43.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/4a7a9820-003f-43bd-8d3b-ed78b045495b/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.45.43.png)

   ![스크린샷 2024-09-11 오후 1.57.43.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/35ab11f4-69d3-4b06-9e67-0d4e925cb7ac/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.57.43.png)

5. 새로운 Feeding 기록 추가하기

   ![스크린샷 2024-09-11 오전 10.43.30.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/148132aa-2b1d-4007-8fc6-32f45c446234/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.43.30.png)

   ![스크린샷 2024-09-11 오후 2.08.04.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/f5f594a3-055e-450a-9370-6b3fa36a53b1/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.08.04.png)

6. 추가한 결과 확인

   ![스크린샷 2024-09-11 오전 10.44.28.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/d1676ded-5dda-49bc-94f5-80c9414012ce/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB_10.44.28.png)

7. 캘린더에 먹이준 날짜 표시

   ![스크린샷 2024-09-11 오후 1.51.44.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/ff0eb6cc-d47d-44d4-a27a-f49550eb22d0/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.51.44.png)

8. 통계기능

   ![스크린샷 2024-09-11 오후 1.50.31.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/64aa3a42-8f18-4105-a0a1-bdedec1cfef5/9b4c2dfb-c35d-45ab-b303-b70e23cd977c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-09-11_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_1.50.31.png)

### [시연 영상]

- 동봉된 영상 참조

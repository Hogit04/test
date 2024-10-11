# KT “소동물 펫케어” 개인 프로젝트 기획서

## 👀 개요

- 동물을 기르는 사람들을 위한 펫케어 프로젝트(KT 소동물 팻캐어 관리 플랫폼)입니다.
- 간단하게 대쉬보드를 통해 반려동물 항목을 추가하고 관리하는 웹 플랫폼으로 구성돼있습니다.
- 일일 급여량을 기록하고 날짜별 반려동물의 체중 변화, 일일 급여량등의 정보를 시각화하여 제공합니다.

- 자세히
  _비전_ 모든 소동물들이 행복한 삶을 살고, 주인들은 동물관계 관계에서 행복을 느끼는 것.
  단, 케이지안에서 기를 수 있는 동물들은 모두 소동물로 정의한다. 단, 이 프로젝트는 우선 파충류로 한정짓는다.

  _미션_ 사용자가 반려 뱀을 효율적으로 관리할 수 있도록 데이터 기반의 맞춤형 솔루션을 제공하고, 언제 어디서나 반려 뱀의 상태를 확인할 수 있는 플랫폼을 구축하는 것.
  _핵심가치_

  1. 사용자 중심: 사용자의 요구와 편의를 최우선으로 고려한 기능 설계.
  2. 정확성: 정확하고 신뢰할 수 있는 데이터 제공.
  3. 접근성: 누구나 쉽게 접근하고 사용할 수 있는 간단하고 직관적인 인터페이스.
  4. 지속 가능성: 장기적인 반려 뱀 관리 솔루션을 제공하여 사용자와 반려 동물의 지속적인 관계 유지.
  5. 혁신성: 최신 기술을 활용하여 지속적으로 기능을 개선하고 새로운 기능을 도입.
  6. 안정성: 핵심 기능인 반려동물 등록, 급여량 기록 기능을 MSA방식으로 설계하여 솔루션 안정성 확보.

## 🗂️기능 목록

- 새로운 친구 추가하기, 삭제하기
- 개체별 먹이기록 추가하기, 불러오기
- 통계기능
  - 날짜별 몸무게 추이 그래프
  - 달력에 먹이기록 별 표시하기
 
## UI/UX

![image](https://github.com/user-attachments/assets/c4fc60ed-70a2-4009-8143-fb5b53157f35)
![image](https://github.com/user-attachments/assets/4d2a3907-fad2-4712-a129-606f6862dcbf)



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
## 서비스 시나리오

  1. 사용자가 반려동물을 등록한다.
  2. 등록된 반려동물별로 급여량, 체중등을 기록한다.
  3. 데이터를 수합하여 반려동물 별 시각화자료를 제공한다.
  4. 반려동물, 급여량 데이터는 수정/삭제가 가능하다.
  5. 등록한 반려동물 정보는 메인화면에서 조회가 가능하다.
     
## 분석/설계
### AS-IS조직(Horizontally-Aligned)
![image](https://github.com/user-attachments/assets/42987a4f-dd7e-4f69-86e7-71db9ca8513e)
### TO-BE조직(Vertically-Aligned)
![image](https://github.com/user-attachments/assets/03d85da0-9212-42ef-afae-141fe3756b54)

## 이벤트 스토밍
1. 이벤트 도출
   ![image](https://github.com/user-attachments/assets/87a6da6e-3ce7-4ef3-b89c-bf3d5e8bf26e)
2. 부적격 이벤츠 탈락
  - 단순 프론트엔드 작업 제외
  ![image](https://github.com/user-attachments/assets/4f49ba05-f18f-4d86-9c9b-d269abe8a089)
3. 액터, 커맨드 부착
  ![image](https://github.com/user-attachments/assets/7ace939e-c403-4940-ad6e-d58fcca56b51)
4. 어그리게잇으로 묶기
  ![image](https://github.com/user-attachments/assets/12ba3ba0-0ef0-4bbd-9069-4e7187dc4d15)
5. 바운디드 컨텍스트로 묶기
  ![image](https://github.com/user-attachments/assets/4fd2eaff-fd76-4dc6-a487-c1467c404292)
6. 폴리시 부착및 컨텍스트 매핑(점선은 pub/sub방식)
  ![image](https://github.com/user-attachments/assets/92bd2205-924c-4c81-a112-f5d32af8bd62)
- 최종 결과
  ![image](https://github.com/user-attachments/assets/e39a9a9c-09b4-49f6-b4ca-a6b7b7145c54)
  - 링크
  **https://www.msaez.io/#/130229528/storming/ndpro**

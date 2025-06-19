# 📚 도서 쇼핑몰, **[ink3](https://ink3.shop/)**
<img src='' width="600" height="450" />
<br />

## 💡 프로젝트 개요
**ink3** 는 도서 쇼핑몰 서비스를 제공하는 웹 애플리케이션으로,<br />
Gateway, Eureka, API 서버, 인증 서버, 프론트 서버로 구성된<br />
유사 MSA 아키텍처를 기반으로 개발되었습니다.
<br /><br />

### MSA 도입
기능별 책임을 분리해 독립적인 배포와 장애 격리가 가능하도록 하였고,<br />
팀 간 협업 효율성과 유지보수 용이성을 높이기 위해 MSA 구조를 채택했습니다.
<br /><br />

### 인증 서버 분리
인증, 회원가입, JWT 발급/검증 등 보안 기능을 전담함으로써 민감한 로직을 API 서버와 분리하고,<br />
추후 SSO나 OAuth 연동까지 유연하게 대응할 수 있도록 설계했습니다.
<br /><br />

## 🤗 팀을 소개합니다!
### 우리 팀은 이렇게 협업해요!
- [스크럼](https://github.com/orgs/nhnacademy-be09-ink3/projects/3/views/5) 기반 스프린트 회의
  - 매일 9시 데일리 스크럼
  - 로테이션 스크럼 마스터
  - [WBS](https://github.com/orgs/nhnacademy-be09-ink3/projects/3/views/6) 작성
- 매주 금요일 main 브랜치 배포
  - 테스트 커버리지 측정
- [프로젝트 규칙](https://github.com/orgs/nhnacademy-be09-ink3/projects/3/views/1?pane=issue&itemId=108346363&issue=nhnacademy-be09-ink3%7CInk3%7C1) 기반 개발
  - 브랜치 전략
  - PR 전략
  - Git Commit Convention
<br />

### 팀원 소개
| **Backend** | **Backend** | **Backend** | **Backend** |
| :------: |  :------: |  :------: |  :------: |
| ![](https://github.com/moooooooonlight.png?size=430) | ![](https://github.com/junopo.png?size=150) | ![](https://github.com/KastanEr.png?size=420) | ![](https://github.com/snackcookie.png?size=150) |
| [권용민](https://github.com/moooooooonlight) | [김범준](https://github.com/junopo) | [김윤섭](https://github.com/KastanEr) | [이민후](https://github.com/snackcookie) |
| **Backend** | **Backend** | **Backend** | **Backend** |
| ![](https://github.com/Jihyun3478.png?size=400) | ![](https://github.com/neamoo.png?size=150) | ![](https://github.com/dusk1006.png?size=150) | ![](https://github.com/Messier333.png?size=420) |
| [이지현](https://github.com/Jihyun3478) | [이현수](https://github.com/neamoo) | [정인엽](https://github.com/Jihyun3478) | [최덕영](https://Messier333.com/neamoo) |
<br />

### 역할
#### 권용민
- 

#### 김범준
- 

#### 김윤섭
- 

#### 이민후
- batch server
- rabbit mq
- coupon api/front

#### 이지현
- 

#### 이현수
- 

#### 정인엽
- 

#### 최덕영
- config server
- ci/cd
- 도서 api/front

<br />

## ⚒️ 기술 스택
### 아키텍처 다이어그램
<img width="900" alt="스크린샷 2025-06-16 오후 7 16 18" src="https://github.com/user-attachments/assets/4c9b73f6-ead4-4990-8142-cb329ffdc2ed" />


### CI/CD 다이어그램
<img width="907" alt="스크린샷 2025-06-16 오후 7 13 22" src="https://github.com/user-attachments/assets/d6de5e10-8ad0-48ea-a978-4facfb7512e1" />


# 📚 도서 쇼핑몰, **[ink3](https://ink3.shop/)**
<img width="1728" alt="스크린샷 2025-06-20 오후 12 05 43" src="https://github.com/user-attachments/assets/fee087e7-70c1-4959-a872-95f2339a64c5" />


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
### 1️⃣ 우리 팀은 이렇게 협업해요!
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

### 2️⃣ 팀원 소개
| **Backend** | **Backend** | **Backend** | **Backend** |
| :------: |  :------: |  :------: |  :------: |
| ![](https://github.com/moooooooonlight.png?size=430) | ![](https://github.com/junopo.png?size=150) | ![](https://github.com/KastanEr.png?size=420) | ![](https://github.com/snackcookie.png?size=150) |
| [권용민](https://github.com/moooooooonlight) | [김범준](https://github.com/junopo) | [김윤섭](https://github.com/KastanEr) | [이민후](https://github.com/snackcookie) |
| **Backend** | **Backend** | **Backend** | **Backend** |
| ![](https://github.com/Jihyun3478.png?size=400) | ![](https://github.com/neamoo.png?size=150) | ![](https://github.com/dusk1006.png?size=150) | ![](https://github.com/Messier333.png?size=420) |
| [이지현](https://github.com/Jihyun3478) | [이현수](https://github.com/neamoo) | [정인엽](https://github.com/Jihyun3478) | [최덕영](https://Messier333.com/neamoo) |
<br />

### 3️⃣ 역할
#### 권용민
- 인프라
  - GitHub Action을 이용한 CI/CD 파이프라인 구축
  - 무중단 배포를 위한 Shell Script 작성
  - 마이크로 서버 Eureka 연결
  - NginX 리버스 프록시 설정
- DB 관리
  - ERD 및 DDL 버전 관리
- Shop Server(주문/결제)
  - 주문 API
    - 회원/비회원 주문 API 구현
    - 주문 조회 API 구현
    - 배송 API 구현
    - 반품 API 구현
    - 포장지 API 구현
    - 상품 재고 및 포인트, 쿠폰 처리
  - 결제 API
    - 회원/비회원 결제 API 구현
    - 토스 페이먼트 연동 
    - PayType에 따른 Resolver를 활용한 페이먼트 확장 설계
- Front Server 
  - 주문서 작성 페이지 구현
  - 주문 내역 페이지 구현 (주문 상세 페이지)
  - 관리자 페이지 구현 (배송정책, 반품정책, 주문관리, 포장지관리 페이지)


#### 김범준
- Shop API
  - 도서 API
    - 도서 등록 API 구현
    - 도서 외부 API(알라딘)를 활용한 등록 구현
    - 작가 API 구현
    - 출판사 API 구현
    - 태그 API 구현
- Frontend
  - TUI Editor를 활용한 도서 등록 구현
  - 도서 관리 페이지 구현(도서 등록, 도서 수정, 관리자 도서 목록)
  - 작가, 출판사, 태그 관리 페이지 구현
  - 메인 페이지 구현
  - 도서 상세 페이지 구현


#### 김윤섭
- CI/CD 구성
- 인프라
  - Nginx 리버스 프록시 및 로드 밸런서 설정
  - 게이트웨이 구축 및 연결
    - API Gateway에서 JWT 토큰 검증 필터 구현
    - 비인증 라우팅 경로 화이트리스트 설계 및 적용
- 인증 API
  - 인증 플로우 설계 및 구현
  - JWT 기반 인증 시스템 구축(RSA 서명, Access/Refresh 토큰, 블랙리스트, Refresh 토큰 로테이션)
  - ID/Password, OAuth2 로그인 구현
- Shop API
  - API 응답 일관성을 위한 공통 응답 포맷 구성  
  - 전역 예외 핸들러 구성
  - 권한별 접근 제어 구현
  - 회원 API
    - 회원/어드민 API 구현
    - 맴버십 API 구현
    - 포인트 API 구현
    - 주소 API 구현
    - 좋아요 API 구현
  - 도서 API
    - N 단계 카테고리 설계 및 구현
    - 캐싱 구현
    - 도서 검색 기능(Elasticsearch) 구현
- 프론트엔드
  - 프론트엔드 레이아웃 설계(Thymeleaf, Tailwind CSS)
  - 프론트 서버 로컬 개발환경 분리 및 구성
  - 스프링 시큐리티를 이용한 인증/인가 구현
  - 로그인, 회원가입, 휴면 회원 활성화 페이지 구현
  - 회원 마이페이지 구현(내정보, 주소관리, 포인트 내역, 좋아요 목록, 회원 탈퇴)
  - 관리자 페이지 구현(회원 관리, 맴버십 관리, 포인트 정책 관리, 도서 카테고리 관리)
- DB 인덱스 튜닝


#### 이민후
- batch server
- rabbit mq
- coupon api/front


#### 이지현
- 인프라
  - GitHub Action을 이용한 CI/CD 파이프라인 구축
  - 무중단 배포를 위한 Shell Script 작성
  - Gateway Load Balancer 구현
  - Minio 리버스 프록시 구현
  - 장바구니 조회 시, Apache Bench를 활용한 캐싱 도입 전후 성능 비교
- DB 관리
  - 프로젝트 초기 DDL을 통한 테이블 생성 및 관리
- Shop Server
  - 장바구니 API
    - 비회원 쿠키 기반 장바구니 기능 구현
    - 회원 Redis/DB 기반 장바구니 기능 구현
    - 장바구니 조회 시 Redis 캐싱되도록 구현
  - 리뷰 API
    - 리뷰 API 구현
    - Minio를 활용한 이미지 업로드/수정/삭제 구현
    - 도서에서도 활용하도록 Minio 관련 공통 클래스 분리
  - 도서 API
    - 베스트셀러/신간/추천 도서 API 구현
  - 도서 좋아요 API
    - 도서 좋아요 기능 동작하도록 구현
  - 쿠폰 API
    - 유저 쿠폰함 조회 구현
  - 포인트 API
    - 회원가입 시 포인트 적립 구현
    - 리뷰 작성 시 포인트 적립 구현
    - 결제 시 포인트 적립 구현
    - 포인트 정책 오류 해결
  - 테스트 커버리지 부족한 부분에 대한 테스트코드 작성
- Front Server 
  - 메인 페이지
  - 베스트셀러/신간/추천 도서 목록 페이지
  - 장바구니 페이지
  - 도서 상세 페이지(도서 좋아요 및 리뷰)
  - 유저 쿠폰함 조회 페이지


#### 이현수
- 포인트 정책 API


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


# 기획과 백엔드 구조 설계를 중시하는 백엔드 개발자. 홍성휘입니다.

## 👨‍💻 About Me

**기획과 구조 설계를 중시하는 백엔드 개발자**입니다.  
기능 구현에 앞서, **누구를 위한 기능인지**, **어떻게 구조화할 것인지**를 정의하는 과정을 중요하게 생각합니다.

**협업을 전제한 개발 환경 구성**을 중요시합니다.  
혼자 프로젝트를 진행하면서도 API 명세, Git 커밋/브랜치 전략, Swagger 문서화 등을 작성해왔습니다.

**구조적 설계, 명세 문서화, 협업 준비를 프로젝트에 녹여내려 노력**해왔습니다.

**사용자의 입장에서 문제를 정의하고 해결 방안을 고민합니다.**  
서비스 전반에 대한 깊은 이해와 사용자 중심의 사고방식을 바탕으로 더 나은 경험을 제공하려 노력합니다.

---

## 🛠 Tech Stack

### Languages
![Java](https://img.shields.io/badge/Java-007396.svg?style=flat&logo=java&logoColor=white)

### Backend & Database
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-336791?style=flat)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

### DevOps & Infra
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat)
![Vercel](https://img.shields.io/badge/Vercel-000?style=flat&logo=vercel)

---

## Representative Project – VisiLog (2025)

> **방문자 행동 기반 자동화 마케팅 SaaS 서비스**  
> 웹사이트 방문자의 행동을 수집하고, 조건을 만족할 경우 자동으로 이메일을 발송하는 플랫폼입니다.

- **프로젝트 시작 배경**  
  Cursor IDE를 무료 플랜으로 사용하던 중, 유료 결제 페이지에 진입했다가 결제를 진행하지 않은 채 이탈한 적이 있었습니다.  
  며칠 후, Cursor 팀의 담당자로부터 "**결제 페이지까지 왔다가 나간 이유가 무엇인지, 도움이 필요하다면 연락해달라**"는 메일을 받았습니다.

  이 경험을 통해, **단순한 행동 이력(결제 페이지 진입)만으로도 개인화된 메시지를 보낼 수 있다면, 사용자 경험을 크게 향상시킬 수 있겠다는 인사이트**를 얻게 되었습니다.  
  이에 착안하여, **웹사이트 방문자의 행동 데이터를 수집하고, 특정 조건을 만족하면 자동으로 이메일을 발송하는 SaaS 플랫폼을 직접 만들어보기로** 했습니다.

- **사용자 Pain Point와 해결 방식**  
  많은 웹사이트 운영자는 **사용자의 이탈 순간을 정확히 인지하거나, 그에 맞춰 대응하지 못하는 어려움**을 겪습니다.  
  예를 들어, 결제 직전 페이지까지 접근한 방문자에게 아무런 후속 조치를 하지 못한 채 이탈을 방치하는 경우가 많습니다.

  이 문제를 해결하기 위해,  
  - **SDK로 사용자의 행동 로그를 수집하고**,  
  - **Spring Boot 기반 조건 판별 로직으로 세그먼트를 자동 구성**,  
  - **SendGrid API를 통해 맞춤형 이메일을 자동 발송**하는 구조를 설계했습니다.

  이를 통해 **조건 기반 마케팅 자동화를 구현**할 수 있습니다.

- **구현 기능**  
  - SDK 삽입 → 방문자 행동(page_view, click 등) 자동 수집  
  - 조건 등록 → 조건 충족 시 세그먼트 생성  
  - 스케줄러 → 세그먼트 대상 이메일 자동 발송  
  - 도메인 검증(Interceptor), JWT 인증 구조 구현
 
- **주요 기술**  
  Java 17, Spring Boot 3.4.4, PostgreSQL, Swagger, SendGrid, JWT, GitHub Actions, Docker

 SDK: [behavior-tracking-sdk](https://github.com/SungHuii/behavior-tracking-sdk)  
 Backend: [sdk-behavior-trigger-mvp](https://github.com/SungHuii/sdk-behavior-trigger-mvp)

---

## 개발 시 중요하게 여기는 점

-  기능 단위 설계 → 유저 스토리 / ERD / 시퀀스 → API 명세 → 구현
-  도메인 기반 패키지 구성 (visitor, log_event, condition 등)
-  MockMvc 기반 통합 테스트 작성 및 CI 연동
-  보안 인증 로직 분리 (JWT + Security Filter)
-  Swagger 기반 문서 자동화 → 협업/테스트 가이드화

---

## 학습 중인 기술 (Why & What for)

- **MQ (Message Queue)**  
  → 대량 이메일 발송 시 병목 현상을 줄이고, 발송 요청을 비동기 처리하기 위해 MQ 도입을 고려 중입니다.  
  메시지 유실 시의 처리 방식, 재시도 전략 등 실무 적용을 위한 구조를 학습하고 있습니다.

- **Redis (pub/sub, TTL 등)**  
  → 프로젝트의 세그먼트 조건 만족 여부를 빠르게 판단하고, 발송 큐의 부하를 분산하기 위한 캐시 및 메시지 브로커 용도로 학습 중입니다.  
  향후 pub/sub 구조로 이벤트 기반 알림 시스템 확장을 염두에 두고 있습니다.

- **OAuth2 인증 구조**  
  → 사용자 경험 개선을 위한 소셜 로그인 연동(Discord, Google 등)을 직접 구현하기 위해 OAuth2의 인증 흐름과 토큰 구조를 학습하고 있습니다.

## 📫 Contact

- Email: gkemg2017@gmail.com  
- Blog: [개발블로그](https://b-t-d.tistory.com/)  
- GitHub: [@SungHuii](https://github.com/SungHuii)

---


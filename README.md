# 안녕하세요, 백엔드 개발자 홍성휘입니다. 👋

> **근거 중심의 검증과 최적화로 시스템의 안정성을 확보합니다.**
> 기술을 도입할 때 항상 "왜 이 기술이어야 하는가?"를 집요하게 질문하고, 모니터링과 테스트(k6)를 통한 성능 지표 검증을 바탕으로 아키텍처 당위성을 증명해 나가는 백엔드 개발자입니다.

---

## 🛠️ Tech Stacks

<p>
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=OpenJDK&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=Spring-Boot&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=Spring&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=PostgreSQL&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=Redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=Apache-Kafka&logoColor=white"/>
</p>
<p>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=Amazon-AWS&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=GitHub-Actions&logoColor=white"/>
  <img src="https://img.shields.io/badge/k6-7B62FC?style=flat-square&logo=k6&logoColor=white"/>
</p>

---

## 📊 GitHub Stats & Streak

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=SungHuii&show_icons=true&theme=vue-dark&hide_border=true" alt="SungHuii's GitHub stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=SungHuii&theme=vue-dark&hide_border=true" alt="SungHuii's GitHub Streak" />
</p>

---

## 🚀 Projects

### 🎵 모두의 플리
**대규모 트래픽 대응 글로벌 컨텐츠 평점 및 큐레이션 플랫폼**
- 멀티 인스턴스 스케일아웃 환경에서 **Kafka 메시지 큐와 Redis Pub/Sub 라우팅 아키텍처**를 결합하여 알림/팔로우 도메인의 비동기 디커플링 구현.
- **k6 Soak 테스트 기준 p(95) 응답 속도를 2.00s에서 23.92ms로 약 98.8% 개선.**
- 네트워크 단절 시 알림 유실 방지를 위해 **Redis ZSet 기반의 Last-Event-Id 자동 재연결(자가 치유)** 인프라 구축.

### 📚 덕후감
**도서 이미지 OCR 및 ISBN 매칭 독서 기록 공유 서비스**
- 외부 API 호출 제한을 극복하기 위해 가변성을 분석하고 **Redis 글로벌 캐시와 Caffeine 로컬 캐시를 분산 적용하는 이중화 전략** 수립. (응답 속도 93.5% 향상: 63.3ms ➡️ 4.1ms)
- 외부 API 통신 장애 시 가용성을 지키기 위해 **Spring Retry**를 도입하고, 구체적인 네트워크 예외 대상으로 **1초 지연 간격 최대 3회 재시도의 백오프 전략** 구현.

---

## 📝 Latest Blog Posts
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

---

## 📫 Contact
- **Email:** [gkemg2017@gmail.com](mailto:gkemg2017@gmail.com)
- **Blog:** [Hong's Develop Diary](https://b-t-d.tistory.com/)

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
  <!-- 캐시 갱신 강제 옵션(&cache_seconds=1800) 추가 -->
  <img src="https://github-readme-stats.vercel.app/api?username=SungHuii&show_icons=true&theme=vue-dark&hide_border=true&cache_seconds=1800" alt="SungHuii's GitHub stats" />
  
  <!-- 불안정한 Heroku 서버 대신 공식 최신 데모랩(demolab.com) 서버로 주소 변경 -->
  <img src="https://streak-stats.demolab.com/?user=SungHuii&theme=vue-dark&hide_border=true" alt="SungHuii's GitHub Streak" />
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
- [[CS/Network] C언어 소켓 코드 Java로 이해하기](https://b-t-d.tistory.com/entry/CSNetwork-C%EC%96%B8%EC%96%B4-%EC%86%8C%EC%BC%93-%EC%BD%94%EB%93%9C-Java%EB%A1%9C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)
- [[CS] 프로세스의 계층 구조 - 고아 프로세스, 좀비 프로세스](https://b-t-d.tistory.com/entry/CS-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%9D%98-%EA%B3%84%EC%B8%B5-%EA%B5%AC%EC%A1%B0-%EA%B3%A0%EC%95%84-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EC%A2%80%EB%B9%84-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4)
- [[CS] 메인보드 버스 속도가 CPU만큼 빨라지면, 캐시 메모리는 필요한가?](https://b-t-d.tistory.com/entry/CS-%EB%A9%94%EC%9D%B8%EB%B3%B4%EB%93%9C-%EB%B2%84%EC%8A%A4-%EC%86%8D%EB%8F%84%EA%B0%80-CPU%EB%A7%8C%ED%81%BC-%EB%B9%A8%EB%9D%BC%EC%A7%80%EB%A9%B4-%EC%BA%90%EC%8B%9C-%EB%A9%94%EB%AA%A8%EB%A6%AC%EB%8A%94-%ED%95%84%EC%9A%94%ED%95%9C%EA%B0%80)
- [[아키텍처] 팀 프로젝트에 Kafka / Redis 도입](https://b-t-d.tistory.com/entry/%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98-%ED%8C%80-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%97%90-Kafka-Redis-%EB%8F%84%EC%9E%85)
- [[CS] 커널 자세히 알아보기](https://b-t-d.tistory.com/entry/CS-%EC%BB%A4%EB%84%90-%EC%9E%90%EC%84%B8%ED%9E%88-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0)
<!-- BLOG-POST-LIST:END -->

---

## 📫 Contact
- **Email:** [gkemg2017@gmail.com](mailto:gkemg2017@gmail.com)
- **Blog:** [Hong's Develop Diary](https://b-t-d.tistory.com/)

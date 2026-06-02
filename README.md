# 👨‍💻 Backend Developer Portfolio — 구성모

> Java / Spring Boot 기반 백엔드 개발자입니다. 성능 최적화, 동시성 제어, 그리고 도메인 설계에 관심이 많으며,
> 실제 트래픽을 가정한 캐싱·배치·비동기 처리 경험을 쌓아왔습니다.

📧 **Email:** gusm2561@gmail.com
🔗 **GitHub:** [github.com/gusm96](https://github.com/gusm96)

---

## 🚀 Main Projects

### 1. [myblog-boot](https://github.com/gusm96/myblog-boot) — Spring Boot 기반 블로그 플랫폼

게시글 작성·공유·소통이 가능한 풀스택 블로그 서비스로, **JWT 인증·Redis 캐싱·AWS S3 파일 업로드**를 포함한 실제 운영을 가정해 구현했습니다.
조회수·좋아요 처리에 Redis Write-Behind 전략을 적용해 **응답시간 789ms → 174ms (TPS 4배 개선)** 의 성능 향상을 달성했습니다.
N+1 문제는 Fetch Join · Lazy Loading 으로 해결했고, 스케줄러로 Redis ↔ DB 동기화와 Soft-Delete 게시글의 15일 자동 정리를 처리합니다.
Refresh Token은 HttpOnly Cookie 에 저장해 XSS 공격을 차단하고, Docker · Jenkins · AWS EC2 로 CI/CD 파이프라인을 구성했습니다.

**Tech:** `Java 17` · `Spring Boot` · `Spring Security` · `JPA` · `MariaDB` · `Redis` · `React` · `Docker` · `Jenkins` · `AWS(EC2, S3)`

---

### 2. [WEBA11Y-Server](https://github.com/WEBA11Y/WEBA11Y-Server) — 웹 접근성 자동 검사 API 서버

**KWCAG 2.2 / WCAG 2.1 기준** 으로 웹페이지의 접근성을 자동 점검하는 REST API 서버로, 정적 검사 26종 + 동적 검사 7종 총 **33가지 검사 항목**을 수행합니다.
SPA 환경 대응을 위해 **Playwright** 로 동적 렌더링 후 검사하고, **Jsoup** 으로 정적 HTML 을 파싱해 정적/동적 검사를 분리 설계했습니다.
`@Async` · `CompletableFuture` 로 비동기 병렬 처리하되, 페이지 객체를 공유하는 동적 검사는 순차 실행해 **Race Condition** 을 방지했습니다.
검사 결과는 **SSE(Server-Sent Events)** 로 실시간 스트리밍하며, JPA Batch Insert 로 대량 위반사항 저장 성능을 최적화했습니다.

**Tech:** `Java 17` · `Spring Boot 3.3.7` · `Spring WebFlux` · `Playwright` · `Jsoup` · `JPA/Hibernate` · `MariaDB` · `Redis` · `SSE` · `JWT`

---

## 📚 Sub Projects

| Project                                                      | 설명                                                         | Stack              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------ |
| [daily-transaction-batch](https://github.com/gusm96/daily-transaction-batch) | 대용량 거래 데이터의 효율적 읽기·처리·저장 배치 학습 프로젝트 | Java, Spring Batch |
| [Ticketing](https://github.com/gusm96/Ticketing)             | API Gateway·Concert·Customer·Ticketing 4개 서비스 기반 콘서트 예매 MSA | Java, MSA          |
| [e-commerce](https://github.com/gusm96/e-commerce)           | Spring Cloud 기반 마이크로서비스 아키텍처 학습 프로젝트      | Spring Cloud       |
| [mbti-world](https://github.com/gusm96/mbti-world)           | MBTI 검사와 SNS 기능을 결합한 소셜 플랫폼                    | Java, Spring       |

---

## 🛠 Tech Stack

**Language** &nbsp; `Java` `JavaScript` `TypeScript`
**Backend** &nbsp; `Spring Boot` `Spring Security` `Spring WebFlux` `Spring Cloud` `JPA / Hibernate`
**Database** &nbsp; `MariaDB` `MySQL` `Redis` `H2`
**Frontend** &nbsp; `React` `Redux` 
**DevOps** &nbsp; `Docker` `Jenkins` `AWS (EC2, S3)` `Gradle`
**Tools** &nbsp; `IntelliJ` `Git` `Postman` `JMeter` `Swagger`

---

## 📈 핵심 역량

- **성능 최적화** — Redis 캐싱·Fetch Join·Batch Insert 등으로 응답 속도 및 TPS 개선 경험
- **동시성 제어** — Redis 단일 스레드 모델 활용 및 비동기 처리 시 Race Condition 방지 설계
- **비동기/실시간 처리** — `@Async`·`CompletableFuture`·SSE 기반 실시간 데이터 스트리밍 구현
- **아키텍처 설계** — DDD·MSA·Layered Architecture 학습 및 실제 프로젝트 적용 경험

---

<p align="center">
  <i>꾸준히 학습하고, 더 나은 코드를 고민하는 개발자입니다.</i>
</p>


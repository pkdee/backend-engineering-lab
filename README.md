# Backend Engineering Lab

Java/Kotlin과 Spring 생태계를 기반으로 **백엔드 엔지니어링, 소프트웨어 아키텍처, 분산 시스템**을 탐구하는 개인 학습·실험 저장소입니다.

커머스 도메인의 문제를 직접 구현하고, 장애와 성능 병목을 재현하며, 기술 선택의 근거와 트레이드오프를 검증하는 것을 목표로 합니다.

## Domain

**Commerce Platform — Order & Payment**

주문·결제를 중심으로 필요한 도메인을 확장합니다. 실제 결제 대신 **Mock/Fake PG**를 사용합니다.

|Domain|Scope|
|---|---|
|Member|회원 관리, 인증·인가|
|Product & Search|상품·가격 관리, 검색|
|Inventory|재고 정합성, 동시성 제어|
|Order|주문 생성·취소, 상태 전이|
|Payment|결제 승인·취소·환불, 멱등성, PG 연동|
|Settlement|정산, 거래 대사(Reconciliation), 배치 처리|
|Promotion|쿠폰·할인 정책, 선착순 처리|
|Notification|이벤트 기반 알림·비동기 작업|
|Backoffice|거래 조회, 장애 거래 재처리, 운영 기능|

## Topics & Technologies

아래 항목은 **학습·비교 실험 대상**이며, 모든 기술을 동시에 도입하거나 이미 구현했다는 의미는 아닙니다.

| Category                | Technologies                                                    |
| ----------------------- | --------------------------------------------------------------- |
| Language                | Java, Kotlin                                                    |
| Framework               | Spring Boot, Spring MVC, Spring WebFlux, Spring Security        |
| Asynchronous & Reactive | `@Async`, `CompletableFuture`, Virtual Threads, Project Reactor |
| Persistence             | Spring Data JPA, Hibernate, MySQL, MongoDB                      |
| Search & Cache          | Elasticsearch, Redis                                            |
| Messaging               | Apache Kafka, RabbitMQ, Spring AMQP                             |
| Communication           | REST API, gRPC, Protocol Buffers                                |
| Batch                   | Spring Batch                                                    |
| Build                   | Gradle (Kotlin DSL), Gradle Multi-Module                        |
| Testing                 | JUnit, Mockito, Testcontainers                                  |
| Performance             | k6, Java Flight Recorder (JFR)                                  |
| Infrastructure          | Docker, AWS, Kubernetes, Terraform                              |
| CI/CD                   | GitHub Actions, Argo CD                                         |
| Observability           | Micrometer, Prometheus, Grafana, OpenTelemetry                  |
| AI & Automation         | AI Coding Agents, LLM APIs, MCP                                 |

## Architecture & Design

- OOP, SOLID, Design Patterns
- Layered, Hexagonal (Ports & Adapters), Clean / Onion Architecture
- Domain-Driven Design (DDD), Aggregate, Value Object
- Modular Monolith, Spring Modulith, Gradle Multi-Module
- Microservices Architecture (MSA), Event-Driven Architecture (EDA)
- CQRS, Saga, Transactional Outbox, Event Sourcing — **필요 조건과 비용을 비교하여 선택적으로 실험**

## Engineering Skills

- **Domain & Payment Engineering** — 비즈니스 규칙, 결제 상태·환불, 정산·대사, 멱등성
- **Database & Consistency** — 인덱스·실행 계획, 트랜잭션, 락·데드락, 분산 정합성
- **Concurrency & Messaging** — 스레드 풀, 비동기·리액티브 처리, ACK·Retry·DLQ·중복 소비
- **Performance & Scalability** — 부하 테스트, 병목 분석, 캐싱, p95/p99 지연 시간
- **Reliability & Operations** — Timeout, Circuit Breaker, 장애 복구, SLI/SLO, 관측 가능성
- **Security & Quality** — 인증·인가, 비밀정보 관리, 테스트 자동화, 리팩터링
- **Architecture & Delivery** — 도메인·모듈 경계, API 계약, ADR, CI/CD, 배포·롤백
- **AI-Assisted Engineering** — 개발 자동화, 생성 코드 검증, 생산성 개선

## Approach

**Learn → Build → Experiment → Measure → Document**

단순한 기술 도입보다 **왜 필요한지, 어떤 문제를 해결했는지, 언제 다른 선택이 더 나은지**를 코드·테스트·실험 기록으로 설명합니다.

# Roadmap

Phase별 학습 문서 목록과 핵심 섹션, 실무 연결 포인트를 정리한 로드맵

## Phase 1 — Application Framework

| 순서 | 주제 | 문서 URL | 핵심 섹션 | 실무 연결 |
|---|---|---|---|---|
| 1 | Reactor 스케줄러/에러처리 | https://projectreactor.io/docs/core/release/reference/ | Threading and Schedulers, Handling Errors | WebFlux에서 블로킹 방지, 스케줄러 선택 |
| 2 | Spring WebFlux 동시성 모델 | https://docs.spring.io/spring-framework/reference/web/webflux.html | Concurrency Model, WebClient | Netty 이벤트루프 기반 요청 처리 |
| 3 | Kotlin Coroutines 디스패처 | https://kotlinlang.org/docs/coroutines-guide.html | Coroutine context and dispatchers | WebFlux + Coroutine 조합 시 디스패처 선택 |

## Phase 2 — Data Layer

| 순서 | 주제 | 문서 URL | 핵심 섹션 | 실무 연결 |
|---|---|---|---|---|
| 1 | MongoDB Indexes | https://www.mongodb.com/docs/manual/indexes/ | Compound Indexes, ESR Rule, explain() | 쿼리 실행 계획 검증, 마이그레이션 스크립트 |
| 2 | MongoDB Query Optimization | https://www.mongodb.com/docs/manual/core/query-optimization/ | Query Plans, Plan Cache | explain 결과 분석, 성능 최적화 |
| 3 | WiredTiger | https://www.mongodb.com/docs/manual/core/wiredtiger/ | Cache, Checkpoints, Compression | 컨테이너 환경 메모리 설정, 디스크 I/O |
| 4 | DDIA Ch.3 | 서적 | B-tree vs LSM-tree | WiredTiger 설계 배경 이론 |
| 5 | Kafka 내부 동작 | https://kafka.apache.org/documentation/#design | Partition, Replication, ISR, Log structure | MSA 비동기 통신, 이벤트 기반 아키텍처 |
| 6 | 분산 트랜잭션 / Saga 패턴 | https://microservices.io/patterns/data/saga.html | Choreography vs Orchestration, DDIA Ch.7·9 | 서비스 간 데이터 정합성, 결제 트랜잭션 |

## Phase 3 — Runtime & Observability

| 순서 | 주제 | 문서 URL | 핵심 섹션 | 실무 연결 |
|---|---|---|---|---|
| 1 | JVM GC Tuning | https://docs.oracle.com/en/java/javase/21/gctuning/ | G1/ZGC 동작 원리, Heap Sizing | 힙/RSS 차이, OOMKilled 분석 |
| 2 | JVM Memory | https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-2.html#jvms-2.5 | Heap, Method Area, Stack | 네이티브 메모리 사용 패턴 |
| 3 | PromQL | https://prometheus.io/docs/prometheus/latest/querying/basics/ | Selectors, Functions, Aggregation | Grafana 대시보드 쿼리 작성 |
| 4 | Prometheus Data Model | https://prometheus.io/docs/concepts/data_model/ | Metric types, Labels, Cardinality | Micrometer URI cardinality 문제 |
| 5 | Grafana | https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/best-practices/ | Variables, Template queries | 대시보드 설계 |
| 6 | Pinpoint | https://pinpoint-apm.gitbook.io/pinpoint/want-a-quick-tour/overview | Architecture, Agent 동작 | APM 트레이스 수집 원리 |

## Phase 4 — Infrastructure

| 순서 | 주제 | 문서 URL | 핵심 섹션 | 실무 연결 |
|---|---|---|---|---|
| 1 | K8s Components | https://kubernetes.io/docs/concepts/overview/components/ | Control Plane, Node Components | 클러스터 전체 구조 |
| 2 | Linux 네트워크 스택 | https://jvns.ca/blog/2017/06/03/async-io-on-linux--select--poll--and-epoll/ , Beej's Guide to Network Programming (https://beej.us/guide/bgnet/) | TCP/IP, 소켓, epoll, select/poll 차이 | Netty 이벤트루프 기반, SNAT 문제의 근본 레이어 |
| 3 | K8s Networking | https://kubernetes.io/docs/concepts/services-networking/ | Service, DNS, kube-proxy | SNAT 포트 고갈 등 네트워크 문제 |
| 4 | K8s Resource Management | https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/ | Requests/Limits, QoS | OOMKilled, CPU throttling |
| 5 | eBPF | https://ebpf.io/what-is-ebpf/ | 개요 전체 | kube-proxy → eBPF 전환 배경 |
| 6 | Envoy 아키텍처 | https://www.envoyproxy.io/docs/envoy/latest/intro/arch_overview | Threading model, L7 filter chain | sidecar proxy의 요청 처리 구조, 커넥션 풀링 |
| 7 | Istio 아키텍처 | https://istio.io/latest/docs/ops/deployment/architecture/ | Control plane(istiod), Data plane(Envoy) | 트래픽 라우팅, mTLS, circuit breaker, 분산 트레이싱 |
| 8 | CI/CD 파이프라인 | https://docs.github.com/en/actions/about-github-actions/understanding-github-actions , https://argo-cd.readthedocs.io/en/stable/operator-manual/architecture/ | GitHub Actions Runner 실행 모델, ArgoCD GitOps 구조, Argo Rollouts Canary/Blue-Green | self-hosted runner 운영, 배포 전략의 K8s 레벨 구현 |

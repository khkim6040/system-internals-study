# Phase 3 — Runtime & Observability

## 학습 목표
- JVM의 GC 알고리즘(G1, ZGC)과 메모리 구조를 이해하고 튜닝 포인트를 식별할 수 있다
- Prometheus의 데이터 모델과 PromQL로 의미 있는 메트릭 쿼리를 작성할 수 있다
- APM(Pinpoint) 트레이스를 읽고 병목 구간을 분석할 수 있다

## 포함 주제
- [JVM GC](jvm-gc/) — G1/ZGC 동작 원리, Heap Sizing
- [JVM Memory](jvm-memory/) — Heap, Method Area, Stack, 네이티브 메모리
- [PromQL](promql/) — Selectors, Functions, Aggregation
- [Prometheus Internals](prometheus-internals/) — Metric types, Labels, Cardinality
- [Grafana](grafana/) — Variables, Template queries, 대시보드 설계
- [Pinpoint](pinpoint/) — Architecture, Agent 동작

## 완료 산출물 체크리스트

### 주제별
- [ ] jvm-gc — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] jvm-memory — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] promql — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] prometheus-internals — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] grafana — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] pinpoint — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록

### Phase 회고
- [ ] Phase 회고 노트 작성 (아래 섹션)

## Phase 회고
(Phase 완료 후 작성: 가장 큰 깨달음, 의외였던 점, 실무에서 바로 써먹을 수 있는 것)

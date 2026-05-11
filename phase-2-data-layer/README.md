# Phase 2 — Data Layer

## 학습 목표
- MongoDB의 인덱스 구조와 쿼리 옵티마이저 동작을 이해하고 explain 결과를 읽을 수 있다
- WiredTiger 스토리지 엔진의 캐시/체크포인트 메커니즘을 이해한다
- Kafka의 파티션/복제/ISR 구조와 Saga 패턴의 트레이드오프를 설명할 수 있다

## 포함 주제
- [MongoDB Indexes](mongodb-indexes/) — 복합 인덱스, ESR 규칙, explain
- [MongoDB Query Optimization](mongodb-query-optimization/) — 쿼리 플랜, Plan Cache
- [WiredTiger](wiredtiger/) — 캐시, 체크포인트, 압축
- [DDIA Ch.3](ddia-ch3/) — B-tree vs LSM-tree
- [Kafka](kafka/) — 파티션, 복제, ISR, 로그 구조
- [Saga Pattern](saga-pattern/) — Choreography vs Orchestration

## 완료 산출물 체크리스트

### 주제별
- [ ] mongodb-indexes — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] mongodb-query-optimization — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] wiredtiger — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] ddia-ch3 — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] kafka — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] saga-pattern — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록

### Phase 회고
- [ ] Phase 회고 노트 작성 (아래 섹션)

## Phase 회고
(Phase 완료 후 작성: 가장 큰 깨달음, 의외였던 점, 실무에서 바로 써먹을 수 있는 것)

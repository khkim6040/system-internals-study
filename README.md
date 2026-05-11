# system-internals-study

백엔드 기술 스택의 내부 동작(internals)을 레이어별로 학습하고 정리하는 공간

## 학습 철학

- "이게 없으면 어떻게 되지?" — 기술 요소를 제거했을 때 벌어지는 일을 상상해본다
- "이건 누가 대신 해주고 있지?" — 추상화 아래에서 작동하는 것을 의식한다
- "지금 내가 보고 있는 건 몇 층이지?" — 문제를 바라보는 레이어를 메타 인식한다

## 레이어 구조

| 레이어 | 기술 | Phase |
|---|---|---|
| 애플리케이션 프레임워크 | Reactor, WebFlux, Kotlin Coroutines | Phase 1 |
| 데이터 | MongoDB, WiredTiger, Kafka, Saga, DDIA | Phase 2 |
| 런타임 + 관측 | JVM, Prometheus, Grafana, Pinpoint | Phase 3 |
| 인프라 | Linux Network, K8s, eBPF, Istio/Envoy, CI/CD | Phase 4 |

## 일일 루틴

1. **읽기 (15~20분)** — 현재 주제 문서에서 한 섹션
2. **연결 (5~10분)** — 실무 코드/인프라 어디에 해당하는지 하나 찾기
3. **기록 (5분)** — 핵심 개념을 자기 말로 1~2줄 정리

매주 1~2회는 hands-on 실험으로 30분을 대체한다.

## Phase 완료 정의

각 Phase는 다음이 모두 충족되면 완료된다.

- Phase 내 모든 주제 폴더에 `topic-summary.md` 작성 완료
- 각 주제마다 최소 hands-on 1개 실행하고 결과를 주제 README에 기록
- Phase 회고 노트 1편 작성 (Phase README 하단)

## 진행 상황

### Phase 1 — Application Framework
- [ ] reactor
- [ ] webflux
- [ ] kotlin-coroutines

### Phase 2 — Data Layer
- [ ] mongodb-indexes
- [ ] mongodb-query-optimization
- [ ] wiredtiger
- [ ] ddia-ch3
- [ ] kafka
- [ ] saga-pattern

### Phase 3 — Runtime & Observability
- [ ] jvm-gc
- [ ] jvm-memory
- [ ] promql
- [ ] prometheus-internals
- [ ] grafana
- [ ] pinpoint

### Phase 4 — Infrastructure
- [ ] k8s-components
- [ ] linux-network-stack
- [ ] k8s-networking
- [ ] k8s-resource-management
- [ ] ebpf
- [ ] envoy
- [ ] istio
- [ ] cicd

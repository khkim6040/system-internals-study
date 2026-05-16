# system-internals-study

AI에게 휘둘리지 않고 AI를 잘 휘두르기 위해서는 결국 기반 지식이 깊어야 한다.

백엔드를 이루는 각 계층을 깊이 학습해 AI가 짠 코드뿐만 아니라 새로운 지식을 맞닦뜨릴 때에도 쉽게 이해하고, 비판할 수 있는 자신만의 추상화된 구조를 정립해보자.

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

# Phase 1 — Application Framework

## 학습 목표
- Reactor/WebFlux의 논블로킹 모델이 전통적 서블릿 모델과 어떻게 다른지 구조적으로 이해한다
- 스레드 모델(이벤트루프, 스케줄러, 디스패처)의 차이를 실험으로 체감한다
- WebFlux + Kotlin Coroutines 조합에서의 컨텍스트 전환을 추적할 수 있게 된다

## 포함 주제
- [Reactor](reactor/) — 스케줄러, 에러 처리, 리액티브 스트림
- [WebFlux](webflux/) — 동시성 모델, Netty 이벤트루프, WebClient
- [Kotlin Coroutines](kotlin-coroutines/) — 디스패처, 구조화된 동시성, suspend fun

## 완료 산출물 체크리스트

### 주제별
- [ ] reactor — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] webflux — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] kotlin-coroutines — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록

### Phase 회고
- [ ] Phase 회고 노트 작성 (아래 섹션)

## Phase 회고
(Phase 완료 후 작성: 가장 큰 깨달음, 의외였던 점, 실무에서 바로 써먹을 수 있는 것)

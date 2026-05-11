# Reactor

## 📚 학습 자료
- 공식 문서: https://projectreactor.io/docs/core/release/reference/
- 핵심 섹션: Threading and Schedulers, Handling Errors

## 🎯 학습 목표
- Reactor의 스케줄러 종류와 각 스케줄러가 적합한 작업 유형을 구분할 수 있다
- 에러 처리 연산자(`onErrorResume`, `onErrorReturn`, `retry`)의 동작 차이를 이해한다
- `publishOn`과 `subscribeOn`의 스레드 전환 지점을 정확히 설명할 수 있다

## 🔗 실무 연결
- WebFlux에서 블로킹 호출을 안전하게 격리하기 위한 스케줄러 선택
- 외부 API 호출 실패 시 에러 복구 전략 설계
- 스레드 컨텍스트 유실 문제(MDC, 트레이스 ID) 진단

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `Schedulers.parallel()`, `Schedulers.boundedElastic()`, `Schedulers.single()` 각각에서 작업 실행 후 `Thread.currentThread().name` 찍어서 스레드 이름 비교
- [ ] `Mono.error()` 후 `.onErrorResume()`, `.onErrorReturn()`, `.retry()` 적용해서 동작 차이 확인
- [ ] `Flux.range(1, 100).publishOn(Schedulers.parallel()).subscribeOn(Schedulers.boundedElastic())` 에서 어디서 어떤 스레드가 잡히는지 로그로 추적

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

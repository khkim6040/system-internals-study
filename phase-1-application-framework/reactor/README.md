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
- [ ] 왜 이름이 reactor 인가
- [ ] backpressure 를 관리해준다는데 backpressure 가 정확히 무엇인지?
- [ ] Flux, Mono 이름의 유래?
- [ ] BOM (Bill of Materials)?
- [ ] reactor 는 iterable-iterator pair 관계 모델이라는데 그 의미? 사용 예시가? .flatMap()?
  - [ ] pull-based 가 아니라 push-based 라고 하는데 그 의미도 궁금함 data source 에서부터 결과값이 바깥으로 빠져나가는(emit) 형식이라서 push-based 인가? == publish? -> 그런 것 같음. 바로 다음줄에 reactor model 에서는 publisher-subscriber 모델이고 publisher 가 subscriber 에게 데이터가 준비되었다고 알릴 책임이 있다고 함. push 가 reactive 함에 있어서 중요한 개념이다.
- [ ] imperatively vs declaratively 차이 => 전자는 뭘 구하고 변수에 넣고, 그걸 이용해서 다음 단계를 구하는 통제하는 형태. 후자는 연산의 흐름만 기술하고 변수를 할당하는 등 그 이상의 통제는 하지 않음? 순수 함수?

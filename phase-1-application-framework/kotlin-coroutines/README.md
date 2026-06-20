# Kotlin Coroutines

## 📚 학습 자료
- 공식 문서: https://kotlinlang.org/docs/coroutines-guide.html
- 핵심 섹션: Coroutine context and dispatchers

## 🎯 학습 목표
- 코루틴 디스패처(IO, Default, Unconfined)의 차이와 적합한 사용 시나리오를 구분할 수 있다
- `launch`와 `async`의 차이(반환 타입, 예외 전파)를 명확히 이해한다
- WebFlux + suspend fun 조합에서의 스레드 전환을 추적할 수 있다

## 🔗 실무 연결
- WebFlux + Coroutine 조합 시 디스패처 선택 전략
- 구조화된 동시성(Structured Concurrency)으로 안전한 비동기 처리
- `withContext(Dispatchers.IO)` 사용이 필요한 상황 판단

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `Dispatchers.IO`, `Dispatchers.Default`, `Dispatchers.Unconfined` 에서 `coroutineContext` 출력해서 어떤 스레드풀이 잡히는지 확인
- [ ] `runBlocking` 안에서 `launch`와 `async`의 차이 확인 (반환 타입, 예외 전파 방식)
- [ ] WebFlux + suspend fun 조합에서 `withContext(Dispatchers.IO)` 사용 전후 스레드 변화 관찰

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
코루틴은 spring webflux 와는 관계가 없음. spring webflux 는 reactor 를 이용한 비동기 웹 프레임워크이고, 코루틴은 코틀린 언어 레벨에서 제공하는 비동기 기능임. 따라서 webflux 에서 코루틴을 채택해 사용할수도 있고 그렇게 하지 않을수도 있음. 

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

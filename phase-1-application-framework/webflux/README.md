# WebFlux

## 📚 학습 자료
- 공식 문서: https://docs.spring.io/spring-framework/reference/web/webflux.html
- 핵심 섹션: Concurrency Model, WebClient

## 🎯 학습 목표
- WebFlux의 Netty 이벤트루프 기반 요청 처리 구조를 설명할 수 있다
- 블로킹 코드가 이벤트루프에 미치는 영향을 정량적으로 체감한다
- WebClient의 비동기 요청 처리와 스레드 전환 지점을 추적할 수 있다

## 🔗 실무 연결
- Netty 이벤트루프 기반 요청 처리 구조
- 블로킹 코드가 WebFlux 처리량에 미치는 영향
- WebClient를 통한 외부 서비스 호출 패턴

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] WebFlux 컨트롤러에서 `Thread.currentThread().name` 찍어서 Netty 이벤트루프 스레드 이름(`reactor-http-nio-N`) 확인
- [ ] WebFlux 핸들러 안에 `Thread.sleep(1000)` 같은 블로킹 코드 넣고 동시 요청 시 처리량 변화 측정 (블로킹의 위험 체감)
- [ ] WebClient로 외부 호출 시 `.publishOn()` 위치를 바꿔가며 응답 처리가 어느 스레드에서 일어나는지 관찰

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

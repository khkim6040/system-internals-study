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
webflux 는 기존 mvc 가 이뤄주지 못했던 비동기 처리(non-blocking) 요구 및 함수형(functional) 프로그래밍이란 두가지 큰 요구를 이뤄준다.

리액티브(non-blocking) 프로그래밍에서 왜 back pressure 를 언급하는지 이유
- 그냥 blocking 프로그래밍에서는 처리하는 downstream(=subscriber) 의 처리량 자체가 upstream(=publisher)의 처리량이 됨. back pressure 신경쓸 필요 없음
- 그러나 non-blocking 환경에서는 downstream 과 upstream 의 처리가 묶여있지 않고 따로 진행됨.
  - downstream 이 upstream 의 처리량을 커버할 수 있으면 상관 없음
  - 커버하지 못해 upstream 이 downstream 으로 더 많은 데이터를 공급하면 데이터가 유실되거나, 버퍼가 꽉 차서 문제가 생기거나, 아예 처리가 실패하거나 문제가 생김
  - 따라서 downstream 의 처리량이 딸릴 때 upstream 으로 처리량을 줄일 수 있어야 함. 그게 back pressure 개념임. 즉, non-blocking 성질을 갖고있는 reactive 프로그래밍에서는 back pressure 개념이 중요하다.

## ❓ 궁금한 점 / 추가 학습
- spring MVC 는 servlet 위에서, webflux 는 netty(혹은 servlet) 위에서 동작한다는데, servlet 과 netty 의 차이? 같은 계층인가?
- **annotated** controller 가 무엇이지?
- 

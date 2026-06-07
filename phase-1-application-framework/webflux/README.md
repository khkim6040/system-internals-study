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
 
webflux 의 non-blocking, funtional programming, declarative programming 개념을 학습하는 비용이 크다. 그래서 spring MVC 로 잘 굴러가거나 non-blocking 이 필요없는 곳에서는 webflux 를 쓰지 말라고 한다 ㅋㅋ 쓰려거든 일부분씩만 바꾸면서 이점이 뭔지 계속 파악하라고 함

그래서 reactive 한 논블로킹 프레임워크를 쓰는 이유?
- 블로킹에 비해 더 빨라서는 아님. 심지어 약간의 추가 처리 시간이 더 들 수 있음
- **스케일에 유리하기 때문**임: 더 적은 스레드와 메모리로 블로킹 대비 더 많은 요청을 **예상 가능한 범위**로 처리할 수 있음
- 다만 스케일 상 이점을 얻기 위해서는 요청을 처리하는 데 있어 일정 수준의 지연 시간이 있어야 함

동시성
- MVC: 어플리케이션 로직이 현재 스레드를 블락 가능함 -> 잠재적으로 블락될 스레드를 보상해주기 위해 기반 서버(servlet)는 많은 수의 스레드를 가지고 요청을 처리함
- webflux: 어플리케이션 로직이 현재 스레드를 **블락할 수 없음** -> 잠재적인 블락이 없으니 서버(netty)는 작고 고정된 스레드 풀(event loop workers)만 운용하면 됨

스레드 모델(netty)
- netty 를 위한 스레드 1개. **블록되면 안 됨**
- cpu 개수만큼 1개 -> 요청 처리. **블록되면 안 됨**
- webClient 용 스레드 풀
- 스케줄러 용 스레드 풀: 현재 실행되는 부분을 다른 스레드에 넘기고 싶을 때 publishOn 을 호출함. 이 때 현재 스레드는 계속 실행되면서 스케줄러 스레드 풀에서는 각종 병렬 작업, 블로킹 I/O 작업 등을 수행할 수 있음. 즉, 여기서는 **블록되도 됨**
- 

## ❓ 궁금한 점 / 추가 학습
- spring MVC 는 servlet 위에서, webflux 는 netty(혹은 servlet) 위에서 동작한다는데, servlet 과 netty 의 차이? 같은 계층인가?
  - spring application 을 구동시켜주는 같은 서버 계층이다(여기서 말하는 서버는 따로 정리)
  - netty 는 비동기, 논블로킹 환경에서 주로 사용되며 클라이언트와 서버가 자원을 공유하도록 해 줌. 그래서 webflux 의 기본 서버로 사용됨
  - 다른 것들 tomcat, jetty, servlet 은 그렇지 않나?
- **annotated** controller 가 무엇이지? : 일반적인 @ 어노테이션으로 생성되는 컨트롤러. spring MVC 와 같음. webflux 는 annotated controller 말고도 프로그래밍 모델로 functional endpoints 도 지원함
- functional endpoints: 람다식으로 컨트롤러를 매핑하는 것.
- functional endpoints 는 annotated controller 와의 차이로 "the application is in charge of request handling from start to finish versus declaring intent through annotations and being called back." 라고 하는데 그 의미? 경로 시작부터 끝까지 처리를 자신이 다 한다는 건가? intent through annotations and being called back 의 의미
- webflux 는 reactive api 말고 coroutines api 로도 사용될 수 있다고 하는데, 둘은 같은 레벨인가? 코루틴은 절차형이라는데 차이는?

> - 다만 스케일 상 이점을 얻기 위해서는 요청을 처리하는 데 있어 일정 수준의 지연 시간이 있어야 함
ㄴ 이게 없으면 왜 논블로킹이 블로킹 대비 이점을 갖지 못하지? 만약 처리 시간이 즉각적이라면 요청이 많이 들어왔을 때 블로킹도 막히지 않고 많은 요청을 쳐낼 수 있으므로? 처리 시간이 길면 길수록 블로킹에서 들어온 요청들은 더 길게 기다려야 할 것이기 때문에

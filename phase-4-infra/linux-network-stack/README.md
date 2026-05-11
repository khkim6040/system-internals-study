# Linux Network Stack

## 📚 학습 자료
- 공식 문서: https://jvns.ca/blog/2017/06/03/async-io-on-linux--select--poll--and-epoll/
- 추가 자료: Beej's Guide to Network Programming (https://beej.us/guide/bgnet/)
- 핵심 섹션: TCP/IP, 소켓, epoll, select/poll 차이

## 🎯 학습 목표
- TCP/IP 소켓 프로그래밍의 시스템 콜 흐름을 추적할 수 있다
- select/poll/epoll의 차이와 epoll이 고성능인 이유를 설명할 수 있다
- 네트워크 관련 커널 카운터를 읽고 문제를 진단할 수 있다

## 🔗 실무 연결
- Netty 이벤트루프 기반, SNAT 문제의 근본 레이어
- TIME_WAIT, 포트 고갈 문제 진단

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `strace -e trace=network curl https://example.com` 으로 시스템 콜 흐름 확인 (socket, connect, write, read, close)
- [ ] `ss -tn` 으로 TCP 연결 상태(ESTABLISHED, TIME_WAIT 등) 관찰
- [ ] `nstat -a` 또는 `netstat -s` 로 SNAT/포트 고갈 관련 카운터 위치 파악 (`TcpExt: TCPTimeWaitOverflow`, `IpExt` 등)

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

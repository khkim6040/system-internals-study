# JVM GC

## 📚 학습 자료
- 공식 문서: https://docs.oracle.com/en/java/javase/21/gctuning/
- 핵심 섹션: G1/ZGC 동작 원리, Heap Sizing

## 🎯 학습 목표
- G1 GC와 ZGC의 동작 방식 차이를 설명할 수 있다
- GC 로그를 읽고 pause time, throughput 관점에서 분석할 수 있다
- Heap 크기 설정이 GC 동작에 미치는 영향을 이해한다

## 🔗 실무 연결
- 힙/RSS 차이, OOMKilled 분석
- 컨테이너 환경에서의 JVM 메모리 설정

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] 로컬 Spring Boot 앱에 `-XX:+UseG1GC -Xlog:gc*:file=gc.log` 옵션 붙이고 GC 로그 패턴 분석
- [ ] 같은 앱에 `-XX:+UseZGC` 적용 후 GC 로그 비교 (pause time 차이)
- [ ] `jstat -gc <pid> 1000` 로 실시간 Eden, Survivor, Old 영역 변화 관찰

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

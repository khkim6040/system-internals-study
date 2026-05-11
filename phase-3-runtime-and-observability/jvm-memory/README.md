# JVM Memory

## 📚 학습 자료
- 공식 문서: https://docs.oracle.com/javase/specs/jvms/se21/html/jvms-2.html#jvms-2.5
- 핵심 섹션: Heap, Method Area, Stack

## 🎯 학습 목표
- JVM 메모리 영역(Heap, Method Area, Stack, Native)의 역할을 구분할 수 있다
- Heap 메모리와 컨테이너 RSS의 차이를 이해한다
- NMT(Native Memory Tracking)로 메모리 사용을 진단할 수 있다

## 🔗 실무 연결
- 네이티브 메모리 사용 패턴
- 컨테이너 메모리 limit과 JVM 힙 설정의 관계

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `jcmd <pid> VM.native_memory summary` 로 JVM 네이티브 메모리 사용 영역별 확인 (NMT 활성화 필요)
- [ ] Spring Boot 앱의 `Runtime.getRuntime().totalMemory()` vs 컨테이너 `cat /sys/fs/cgroup/memory.current` 비교 (heap vs RSS 차이 체감)
- [ ] `jcmd <pid> GC.heap_info` 로 힙 영역 상세 정보 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

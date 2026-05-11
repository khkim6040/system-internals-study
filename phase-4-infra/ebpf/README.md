# eBPF

## 📚 학습 자료
- 공식 문서: https://ebpf.io/what-is-ebpf/
- 핵심 섹션: 개요 전체

## 🎯 학습 목표
- eBPF의 개념과 커널 내 동작 원리를 설명할 수 있다
- kube-proxy를 eBPF로 대체하는 배경과 장점을 이해한다
- eBPF 기반 도구(bcc-tools)로 시스템 관측을 수행할 수 있다

## 🔗 실무 연결
- kube-proxy → eBPF 전환 배경
- CNI(Cilium/Calico)의 eBPF 활용 이해

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `bpftool prog list` 로 시스템에 로드된 eBPF 프로그램 확인
- [ ] bcc-tools의 `tcptop`, `execsnoop` 같은 도구 한두 개 실행해보고 출력 관찰
- [ ] 사용 중인 CNI(Cilium/Calico 등)가 eBPF를 어떻게 활용하는지 status 명령으로 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

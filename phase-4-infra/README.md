# Phase 4 — Infrastructure

## 학습 목표
- Kubernetes의 컴포넌트 구조와 네트워킹/리소스 관리 메커니즘을 이해한다
- Linux 네트워크 스택(TCP/IP, epoll)에서 애플리케이션까지의 요청 흐름을 추적할 수 있다
- Service Mesh(Istio/Envoy)와 CI/CD 파이프라인의 내부 동작을 파악한다

## 포함 주제
- [K8s Components](k8s-components/) — Control Plane, Node Components
- [Linux Network Stack](linux-network-stack/) — TCP/IP, 소켓, epoll
- [K8s Networking](k8s-networking/) — Service, DNS, kube-proxy
- [K8s Resource Management](k8s-resource-management/) — Requests/Limits, QoS
- [eBPF](ebpf/) — 개요, kube-proxy 대체 배경
- [Envoy](envoy/) — Threading model, L7 filter chain
- [Istio](istio/) — Control plane, Data plane
- [CI/CD](cicd/) — GitHub Actions, ArgoCD, Argo Rollouts

## 완료 산출물 체크리스트

### 주제별
- [ ] k8s-components — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] linux-network-stack — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] k8s-networking — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] k8s-resource-management — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] ebpf — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] envoy — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] istio — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록
- [ ] cicd — topic-summary.md 작성 + hands-on 1개 이상 실행 결과 기록

### Phase 회고
- [ ] Phase 회고 노트 작성 (아래 섹션)

## Phase 회고
(Phase 완료 후 작성: 가장 큰 깨달음, 의외였던 점, 실무에서 바로 써먹을 수 있는 것)

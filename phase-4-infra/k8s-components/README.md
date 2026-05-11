# K8s Components

## 📚 학습 자료
- 공식 문서: https://kubernetes.io/docs/concepts/overview/components/
- 핵심 섹션: Control Plane, Node Components

## 🎯 학습 목표
- Kubernetes Control Plane 컴포넌트(API Server, etcd, Scheduler, Controller Manager)의 역할을 설명할 수 있다
- Node 컴포넌트(kubelet, kube-proxy, container runtime)의 동작을 이해한다
- 클러스터 전체 구조에서 각 컴포넌트의 상호작용을 파악한다

## 🔗 실무 연결
- 클러스터 전체 구조 이해
- 장애 시 어떤 컴포넌트를 확인해야 하는지 판단

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `kubectl get pods -n kube-system` 로 control plane 컴포넌트 목록 확인
- [ ] `kubectl describe node <node-name>` 로 노드의 kubelet, container runtime 정보 확인
- [ ] `kubectl logs -n kube-system kube-apiserver-xxx` 로 API 서버 로그 일부 분석

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

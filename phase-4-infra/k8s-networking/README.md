# K8s Networking

## 📚 학습 자료
- 공식 문서: https://kubernetes.io/docs/concepts/services-networking/
- 핵심 섹션: Service, DNS, kube-proxy

## 🎯 학습 목표
- Kubernetes Service의 네트워킹 모델(ClusterIP, NodePort, LoadBalancer)을 이해한다
- kube-proxy가 iptables/IPVS 규칙을 통해 서비스 라우팅을 구현하는 방식을 파악한다
- Pod 간 DNS 해석과 서비스 디스커버리 메커니즘을 설명할 수 있다

## 🔗 실무 연결
- SNAT 포트 고갈 등 네트워크 문제 진단
- Service mesh 도입 전 기본 네트워킹 이해

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `kubectl exec` 로 Pod 안에서 `nslookup <service-name>` 실행해 ClusterIP 확인
- [ ] `iptables-save | grep KUBE` 로 kube-proxy가 만든 iptables 규칙 일부 확인 (또는 `ipvsadm -ln`)
- [ ] `kubectl get endpoints <service>` 로 Service 뒤의 실제 Pod IP 목록 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

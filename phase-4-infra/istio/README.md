# Istio

## 📚 학습 자료
- 공식 문서: https://istio.io/latest/docs/ops/deployment/architecture/
- 핵심 섹션: Control plane(istiod), Data plane(Envoy)

## 🎯 학습 목표
- Istio의 Control plane(istiod)과 Data plane(Envoy sidecar)의 역할을 설명할 수 있다
- 트래픽 라우팅, mTLS, circuit breaker의 동작 원리를 이해한다
- VirtualService/DestinationRule을 통한 트래픽 제어를 파악한다

## 🔗 실무 연결
- 트래픽 라우팅, mTLS, circuit breaker, 분산 트레이싱
- 카나리 배포, A/B 테스트 등 트래픽 분할 전략

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `istioctl proxy-config cluster <pod>` 로 sidecar에 주입된 cluster 설정 확인
- [ ] `istioctl proxy-config route <pod>` 로 라우팅 규칙 확인
- [ ] VirtualService 만들어서 라우팅 규칙 변경하고 `istioctl proxy-config` 결과가 어떻게 바뀌는지 추적

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

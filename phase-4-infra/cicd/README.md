# CI/CD

## 📚 학습 자료
- 공식 문서: https://docs.github.com/en/actions/about-github-actions/understanding-github-actions
- 추가 자료: https://argo-cd.readthedocs.io/en/stable/operator-manual/architecture/
- 핵심 섹션: GitHub Actions Runner 실행 모델, ArgoCD GitOps 구조, Argo Rollouts Canary/Blue-Green

## 🎯 학습 목표
- GitHub Actions의 Runner 실행 모델과 워크플로우 구조를 이해한다
- ArgoCD의 GitOps 아키텍처와 sync 메커니즘을 설명할 수 있다
- Argo Rollouts의 Canary/Blue-Green 배포 전략의 K8s 레벨 구현을 파악한다

## 🔗 실무 연결
- self-hosted runner 운영, 배포 전략의 K8s 레벨 구현
- CI/CD 파이프라인 설계 및 트러블슈팅

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] GitHub Actions workflow 하나에 `runs-on: self-hosted` 라벨 붙여서 self-hosted runner의 실행 흐름 확인
- [ ] ArgoCD UI에서 Application의 sync 상태, diff 확인
- [ ] Argo Rollouts에서 Canary 전략으로 배포 시 step별 트래픽 비중 변화 관찰

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

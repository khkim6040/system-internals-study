# K8s Resource Management

## 📚 학습 자료
- 공식 문서: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/
- 핵심 섹션: Requests/Limits, QoS

## 🎯 학습 목표
- Requests와 Limits의 차이와 스케줄링에 미치는 영향을 설명할 수 있다
- QoS Class(Guaranteed, Burstable, BestEffort)의 결정 조건을 이해한다
- CPU throttling과 OOMKilled의 발생 메커니즘을 파악한다

## 🔗 실무 연결
- OOMKilled, CPU throttling 문제 분석
- 컨테이너 리소스 설정 최적화

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] Pod spec에 `resources.requests/limits` 다양하게 설정해보고 `kubectl describe pod` 의 QoS Class 변화 확인 (Guaranteed/Burstable/BestEffort)
- [ ] CPU limit 낮게 설정 후 `kubectl top pod` 와 컨테이너 내부 `cat /sys/fs/cgroup/cpu.stat` 의 `throttled_time` 비교
- [ ] Memory limit 초과 시 OOMKilled 발생시키고 `kubectl describe pod` 의 Last State 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

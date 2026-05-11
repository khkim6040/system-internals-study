# Envoy

## 📚 학습 자료
- 공식 문서: https://www.envoyproxy.io/docs/envoy/latest/intro/arch_overview
- 핵심 섹션: Threading model, L7 filter chain

## 🎯 학습 목표
- Envoy의 스레딩 모델과 요청 처리 구조를 설명할 수 있다
- L7 filter chain의 동작 방식을 이해한다
- Admin endpoint를 통한 런타임 상태 확인 방법을 익힌다

## 🔗 실무 연결
- sidecar proxy의 요청 처리 구조, 커넥션 풀링
- Istio 데이터 플레인의 기반 기술 이해

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] Envoy admin endpoint `curl localhost:15000/clusters` 로 upstream cluster 상태 확인
- [ ] `localhost:15000/stats` 로 연결, 요청, 에러 카운터 확인
- [ ] `localhost:15000/config_dump` 로 실시간 설정 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

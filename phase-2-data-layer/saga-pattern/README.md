# Saga Pattern

## 📚 학습 자료
- 공식 문서: https://microservices.io/patterns/data/saga.html
- 핵심 섹션: Choreography vs Orchestration, DDIA Ch.7·9

## 🎯 학습 목표
- Saga 패턴의 두 가지 구현 방식(Choreography, Orchestration)의 차이를 설명할 수 있다
- 보상 트랜잭션(Compensating Transaction)의 설계 원칙을 이해한다
- 분산 환경에서 데이터 정합성을 유지하는 전략을 비교할 수 있다

## 🔗 실무 연결
- 서비스 간 데이터 정합성, 결제 트랜잭션
- MSA 환경에서의 트랜잭션 경계 설계

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] 결제 → 재고 차감 → 배송 시나리오를 종이에 그려보고 각 단계 실패 시 보상 트랜잭션 흐름 작성
- [ ] 같은 시나리오를 Choreography 방식과 Orchestration 방식 두 다이어그램으로 비교
- [ ] Naver Pay 실무에서 비슷한 패턴 찾아서 어떤 방식인지 식별 (찾을 수 있다면)

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

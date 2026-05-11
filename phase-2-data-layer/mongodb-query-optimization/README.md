# MongoDB Query Optimization

## 📚 학습 자료
- 공식 문서: https://www.mongodb.com/docs/manual/core/query-optimization/
- 핵심 섹션: Query Plans, Plan Cache

## 🎯 학습 목표
- MongoDB 쿼리 옵티마이저가 실행 계획을 선택하는 과정을 이해한다
- Plan Cache의 동작과 무효화 조건을 설명할 수 있다
- 인덱스 활용이 어려운 연산자를 식별하고 대안을 제시할 수 있다

## 🔗 실무 연결
- explain 결과 분석, 성능 최적화
- 인덱스 추가/변경 후 plan cache 영향 이해

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] 동일 쿼리를 여러 번 실행 후 `db.collection.getPlanCache().list()`로 plan cache에 저장된 계획 확인
- [ ] `db.collection.getPlanCache().clear()` 후 인덱스 추가 → plan이 다시 캐싱되는 과정 관찰
- [ ] `$expr`, `$regex` 같은 인덱스 활용 어려운 연산자의 explain 결과 vs 단순 동등 비교 explain 비교

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

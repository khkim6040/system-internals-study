# MongoDB Indexes

## 📚 학습 자료
- 공식 문서: https://www.mongodb.com/docs/manual/indexes/
- 핵심 섹션: Compound Indexes, ESR Rule, explain()

## 🎯 학습 목표
- 복합 인덱스의 순서가 쿼리 성능에 미치는 영향을 설명할 수 있다
- ESR(Equality-Sort-Range) 규칙을 적용해서 인덱스를 설계할 수 있다
- explain 결과에서 IXSCAN/COLLSCAN을 구분하고 성능 지표를 읽을 수 있다

## 🔗 실무 연결
- 쿼리 실행 계획 검증, 마이그레이션 스크립트
- 느린 쿼리 분석 및 인덱스 최적화

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] 테스트 컬렉션에 복합 인덱스(`{a:1, b:1, c:1}`) 만들고 ESR 규칙 어긴 쿼리와 지킨 쿼리의 `explain("executionStats")` 결과 비교 (totalDocsExamined, totalKeysExamined)
- [ ] 인덱스 prefix 활용 쿼리(`{a:1}` 단독)와 prefix 미활용 쿼리(`{b:1}` 단독)의 차이를 explain으로 확인
- [ ] `IXSCAN` vs `COLLSCAN` stage를 explain 결과에서 찾아서 어떤 조건일 때 갈리는지 정리

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

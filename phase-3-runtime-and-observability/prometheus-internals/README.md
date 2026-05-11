# Prometheus Internals

## 📚 학습 자료
- 공식 문서: https://prometheus.io/docs/concepts/data_model/
- 핵심 섹션: Metric types, Labels, Cardinality

## 🎯 학습 목표
- Prometheus의 메트릭 타입(Counter, Gauge, Histogram, Summary)의 차이를 설명할 수 있다
- 라벨 카디널리티가 성능에 미치는 영향을 이해한다
- 시계열 데이터 모델의 구조를 파악한다

## 🔗 실무 연결
- Micrometer URI cardinality 문제
- 메트릭 설계 시 라벨 선택 기준

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `/api/v1/label/__name__/values` 호출해서 현재 수집 중인 메트릭 이름 전체 목록 확인
- [ ] `count by (__name__) ({__name__=~".+"})` 로 메트릭별 시계열 개수 확인 (cardinality 추적)
- [ ] `http_server_requests_seconds_count`의 `uri` 라벨 distinct 개수를 확인해서 Micrometer URI cardinality 폭증 실태 측정

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

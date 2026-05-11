# PromQL

## 📚 학습 자료
- 공식 문서: https://prometheus.io/docs/prometheus/latest/querying/basics/
- 핵심 섹션: Selectors, Functions, Aggregation

## 🎯 학습 목표
- PromQL의 셀렉터, 함수, 집계 연산을 활용해 메트릭 쿼리를 작성할 수 있다
- `rate`, `irate`, `increase`의 차이를 이해하고 적절히 사용할 수 있다
- histogram_quantile로 퍼센타일 쿼리를 작성할 수 있다

## 🔗 실무 연결
- Grafana 대시보드 쿼리 작성
- SLO/SLI 기반 알림 룰 설계

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `rate(http_server_requests_seconds_count[5m])` 기본 쿼리 실행 후 `irate`, `increase` 와 결과 차이 비교
- [ ] `histogram_quantile(0.99, sum by (le) (rate(...)))` 패턴으로 p99 응답시간 쿼리 작성
- [ ] `topk(10, ...)` 로 상위 N개 시계열 추출

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

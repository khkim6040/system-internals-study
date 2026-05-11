# Grafana

## 📚 학습 자료
- 공식 문서: https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/best-practices/
- 핵심 섹션: Variables, Template queries

## 🎯 학습 목표
- Grafana 변수(Variable)를 활용한 동적 대시보드를 구성할 수 있다
- Repeat 옵션과 Template query의 동작을 이해한다
- 효과적인 대시보드 설계 원칙을 적용할 수 있다

## 🔗 실무 연결
- 대시보드 설계 및 유지보수
- 서비스별/환경별 동적 대시보드 구성

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] Grafana 변수(variable) `$service` 만들고 query: `label_values(http_server_requests_seconds_count, service)` 로 동적 드롭다운 구성
- [ ] Repeat 옵션으로 변수별 row/panel 자동 복제 동작 확인
- [ ] 기존 대시보드 하나를 변수 기반으로 리팩토링해서 패널 수 줄여보기

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

# Kafka

## 📚 학습 자료
- 공식 문서: https://kafka.apache.org/documentation/#design
- 핵심 섹션: Partition, Replication, ISR, Log structure

## 🎯 학습 목표
- Kafka의 파티션 기반 메시지 저장과 소비 구조를 설명할 수 있다
- ISR(In-Sync Replicas)과 복제 메커니즘을 이해한다
- Producer의 `acks` 설정에 따른 내구성/성능 트레이드오프를 파악한다

## 🔗 실무 연결
- MSA 비동기 통신, 이벤트 기반 아키텍처
- Consumer group 기반 메시지 처리와 lag 모니터링

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] 로컬에 단일 노드 Kafka 띄우고 `kafka-topics.sh --create --partitions 3` 후 `kafka-console-producer/consumer`로 메시지 흐름 확인
- [ ] `kafka-consumer-groups.sh --describe` 로 consumer group의 offset, lag 관찰
- [ ] `kafka-configs.sh` 로 `min.insync.replicas` 변경 후 producer `acks` 동작 차이 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

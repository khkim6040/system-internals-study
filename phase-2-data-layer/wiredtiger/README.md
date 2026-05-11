# WiredTiger

## 📚 학습 자료
- 공식 문서: https://www.mongodb.com/docs/manual/core/wiredtiger/
- 핵심 섹션: Cache, Checkpoints, Compression

## 🎯 학습 목표
- WiredTiger의 캐시 관리와 eviction 메커니즘을 이해한다
- 체크포인트가 데이터 내구성을 어떻게 보장하는지 설명할 수 있다
- 컨테이너 환경에서의 메모리 설정 고려사항을 파악한다

## 🔗 실무 연결
- 컨테이너 환경 메모리 설정, 디스크 I/O 최적화
- mongostat을 통한 캐시 모니터링

## 🛠 Hands-on

### 시작점 (미리 준비됨, 15분 이내 실행 가능)
- [ ] `mongostat --discover` 띄워두고 대량 insert 실행, `dirty %`, `used %` 변화 관찰
- [ ] `db.serverStatus().wiredTiger.cache` 에서 `bytes currently in the cache`, `eviction server evicting pages` 등 핵심 메트릭 확인
- [ ] `db.collection.stats().wiredTiger` 에서 컬렉션별 cache hit/miss 비율 확인

### 직접 추가 (학습하면서)
- [ ] (학습 중 떠오른 실험을 여기에 추가)

## 📝 학습 노트
(여기에 학습하면서 정리)

## ❓ 궁금한 점 / 추가 학습
(학습 중 생긴 질문이나 더 파볼 주제)

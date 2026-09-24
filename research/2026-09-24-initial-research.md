# 2026-09-24 초기 TTS 연구 기록

## 확보/분석 자료

업로드된 `greatsage-0.0.6.1.jar`에서 OGG 오디오 리소스를 확인했다.

분류 결과(초기 분석):
- 전체 오디오: 약 1,256
- skill: 577
- race: 183
- world: 175
- reply: 167
- voice: 54
- raphael: 27

핵심 TTS 참조 후보는 `voice` + `raphael` 그룹 81개다.

확인된 대표 파일명:
- `kaiseki_kaishi.ogg`
- `kaiseki_kanryou.ogg`
- `kidou.ogg`
- `ryoukai.ogg`

## 엔진 후보

### CosyVoice 계열
우선 검증 대상으로 선정. 한국어/zero-shot 계열 음성 합성 및 API 서버화 가능성을 중점 검증한다.

### F5-TTS
보조 실험 후보. 모델/가중치별 라이선스 조건을 별도로 확인한다.

## 구현 목표

1. 참조 음성 품질 선별
2. OGG → WAV 전처리
3. 음량/무음/샘플레이트 정규화
4. 참조 발화문 메타데이터 작성
5. TTS 엔진 어댑터 구현
6. FastAPI 기반 OpenAI 호환 엔드포인트
7. Docker 패키징
8. OpenClaw/Hermes 연동

## 권리/배포 원칙

캐릭터 또는 성우의 실제 음성을 포함할 가능성이 있는 바이너리 오디오는 권리 확인 전 GitHub에 직접 커밋하지 않는다. 코드, 메타데이터, 연구 기록과 재현 가능한 전처리 도구를 중심으로 저장한다.

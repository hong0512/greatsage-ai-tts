# GreatSage AI TTS

대현자/라파엘 계열의 차분한 AI 시스템 보이스를 연구하기 위한 개인용 TTS 프로젝트입니다.

## 현재 상태

- GitHub 저장소 연결 완료
- `greatsage-0.0.6.1.jar` 음성 리소스 분석 완료
- JAR 내부 오디오: 약 1,256개 OGG
- 핵심 voice 그룹: 54개
- raphael 그룹: 27개
- 핵심 후보 세트: 81개
- TTS 엔진 1차 후보: CosyVoice 계열
- 보조 후보: F5-TTS
- 목표 API: OpenAI 호환 `/v1/audio/speech`
- 최종 연동 목표: OpenClaw / Hermes / NEXORA Vision

## 목표 구조

```
AI Agent
   ↓
TTS API (FastAPI)
   ↓
Voice Profile
   ↓
TTS Engine
   ↓
WAV/MP3
```

## 예정 구성

- `src/` TTS API 및 엔진 어댑터
- `config/` 음성 프로필과 런타임 설정
- `scripts/` 오디오 전처리/검증
- `research/` 엔진 비교 및 실험 기록
- `samples/` 권한 확인된 참조 음성의 로컬 배치 위치

## 주의

원본 캐릭터/성우 음성을 포함할 수 있는 오디오 자체는 라이선스 및 사용 권한을 확인하기 전 공개 배포하지 않습니다.

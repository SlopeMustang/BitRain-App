# BitRain

macOS용 비트퍼펙트 오디오 플레이어. 다운로드와 문제 신고를 위한 저장소입니다.

> A bit-perfect audio player for macOS. This repository hosts downloads and the issue tracker.
> The app's interface is Korean-only at this time.

---

## 무엇을 하는 앱인가

시스템 믹서를 거치지 않고 **DAC에 직접 출력**합니다. 신호 경로에 리샘플링도 믹싱도 넣지 않습니다.

- **AUHAL 직접 출력** — CoreAudio의 출력 유닛을 직접 다뤄 시스템 사운드와 섞이지 않게 합니다
- **독점 모드 (Hog Mode)** — 재생 중 DAC를 점유해 다른 앱의 소리가 들어오지 못하게 합니다
- **자동 샘플레이트 전환** — 트랙마다 원본 레이트로 DAC를 맞춥니다. 44.1k 계열과 48k 계열을 구분합니다
- **업샘플링** — CoreAudio SRC로 1x~16x 또는 DAC가 감당하는 최대치까지
- **NAS 재생** — SMB/NFS 네트워크 스토리지를 전제로 만들었습니다. 다음 곡을 미리 읽어 끊김을 막습니다
- **DSD64 · 고해상도 PCM** — FLAC, ALAC, WavPack, Monkey's Audio 등

## 요구 사양

| 항목 | 내용 |
|---|---|
| OS | macOS 14.0 (Sonoma) 이상 |
| 프로세서 | Apple Silicon **및** Intel |
| 인터페이스 | 한국어 |

**Intel Mac은 아직 실기 검증을 거치지 않았습니다.** 동작 보고를 받는 것이 이 저장소를 연 이유 중 하나입니다.

## 다운로드

준비 중입니다. 준비되면 [Releases](../../releases)에 올립니다.

버전별 변경 내용은 [CHANGELOG](CHANGELOG.md)에 있습니다.

## 문제를 발견했다면

[이슈를 열어](../../issues/new/choose) 주십시오. **진단 스냅샷을 함께 붙여 주시면** 원인을 훨씬 빨리 좁힐 수 있습니다.

스냅샷은 앱에서 얻습니다 — **도움말 › BitRain 도움말 › 진단 › 진단 스냅샷 복사**

스냅샷에 담기는 것은 앱 설정, 오디오 장치 정보, 라이브러리 통계, 하드웨어 사양입니다. **음악 파일의 내용이나 개인 정보는 읽지 않습니다.** 붙여넣기 전에 내용을 직접 확인하실 수 있습니다.

특히 알고 싶은 것은 이 세 가지입니다.

- 다른 **DAC**에서 독점 모드와 샘플레이트 전환이 성립하는지
- **Intel Mac**에서 재생이 정상인지
- 다른 **NAS**(Synology 외)에서 폴더 마운트가 성립하는지

## 라이선스

BitRain은 [Kushal Pandya](https://github.com/kushalpandya)의 [Petrichor](https://github.com/kushalpandya/Petrichor)에서 파생했으며 MIT 라이선스에 따라 사용합니다.

```
Copyright (c) 2025 Kushal Pandya
```

전체 라이선스 고지와 서드파티 크레딧은 앱 안에서 볼 수 있습니다 — **도움말 › BitRain 도움말 › 라이선스 및 크레딧**

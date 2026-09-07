# Findex 배포 채널

[Findex](https://github.com/changinho25/findex) — Windows 파일 검색기 (PyQt6 + SQLite FTS5) 의
**배포물 전용 저장소**입니다. 소스 코드는 포함되어 있지 않습니다.

## 다운로드

[최신 릴리스](https://github.com/changinho25/findex-dist/releases/latest) 에서
`Findex-vX.Y.Z-win64.zip` 을 받아 원하는 폴더에 압축을 풀고 `Findex.exe` 를 실행합니다.

설치 과정은 없으며, 사용자 데이터는 앱 폴더가 아닌 아래 위치에 저장됩니다.

| 데이터 | 위치 |
|---|---|
| 설정 · 검색 히스토리 | `%APPDATA%\Findex` |
| 인덱스 DB | `%LOCALAPPDATA%\Findex` |

따라서 새 버전으로 올릴 때는 **앱 폴더만 통째로 교체**하면 되고, 설정과 인덱스는 그대로 유지됩니다.

## latest.json

Findex 앱이 새 버전 확인에 사용하는 파일입니다.

```
https://raw.githubusercontent.com/changinho25/findex-dist/main/latest.json
```

| 필드 | 설명 |
|---|---|
| `version` | 최신 버전 (SemVer, `v` 접두사 없음) |
| `released` | 릴리스 날짜 (YYYY-MM-DD) |
| `url` | zip 직접 다운로드 URL |
| `size` | zip 바이트 크기 |
| `sha256` | zip 무결성 검증용 해시 |
| `notes` | 한 줄 요약 |
| `notes_url` | 릴리스 상세 페이지 |

앱은 이 파일을 하루 1회 백그라운드로 확인하며, 실패해도 앱 동작에는 영향을 주지 않습니다.
업데이트 확인은 설정 > 고급 에서 끌 수 있습니다.

# HD2 Crash Radar

헬다이버즈2 크래시/튕김 원인 확인을 돕는 비공식 Windows 진단 도구입니다.

Windows 오류 기록과 로컬 캐시 상태를 확인해 헬다이버즈2 크래시 원인 후보를 정리하고, 먼저 시도할 조치를 안내합니다.

## 주요 기능

- 헬다이버즈2 관련 Windows 이벤트 로그 확인
- 크래시 원인 후보 표시
  - 높음
  - 보통
  - 낮음
- 원인 후보별 근거와 먼저 시도할 조치 안내
- 공유용 오류 보고서 저장
- HD2 `shader_cache` 정리 도우미
- Steam `shadercache\553850` 정리 도우미
- DX11 / Toaster / DX11 + Toaster 실행 옵션 복사
- `user_settings.config` 확인 및 삭제 도우미
- GitHub Releases 기반 최신 버전 확인
- 개인정보 마스킹이 적용된 보고서 생성

## 다운로드 및 실행

1. [Releases](https://github.com/SAM7599/HD2-Crash-Radar/releases) 페이지에서 최신 ZIP 파일을 다운로드합니다.
2. ZIP 압축을 풉니다.
3. `HD2_Crash_Radar.exe`를 실행합니다.
4. 진단 대시보드에서 원인 후보를 확인합니다.
5. 필요하면 `공유용 저장`으로 보고서를 저장해 도움 요청 시 첨부합니다.

## 필요 환경

- Windows 10 이상 권장
- .NET 8 Desktop Runtime 필요

현재 배포본은 아래 파일들이 함께 있어야 실행됩니다.

```text
HD2_Crash_Radar.exe
HD2_Crash_Radar.dll
HD2_Crash_Radar.deps.json
HD2_Crash_Radar.runtimeconfig.json
```
`HD2_Crash_Radar.exe`만 따로 빼서 실행하면 정상 작동하지 않을 수 있습니다.
## 실행이 안 될 때

이 실행기는 .NET 8 Desktop Runtime이 필요합니다.

실행 시 .NET 관련 오류가 나오면 아래 Microsoft 공식 페이지에서  
`.NET 8 Desktop Runtime`을 설치한 뒤 다시 실행해 주세요.

https://dotnet.microsoft.com/download/dotnet/8.0
## 사용 방법
## 1. 진단 대시보드
`다시 검사`를 누르면 최근 Windows 오류 기록과 헬다이버즈2 관련 단서를 확인합니다.

위험도 기준:
- `높음`: 크래시 로그와 특정 단서가 함께 잡힌 항목
- `보통`: 가능성은 있지만 다른 원인과 비교가 필요한 항목
- `낮음`: 참고용 단서이거나 재현 직후 다시 검사하면 더 정확해질 수 있는 항목

원인 후보를 클릭하면 세부 정보 칸에서 다음 내용을 확인할 수 있습니다.
- 감지 근거
- 가능성 점수
- 먼저 시도할 조치
- 추가 설명

## 2.FPS·안정성 가이드
Steam 커뮤니티 가이드 흐름에 맞춰 자주 쓰는 조치를 버튼으로 제공합니다.

포함된 기능:
- DX11 실행 옵션 복사
- Toaster Mode 실행 옵션 복사
- HD2 `shader_cache`자동 경로 지정 및 정리
- Steam `shadercache\553850`자동 경로 지정 정리
- DirectX Shader Cache 정리 안내
- `user_settings.config`확인 및 삭제

참고 출처:
https://steamcommunity.com/sharedfiles/filedetails/?id=3167233254

## 3.온라인 정보
`최신 버전 확인`버튼을 누르면 GitHub Releases의 최신 버전을 확인합니다.
https://github.com/SAM7599/HD2-Crash-Radar/releases
이 기능은 사용자가 버튼을 눌렀을 때만 GitHub 공개 릴리스 정보를 읽습니다.
보고서, PC 이름, 사용자 경로, SteamID 등은 전송하지 않습니다.

## 주의사항
- 이 도구는 비공식 팬 제작 도구입니다.
- Arrowhead Game Studios, PlayStation, Steam, Discord와 공식 관련이 없습니다.
- 게임 파일을 변조하지 않습니다.
- GameGuard/nProtect를 우회하지 않습니다.
- 메모리 주입, DLL 삽입, 프로세스 후킹을 하지 않습니다.
- 캐시 정리는 안전 확인을 통과한 경로의 파일만 대상으로 합니다.
- 캐시 정리 후 첫 실행에서는 셰이더 재생성 때문에 잠시 검은 화면이나 로딩 지연이 생길 수 있습니다.
- DX11 / Toaster 옵션은 PC 환경에 따라 효과가 다를 수 있습니다.
- 진단 결과는 확정 판정이 아니라 원인 후보를 좁히기 위한 참고 정보입니다.

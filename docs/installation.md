# 설치 안내

**한국어** · [English](installation.en.md)

**현재 첫 공개 배포를 준비 중이며 설치 파일은 아직 없습니다.** 아래 절차는 검증된 파일이 [Releases](https://github.com/zamk-DAV/trackpad/releases)에 올라온 뒤 사용할 안내입니다.

## 호환성 확인

- Apple silicon Mac과 내장 트랙패드가 필요합니다. Intel Mac과 외장 Magic Trackpad는 현재 지원하지 않습니다.
- 트랙패드 접촉 인식은 macOS 빌드 `25F84`, `25G83`에서만 활성화됩니다. 터미널의 `sw_vers -buildVersion`으로 확인할 수 있습니다.
- 앱의 설치 하한인 macOS 14.0과 트랙패드 접촉 인식의 지원 범위는 다릅니다. 모든 macOS 14 이상 버전에서 인식된다는 뜻이 아닙니다.

## 공개 후 설치 순서

1. 이 저장소의 Releases에서 앱 ZIP과 `SHA256SUMS`를 받습니다.
2. 두 파일이 있는 폴더에서 `shasum -a 256 -c SHA256SUMS`를 실행해 다운로드를 확인합니다.
3. ZIP을 풀고 `Flicklane.app`을 응용 프로그램 폴더로 옮겨 실행합니다. 업데이트라면 기존 Flicklane을 먼저 종료하세요.
4. 사용할 기능에 필요한 권한을 앱 안내에 따라 허용합니다. macOS가 요구하면 앱을 종료하고 다시 엽니다.
5. 규칙을 만들고 인식과 동작을 테스트한 뒤 활성화합니다.

설치할 때 보안 검사에서 차단된다면 macOS 버전과 오류 메시지를 [Issues](https://github.com/zamk-DAV/trackpad/issues)에 알려주세요. 이 안내에서는 시스템 보안 기능을 끄거나 격리 속성을 지우도록 요구하지 않습니다.

## 권한과 업데이트

입력 모니터링은 입력 감지, 손쉬운 사용은 창·키보드·마우스 제어에 사용합니다. 화면 캡처나 다른 앱 제어에는 화면 기록·자동화 권한이 필요할 수 있습니다. [개인정보 안내](../PRIVACY.md)를 참고하세요.

기존 GestureForge 이름으로 사용했다면 이전 앱과 Flicklane을 동시에 실행하지 마세요. 규칙과 녹화 설정의 저장 위치는 그대로 유지됩니다. 설정 파일이나 백업을 지우지 않고 앱만 교체합니다.

[사용법](usage.md) · [처음으로](../README.md)

<p align="center">
  <img src="assets/icon.png" width="112" alt="Flicklane 앱 아이콘">
</p>

# 트랙패드 · Flicklane

**한국어** · [English](README.en.md)

**Mac의 트랙패드 제스처와 키보드 입력에 원하는 동작을 연결하세요.**

Flicklane(플릭레인)은 직접 녹화한 제스처, 키 입력 순서, 단축키로 반복 작업을 줄이는 macOS 앱입니다.

이 저장소는 **앱 다운로드·사용 안내·문의**를 위한 공간입니다. 앱 소스 코드는 공개하지 않습니다.

[사용법](docs/usage.md) · [설치 안내](docs/installation.md) · [Releases](https://github.com/zamk-DAV/trackpad/releases) · [오류 제보·기능 제안](https://github.com/zamk-DAV/trackpad/issues) · [♥ 후원](https://buymeacoffee.com/flicklane)

## 할 수 있는 일

| 기능 | 설명 |
| --- | --- |
| 트랙패드 제스처 | 기본 제스처를 고르거나 나만의 접촉·탭·이동 순서를 녹화합니다. |
| 시간 여유 조절 | 터치 사이의 쉼과 동작 길이 허용 범위를 각각 조절합니다. |
| 키보드 매크로 | 키를 순서대로 누르거나 보조 키와 조합해 동작을 실행합니다. |
| 화면 분할 | 키를 누른 채 마우스를 움직여 창을 절반·사분면·최대화로 배치합니다. |
| 여러 동작 연결 | 앱·웹사이트 열기, 창 제어, 키·텍스트 입력 등의 동작을 순서대로 연결합니다. |
| 규칙별 설정 | 적용할 앱을 고르고 인식·실행 테스트 후 규칙을 켭니다. |
| 언어 선택 | 시스템 언어 자동 선택 또는 한국어·영어·일본어·중국어 간체/번체를 선택합니다. |
| 메뉴 막대 | ♥ 후원, ⚙ 설정, ⏻ 종료에 빠르게 접근합니다. 설정을 누르면 앱 메인 창이 열립니다. |

## 다운로드

**첫 공개 베타: 0.1.0 Beta 1 · 빌드 19 · Apple silicon**

[**Flicklane 다운로드 (.zip)**](https://github.com/zamk-DAV/trackpad/releases/download/v0.1.0-beta.1/Flicklane-0.1.0-19-arm64.zip) · [릴리스 안내·체크섬](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.0-beta.1)

Developer ID 서명과 Apple 공증을 완료했으며, 최종 ZIP을 다시 풀어 서명·공증 티켓·Gatekeeper 검사를 통과했습니다. **초기 베타로, 다른 Mac 모델에서의 동작 검증은 진행 중입니다.** 지원 범위를 확인한 뒤 [설치 안내](docs/installation.md)를 따라주세요.

새 버전 소식은 GitHub **Watch → Custom → Releases**에서 받을 수 있습니다.

## 지원 범위

- Apple silicon Mac의 **내장 트랙패드**를 대상으로 개발하고 있습니다.
- 외장 Magic Trackpad와 Intel Mac은 현재 지원 대상이 아닙니다.
- 현재 접촉 입력이 허용된 macOS 빌드는 `25F84`, `25G83`입니다. 모든 macOS 버전이나 Mac 모델에서 검증된 것은 아닙니다.
- 트랙패드 입력에는 비공개 MultitouchSupport 프레임워크를 사용하므로 macOS 업데이트에 따라 재검증이 필요합니다. Mac App Store 배포 앱은 아닙니다.

## 사용 흐름

1. 트랙패드 또는 키보드 탭에서 **새 규칙**을 만듭니다.
2. 사용할 입력을 선택하거나 녹화합니다.
3. **동작 추가**로 실행할 일을 연결하고 적용할 앱을 선택합니다.
4. 인식과 동작을 테스트한 뒤 **이 규칙 활성화**를 켭니다.

자세한 녹화 방법과 시간 설정은 [사용법](docs/usage.md)을 참고하세요.

앱 오른쪽 위 톱니바퀴 → **언어**에서 표시 언어를 바꿀 수 있습니다. 기본값은 시스템 설정이며, 변경은 앱을 다시 실행하면 적용됩니다. 상단 메뉴 막대의 **설정**은 메인 창을 여는 메뉴입니다.

## 문의와 후원

문제나 아이디어는 [Issues](https://github.com/zamk-DAV/trackpad/issues)로 알려주세요. 오류 제보 시 Mac 모델과 macOS 빌드, 재현 순서를 함께 적어주시면 도움이 됩니다.

개발을 응원하고 싶다면 [Buy Me a Coffee에서 후원](https://buymeacoffee.com/flicklane)할 수 있습니다. 후원은 선택 사항이며, 한국어·영어 설명은 [후원 안내](SPONSORING.md)에서 확인할 수 있습니다.

입력 인식과 규칙 저장은 Mac에서 처리합니다. 필요한 권한과 데이터 보관 방식은 [개인정보 안내](PRIVACY.md)에 정리했습니다.

주변에 소개할 때 사용할 [한국어·영어 소개 문구](docs/share.md)도 준비했습니다.

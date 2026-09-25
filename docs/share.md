# Flicklane 소개 문구 · Share Flicklane

**0.1.6 Beta 1 · 빌드 / build 25** 기준입니다. 아래 글을 복사해 소개할 수 있습니다. / Copy the text below to introduce this release.

## 한국어 · 짧은 소개

Mac에서 제스처와 키보드 매크로, 화면 분할, 커서 옆 퀵 메뉴를 한 앱으로 쓰는 **Flicklane(플릭레인)**을 추천해요. 직접 녹화한 동작에 원하는 기능을 연결하고, 4·5·8·9분할 퀵 메뉴에서 복사·붙여넣기·캡처나 저장한 키보드 매크로를 선택할 수 있습니다. 마우스와 트랙패드의 스크롤 방향을 따로 설정하고, 지원되는 장치의 포인터 감도를 조절할 수 있어요. 한국어를 포함한 5개 언어를 지원하는 공개 베타입니다.

[기능과 다운로드](https://github.com/zamk-DAV/trackpad)

## 한국어 · 0.1.6 업데이트 소개

**Flicklane 0.1.6 Beta 1**을 공개했습니다.

- **독·USB 수신기 장치 감지 수정:** 앱 실행 후 연결한 마우스가 누락되던 문제를 수정했습니다. 자동 감지와 장치 새로고침에 최신 연결 목록을 사용합니다.
- **포인터 적용 상태 확인:** 설정 값이 실제로 바뀌지 않으면 적용 성공으로 처리하지 않습니다. 변경 중 실패하면 이전 값으로 복원을 시도합니다.
- **트랙패드 제한 명확화:** 기기별 설정을 확인할 수 없는 장치는 ‘적용 안 됨’으로 표시하고 조절기를 비활성화합니다. macOS 포인터 설정 바로가기를 제공합니다. **이 업데이트는 내장 트랙패드의 직접 감도 조절을 구현한 것이 아닙니다.**
- **가속 끄기 안내 개선:** 속도 배율이 적용되지 않는 구형 방식에서는 속도 조절기를 비활성화하고 해당 장치를 안내합니다. 새 안내는 5개 언어를 지원합니다.

Apple silicon과 Intel 실행 파일을 함께 담은 Universal 앱이며 macOS 14·15·26을 대상으로 합니다. Developer ID 서명과 Apple 공증을 완료했습니다. 기기에서 입력을 확인한 뒤 트랙패드 동작을 활성화하며, 모든 모델의 실기기 검증을 마쳤다는 뜻은 아닙니다. [현재 지원 범위](https://github.com/zamk-DAV/trackpad#지원-범위)를 확인해 주세요.

[다운로드와 변경 내역](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.6-beta.1) · [사용법](https://github.com/zamk-DAV/trackpad/blob/main/docs/usage.md) · [의견과 오류 제보](https://github.com/zamk-DAV/trackpad/issues) · [♥ 선택 후원](https://buymeacoffee.com/flicklane)

## English · Short introduction

Try **Flicklane**, a macOS app for trackpad gestures, keyboard macros, window tiling, and a Quick Menu beside your cursor. Record your own gestures and choose copy, paste, capture, saved keyboard macros, and other actions from 4/5/8/9 menu positions. Set mouse and trackpad scroll directions separately and adjust pointer sensitivity on supported devices. It is a public beta with support for five languages.

[Features and downloads](https://github.com/zamk-DAV/trackpad/blob/main/README.en.md)

## English · 0.1.6 announcement

**Flicklane 0.1.6 Beta 1 is available.**

- **Dock and USB receiver discovery:** Fixed devices connected after app launch being missed. Automatic discovery and manual refresh now use a fresh device list.
- **Verified pointer settings:** Unchanged settings are no longer treated as successfully applied. Failed changes trigger an attempt to restore earlier values.
- **Clear trackpad limits:** Devices without verifiable per-device settings show “Not applied” with disabled controls and a shortcut to macOS pointer settings. **This update does not implement direct sensitivity control for the affected built-in trackpad.**
- **Acceleration-off guidance:** Speed controls are disabled for legacy modes that ignore the multiplier, with the affected devices named. New messages support all five languages.

The universal app includes Apple silicon and Intel executables and targets macOS 14, 15, and 26. It is Developer ID signed and Apple notarized. Trackpad actions become available after on-device input checks; this does not establish physical compatibility with every model. See the [current compatibility details](https://github.com/zamk-DAV/trackpad/blob/main/README.en.md#compatibility).

[Download and release notes](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.6-beta.1) · [User guide](https://github.com/zamk-DAV/trackpad/blob/main/docs/usage.en.md) · [Feedback](https://github.com/zamk-DAV/trackpad/issues) · [♥ Optional support](https://buymeacoffee.com/flicklane)

## 화면 자료 · Media

[화면 자료의 버전 안내 / UI media versions](media.md)를 확인하세요. 이전 화면을 0.1.6 화면처럼 소개하지 마세요. / Do not present earlier screenshots as the current 0.1.6 interface.

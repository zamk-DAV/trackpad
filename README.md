<p align="center">
  <img src="assets/icon.png" width="112" alt="Flicklane 앱 아이콘">
</p>

# 트랙패드 · Flicklane

**한국어** · [English](README.en.md)

**Mac의 트랙패드 제스처와 키보드 입력에 원하는 동작을 연결하세요.**

[**Flicklane 다운로드 (.zip)**](https://github.com/zamk-DAV/trackpad/releases/download/v0.1.2-beta.1/Flicklane-0.1.2-21-universal.zip) · **0.1.2 Beta 1 · 빌드 21 · Apple silicon + Intel**

[설치 안내](docs/installation.md) · [사용법](docs/usage.md) · [릴리스 안내](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.2-beta.1) · [오류 제보](https://github.com/zamk-DAV/trackpad/issues) · [♥ 후원](https://buymeacoffee.com/flicklane)

Flicklane(플릭레인)은 직접 녹화한 제스처, 키 입력 순서, 단축키로 반복 작업을 줄이는 macOS 앱입니다. 이 저장소에는 앱 다운로드와 안내 문서만 공개하며, 앱 소스 코드는 공개하지 않습니다.

![Flicklane의 규칙과 기능 화면](assets/flicklane-overview.png)

*예시 설정으로 촬영한 실제 앱 화면입니다. 입력 감지와 동작 실행을 꺼 두었으며, 실기기 동작 검증 자료가 아닙니다.*

## 세 단계로 시작하기

1. 위 ZIP을 받아 압축을 풉니다.
2. `Flicklane.app`을 **응용 프로그램**으로 옮겨 엽니다. 업데이트할 때는 기존 앱을 먼저 종료하세요.
3. 앱에서 필요한 권한을 허용하고 첫 규칙을 만듭니다. 입력 확인 안내가 나오면 **손가락 두 개를 잠시 올렸다가 모두 떼세요.**

## 지원 범위

| 환경 | 지원 및 검증 상태 |
| --- | --- |
| Apple silicon · 내장 트랙패드 · macOS 빌드 `25F84`, `25G83` | 기존 로컬 실기기 검증 범위입니다. 모든 Mac 모델을 검증한 것은 아닙니다. |
| Apple silicon · 내장 트랙패드 · macOS 14 / 15 / 26의 다른 빌드 | 호환 대상으로 확장했습니다. 시작 시 실제 접촉 입력을 검사한 뒤 사용합니다. 전체 기기·OS 조합의 실기기 동작은 미검증입니다. |
| Intel · 내장 트랙패드 · macOS 14 / 15 / 26 | Universal 앱에 Intel 실행 파일을 포함합니다. 시작 시 입력 검사를 수행하며, Intel 실기기 동작은 미검증입니다. |
| 외장 Apple Magic Trackpad · macOS 14 / 15 / 26 | 연결된 기기의 접촉·클릭 입력이 같은 트랙패드인지 확인하고 시작 시 입력 검사를 통과하면 활성화합니다. 외장 기기의 실기기 동작은 미검증입니다. |
| 그 밖의 macOS 버전 | 트랙패드 접촉 입력을 활성화하지 않습니다. |

한 번에 트랙패드 한 대를 사용하며, 사용 가능한 외장 Magic Trackpad를 우선 선택하고 없으면 내장 트랙패드를 사용합니다. 연결이 바뀌면 기기를 다시 확인합니다. 일반 마우스와 Magic Mouse는 트랙패드 입력으로 사용하지 않습니다. 구형·신형 모델을 이름만으로 허용하지 않으며, 기기의 실제 입력과 연결 관계가 확인되어야 합니다. Force Touch가 없는 기기에서는 압력 기반 제스처를 사용할 수 없습니다.

새 호환 환경과 외장 트랙패드의 입력 확인 중에는 연결된 동작이 실행되지 않습니다. 검사에 실패하면 입력을 중단합니다. 트랙패드 입력은 비공개 MultitouchSupport 프레임워크를 사용하므로 macOS 업데이트 후 재검증이 필요할 수 있습니다.

[릴리스 파일 자동 검사](https://github.com/zamk-DAV/trackpad/actions/workflows/compatibility.yml)는 macOS 14의 Apple silicon, macOS 15·26의 Apple silicon과 Intel에서 체크섬·앱 서명·공증·리소스·실행 파일 구조를 확인합니다. **0.1.1 Beta 1은 [5개 환경 모두 통과](https://github.com/zamk-DAV/trackpad/actions/runs/35547751009)했습니다.** macOS 14 Intel은 이 CI에 포함되지 않습니다. 실제 제스처·권한·블루투스·잠자기 복귀를 검사하는 작업은 아닙니다.

## 주요 기능

| 기능 | 설명 |
| --- | --- |
| 트랙패드 제스처 | 기본 제스처를 고르거나 접촉·탭·이동 순서를 직접 녹화합니다. |
| 시간 설정 | 키보드는 **빠르게 / 기본 / 여유롭게**, 녹화 제스처는 **녹화 기준 / 여유 조금 / 여유 많이**로 시작하고 세부 값을 조절합니다. |
| 키보드 매크로 | 키를 눌렀다 떼는 순서 또는 보조 키 조합에 동작을 연결합니다. |
| 화면 분할 | 키를 누른 채 포인터를 움직여 창을 절반·사분면·최대화로 배치합니다. |
| 여러 동작 연결 | 앱·웹사이트 열기, 창 제어, 키·텍스트 입력 등을 순서대로 실행합니다. |
| 앱별 규칙 | 적용할 앱을 선택하고 인식과 실행을 테스트한 뒤 규칙을 켭니다. |
| 설정과 도움 | 언어 선택, 수동 업데이트 확인, 문의용 진단 정보 복사를 제공합니다. |

![Flicklane 사용 예시](assets/flicklane-demo.gif)

*규칙 목록 → 키보드 빠르게·여유롭게 설정 → 권한 안내의 11초 반복 화면입니다. 예시 설정을 사용하며 실제 입력이나 동작을 실행하지 않습니다.*

한국어·영어·일본어·중국어 간체/번체를 지원합니다. 녹화와 시간 설정은 [사용법](docs/usage.md), 권한을 다시 연결하는 방법은 [설치 안내](docs/installation.md)에 정리했습니다.

## 업데이트와 문의

앱 설정의 **업데이트 확인**을 누르면 GitHub에서 새 릴리스를 확인합니다. 다운로드와 앱 교체는 직접 진행합니다. GitHub **Watch → Custom → Releases**로 공개 소식을 받을 수도 있습니다.

문제는 [Issues](https://github.com/zamk-DAV/trackpad/issues)에 재현 순서와 함께 알려주세요. 설정의 **진단 정보 미리보기 → 진단 정보 복사**를 사용하면 정해진 기술 정보만 복사할 수 있습니다. 입력 인식과 규칙 저장은 Mac에서 처리하며, 업데이트 요청과 진단 정보 범위는 [개인정보 안내](PRIVACY.md)에 설명했습니다.

[♥ 개발 후원](https://buymeacoffee.com/flicklane)은 선택 사항입니다. [후원 안내](SPONSORING.md) · [공유용 소개 문구](docs/share.md)

# Installation

[한국어](installation.md) · **English**

**The first public release is being prepared. There is no installer yet.** These instructions apply once a verified download is available in [Releases](https://github.com/zamk-DAV/trackpad/releases).

## Check compatibility

- An Apple silicon Mac with a built-in trackpad is required. Intel Macs and external Magic Trackpads are not currently supported.
- Trackpad contact recognition is enabled only on macOS builds `25F84` and `25G83`. Run `sw_vers -buildVersion` in Terminal to check your build.
- The app’s minimum installation version, macOS 14.0, is separate from trackpad recognition compatibility. It does not mean contact recognition works on every macOS 14 or later release.

## Install when the release is available

1. Download the app ZIP and `SHA256SUMS` from this repository’s Releases page.
2. In the folder containing both files, run `shasum -a 256 -c SHA256SUMS` to verify the download.
3. Unzip the archive, move `Flicklane.app` to Applications, and open it. Quit an existing copy of Flicklane before updating.
4. Follow the app’s instructions to grant the permissions needed for the features you use. Quit and reopen the app if macOS requests it.
5. Create a rule, test recognition and actions, then enable it.

If macOS blocks the app during security checks, report your macOS version and the message in [Issues](https://github.com/zamk-DAV/trackpad/issues). These instructions do not require disabling system security or removing quarantine attributes.

## Permissions and updates

Input Monitoring detects input; Accessibility supports window, keyboard, and mouse control. Screenshots and control of other apps may require Screen Recording or Automation permission. See the [privacy guide](../PRIVACY.en.md).

If you used the app under its former GestureForge name, do not run both copies at the same time. Rules and recorded gestures keep the same storage location. Replace the app without deleting settings or backups.

[User guide](usage.en.md) · [Home](../README.en.md)

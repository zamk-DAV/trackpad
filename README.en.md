<p align="center">
  <img src="assets/icon.png" width="112" alt="Flicklane app icon">
</p>

# Flicklane

[한국어](README.md) · **English**

**Connect your Mac’s trackpad gestures and keyboard input to the actions you use every day.**

Flicklane is a macOS app for custom recorded gestures, keyboard sequences, shortcuts, and window tiling.

This repository hosts **downloads, documentation, and feedback**. The application source code is not published here.

[User guide](docs/usage.en.md) · [Installation](docs/installation.en.md) · [Releases](https://github.com/zamk-DAV/trackpad/releases) · [Report an issue](https://github.com/zamk-DAV/trackpad/issues) · [♥ Support](https://buymeacoffee.com/flicklane)

## What you can do

| Feature | How it works |
| --- | --- |
| Trackpad gestures | Choose a built-in gesture or record your own sequence of touches, taps, and movements. |
| Adjustable timing | Allow more or less time between touches and adjust the permitted duration of each movement. |
| Keyboard macros | Trigger actions with sequential key presses or a modifier-key combination. |
| Window tiling | Hold a chosen key and move the pointer to place a window in a half, a quarter, or the full desktop area. |
| Multiple actions | Chain actions such as opening apps or websites, managing windows, and entering keys or text. |
| Per-rule settings | Choose the target apps, test recognition and execution, then enable the rule. |
| Languages | Follow the system language or select Korean, English, Japanese, Simplified Chinese, or Traditional Chinese. |
| Menu bar access | ♥ Support, ⚙ Settings, and ⏻ Quit. Settings brings up the main app window. |

## Download

**First public beta: 0.1.0 Beta 1 · build 19 · Apple silicon**

[**Download Flicklane (.zip)**](https://github.com/zamk-DAV/trackpad/releases/download/v0.1.0-beta.1/Flicklane-0.1.0-19-arm64.zip) · [Release notes and checksum](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.0-beta.1)

The app is Developer ID-signed and notarized by Apple. The app extracted from the final ZIP passed signature, notarization-ticket, and Gatekeeper checks. **This is an early beta; validation on other Mac models is still in progress.** Check compatibility, then follow the [installation guide](docs/installation.en.md).

Select **Watch → Custom → Releases** on GitHub for new release notifications.

## Compatibility

- Intended for the **built-in trackpad on Apple silicon Macs**.
- External Magic Trackpads and Intel Macs are not currently supported.
- Contact input is currently enabled only on macOS builds **`25F84` and `25G83`**. This does not mean every macOS version or Mac model has been tested.
- Trackpad input uses the private MultitouchSupport framework and needs validation after macOS updates. Flicklane is not distributed through the Mac App Store.

## Get started

1. Create a new rule in the trackpad or keyboard tab.
2. Select or record the input that should trigger it.
3. Add actions and choose the apps where the rule applies.
4. Test recognition and actions, then enable the rule.

See the [user guide](docs/usage.en.md) for recording and timing details.

To change the language, use the gear button in the main app window and select **Language**. The default follows your system settings; changes apply after restarting. The **Settings** item in the menu bar opens the main app window.

## Feedback and support

Send bug reports and feature ideas through [Issues](https://github.com/zamk-DAV/trackpad/issues). For bugs, include your Mac model, macOS build, app version, and steps to reproduce. Korean and English reports are welcome.

If you would like to support development, visit [Buy Me a Coffee](https://buymeacoffee.com/flicklane). Support is optional. Read the [support page](SPONSORING.md) for more details.

Input recognition and rule storage run locally on your Mac. See the [privacy and permissions guide](PRIVACY.en.md) for details, or use the [Korean and English introduction](docs/share.md) to tell someone about Flicklane.

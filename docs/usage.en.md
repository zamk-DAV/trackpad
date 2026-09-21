# User guide

[한국어](usage.md) · **English**

This guide covers Flicklane 0.1.1 Beta 1. Start with the [installation guide](installation.en.md) to check compatibility and permissions.

## Trackpad gestures

Create a rule in the trackpad tab. Choose a built-in gesture or open the custom gesture recorder.

Input comes from one selected trackpad at a time. An eligible external Magic Trackpad takes priority; otherwise Flicklane uses the built-in trackpad. If asked to validate input after changing connections, briefly place two fingers on the selected trackpad and lift both. Connected actions remain inactive during this check.

Touches, taps, and movement are checked using live device input. Pressure-based gestures require pressure data and are unavailable on older trackpads without Force Touch. A normal click and a force press are different inputs.

Hold `⌘ + ⇧` while performing the gesture. Lift all fingers before releasing the keys to finish recording. Give it a name, save it to the rule, and finish recording/testing.

You can record repeated taps or sequences such as a tap followed by a swipe. A recording can last up to 5 seconds and contain up to 32 steps with up to 5 simultaneous contacts. Flicklane records contact order, positions, and movement paths; it does not identify fingers by names such as index or middle finger.

### Match your pace

Start with **As recorded / A little extra / More extra time**. These presets change both timing values together; you can adjust each value afterward.

| Preset | Added tolerance for both controls |
| --- | --- |
| As recorded | +0 seconds |
| A little extra | +0.3 seconds |
| More extra time | +1 second |

Expand the timing tolerance controls for finer adjustments.

- **Time between touches:** Allow more time between lifting and touching again, or between taps while other fingers stay on the trackpad.
- **Movement duration:** Allow each contact step to be shorter or longer than the recording.

Each control adds 0–3 seconds of tolerance, in 0.05-second increments. Zero means the recording’s default tolerance. The complete gesture must still finish within 5 seconds.

Timing changes saved in the gesture library also apply to rules that use that saved gesture.

## Keyboard macros

- **Sequential input:** Press and release Q, then press W. Release the first key before pressing the second.
- **Key combination:** Hold a modifier while pressing another key, such as Shift + 1.

For sequences, start with **Fast (0.2 seconds) / Default (0.4 seconds) / Relaxed (1 second)**. Presets apply directly to the existing interval setting. Editing it to another value shows a custom setting.

The maximum interval for a sequence is adjustable from 0.01 to 5 seconds. It is measured from one key-down event to the next. Faster input within the selected maximum is also accepted.

Key input also reaches the app you are using. Choose combinations that do not conflict with your normal typing.

## Window tiling

Enable window tiling and choose its trigger key. Select the window, hold the key, move the pointer, then release the key.

- Center: maximize within the current desktop.
- Up, down, left, or right: half of the screen.
- Diagonals: a quarter of the screen.

Starting a click, drag, or scroll cancels the selection. An app’s minimum window size may affect the final dimensions.

## Test and manage rules

Configure the input, add actions, then choose where to apply and test the rule. Actions run from top to bottom. Use each action’s more menu to reorder or remove it.

Recognition-only testing does not execute actions. An action test runs the actions once after a 3-second delay, so switch to the intended target window first. Use the management menu beside the rule’s enable switch to duplicate, rename, or delete a rule.

## Settings, updates, and diagnostics

![Flicklane settings](../assets/flicklane-settings.png)

*Actual app UI with example settings, input monitoring and action execution disabled. These images do not demonstrate physical trackpad testing.*

Open settings with the gear button at the top right of the main window.

- **Check for Updates:** Queries GitHub releases only when you press the button. Download a new version from the linked release page. Updates are not installed automatically.
- **Preview Diagnostics → Copy Diagnostics:** Review the app version, macOS version/build, CPU architecture, Mac model, language, permissions, and input status before copying them to the clipboard. Rules, input history, and file paths are excluded. Nothing is sent automatically.

If an update check fails, check your internet connection and try again. If GitHub limits requests, wait before retrying. Report problems in [Issues](https://github.com/zamk-DAV/trackpad/issues) with steps to reproduce.

## Language and menu bar

Use the gear button at the top right of the main window, then choose Language. Options include the system setting, Korean, English, Japanese, Simplified Chinese, and Traditional Chinese. Restart to apply a change; finish recording or testing first.

The Flicklane menu bar icon contains three items:

- **♥ Support:** Open the [support page](https://buymeacoffee.com/flicklane) in your default browser.
- **⚙ Settings:** Open the main app window, or return to it if it is already open.
- **⏻ Quit:** Close the app.

[Home](../README.en.md) · [Installation](installation.en.md) · [Privacy](../PRIVACY.en.md)

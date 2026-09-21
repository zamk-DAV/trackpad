# User guide

[한국어](usage.md) · **English**

This guide covers **Flicklane 0.1.3 Beta 1 · build 22**. Start with the [installation guide](installation.en.md) to check compatibility and permissions.

[Trackpad](#trackpad-gestures) · [Keyboard](#keyboard-macros) · [Quick Menu](#quick-menu) · [Window Layout](#window-tiling) · [Troubleshooting](#troubleshooting)

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

## Quick Menu

Open the fourth feature tab, **Quick Menu**, at the top of the main window. Changes are saved as you make them.

1. Choose a layout with 4, 5, 8, or 9 positions.
2. Click a position in the circular layout and select **Change action**. Complete any required parameters, such as the target app for an Open App action.
3. Enter a custom display title, or leave it blank to use the action name.
4. Use **Preview menu** to try selecting an item. Preview selections do not execute actions.
5. Turn on **Enable Quick Menu** and choose an **Activation key**. Select Fn / 🌐, Control, Option, Shift, or Command, or use **Specify another key**. A new configuration starts with dedicated-key activation off and Control selected.

| Layout | Available positions | Releasing the key at the center |
| --- | --- | --- |
| 4 | Up, down, left, right | Cancels |
| 5 | Four directions + center | Runs the center action |
| 8 | Four directions + diagonals | Cancels |
| 9 | Eight directions + center | Runs the center action |

Switching layouts preserves the titles and actions of hidden positions. For example, switching from 9 to 4 and back restores your diagonal and center assignments.

### Open with a key or a rule

- **Activation key:** In the app you want to work with, hold the key, move toward an item, and release. With 5 or 9 positions, releasing without moving can run the center action; check its assignment first.
- **Trackpad or keyboard rule:** Add **Open Quick Menu** to the rule's actions. Choose an item by clicking. This route works without enabling the dedicated activation key.
- **Cancel:** Press Escape or switch to another app. Clicking, dragging, or scrolling also cancels a menu opened by holding a key.

The chosen action targets the app that was active when the menu opened and uses that action's permission and confirmation requirements. Nesting **Open Quick Menu** inside another Quick Menu item is not supported.

### Fn and activation-key conflicts

**Window Layout takes priority** if both features use the same activation key. For example, use Fn for Quick Menu and Option for Window Layout. Ordinary character keys also reach the app you are using.

Fn is different from a function key such as F1. macOS may also open emoji or change input sources when Fn / 🌐 is pressed. To stop that behavior, choose **System Settings → Keyboard → Press fn / 🌐 key to → Do Nothing**. Flicklane does not change this system preference automatically. [Apple keyboard settings](https://support.apple.com/guide/mac-help/keyboard-settings-kbdm162/mac)

## Window tiling

In **Window Layout**, enable the feature and choose Fn / 🌐, a modifier, or another activation key. Select the window, hold the key, move the pointer, then release the key.

- Center: maximize within the current desktop.
- Up, down, left, or right: half of the screen.
- Diagonals: a quarter of the screen.

Starting a click, drag, or scroll cancels the selection. An app’s minimum window size may affect the final dimensions.

## Test and manage rules

Configure the input, add actions, then choose where to apply and test the rule. Actions run from top to bottom. Use each action’s more menu to reorder or remove it.

Recognition-only testing does not execute actions. An action test runs the actions once after a 3-second delay, so switch to the intended target window first. Use the management menu beside the rule’s enable switch to duplicate, rename, or delete a rule.

## Settings, updates, and diagnostics

Open settings with the gear button at the top right of the main window.

- **Check for Updates:** Queries GitHub releases only when you press the button. Download a new version from the linked release page. Updates are not installed automatically.
- **Preview Diagnostics → Copy Diagnostics:** Review the app version, macOS version/build, CPU architecture, Mac model, language, Input Monitoring/Accessibility/Screen Recording permissions, and trackpad input status before copying them to the clipboard. Rules, input history, and file paths are excluded. Nothing is sent automatically.

If an update check fails, check your internet connection and try again. If GitHub limits requests, wait before retrying. Report problems in [Issues](https://github.com/zamk-DAV/trackpad/issues) with steps to reproduce.

## Language and menu bar

Use the gear button at the top right of the main window, then choose Language. Options include the system setting, Korean, English, Japanese, Simplified Chinese, and Traditional Chinese. Restart to apply a change; finish recording or testing first.

The Flicklane menu bar icon contains three items:

- **♥ Support:** Open the [support page](https://buymeacoffee.com/flicklane) in your default browser.
- **⚙ Settings:** Open the main app window, or return to it if it is already open.
- **⏻ Quit:** Close the app.

## Cancellation and text input

Cancelling a region/window capture with Escape, or declining an action confirmation, stops the remaining actions in that execution. Completed actions are not undone. Explicit cancellation takes precedence over the continue-after-error setting.

Text input preserves emoji and supplementary Unicode characters across event boundaries. Cancellation stops remaining actions; it does not undo text already entered or work already completed.

## Troubleshooting

| Symptom | What to check |
| --- | --- |
| Window Layout opens instead of Quick Menu | Give the two features different activation keys. |
| Fn also opens emoji | Check the macOS keyboard behavior described in the Fn section above. |
| A menu opens but its action does not run | Check whether it is a preview, then verify the action's target, parameters, and permissions. Switching apps while the menu is open cancels it. |
| Capture fails after allowing permission | Check **Input Status and Permissions → Screen Recording**, then follow [permission recovery](installation.en.md#if-permission-is-allowed-but-not-detected). |
| Actions after a cancelled capture do not run | This is intentional in 0.1.3: the remaining actions in that execution stop. |
| Fast or slow key sequences are not recognized | Release the first key before the next and adjust the maximum interval. |
| Trackpad input remains pending | Place two fingers on the selected trackpad, then lift both. Check permissions and the device connection. |

If the problem remains, [report a bug](https://github.com/zamk-DAV/trackpad/issues/new?template=bug_report.yml) with the feature and steps. Attach only diagnostics you have reviewed, if needed.

[Home](../README.en.md) · [Installation](installation.en.md) · [Privacy](../PRIVACY.en.md)

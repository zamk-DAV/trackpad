# User guide

[한국어](usage.md) · **English**

This guide covers **Flicklane 0.1.6 Beta 1 · build 25**. Start with the [installation guide](installation.en.md) to check compatibility and permissions.

[Gesture](#gestures) · [Keyboard](#keyboard-macros) · [Quick Menu](#quick-menu) · [Window Layout](#window-tiling) · [Mouse Sensitivity](#mouse-sensitivity) · [Troubleshooting](#troubleshooting)

## Gestures

Create a rule in the **Gesture** tab. Choose a built-in gesture or open the custom gesture recorder.

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

### Configure the trigger and output separately

The **input setting** starts the macro. Its **actions** send keys or text to the app you are working in.

1. Create a rule in Keyboard Macros and choose a trigger, such as **Key combination → Shift+A**.
2. Choose **Add action → Type text** and enter `youtube.com`. This types at the current insertion point; it does not open the URL. Add a separate Enter key action if needed.
3. To send an app shortcut, choose **Add action → Press keys or shortcuts → Record output keys**, then press the desired keys. Use a single key such as `V`, `[`, or `]`, or a combination such as `⌘C` or `⌘⇧S`. Recording output does not change the trigger.
4. Arrange actions from top to bottom and choose the applicable app. Use the action test in the intended window, then enable the rule.

Other input recognition pauses while recording output keys. Cancel or switch apps to stop recording. Execution uses macOS keyboard events, so results depend on the target app's shortcut settings and focus. Behavior has not been verified in every app, including Photoshop. **Type text** sends Unicode characters; use **Press keys or shortcuts** for app tools and commands.

## Quick Menu

Open the fourth feature tab, **Quick Menu**, at the top of the main window. Changes are saved as you make them.

1. Choose a layout with 4, 5, 8, or 9 positions.
2. Select a position and choose **Linked action**. For **Single action**, use **Change action** and fill in required parameters. Choose a saved keyboard macro to run its action sequence.
3. Enter a custom display title, or leave it blank to use the action or macro name.
4. Use **Preview menu** to try selecting an item. Preview selections do not execute actions.
5. Turn on **Enable Quick Menu** and choose an **Activation key**. Select Fn / 🌐, Control, Option, Shift, or Command, or use **Specify another key**. A new configuration starts with dedicated-key activation off and Control selected.

| Layout | Available positions | Releasing the key at the center |
| --- | --- | --- |
| 4 | Up, down, left, right | Cancels |
| 5 | Four directions + center | Runs the center action |
| 8 | Four directions + diagonals | Cancels |
| 9 | Eight directions + center | Runs the center action |

Switching layouts preserves the titles and actions of hidden positions. For example, switching from 9 to 4 and back restores your diagonal and center assignments.

### Link a rule from Keyboard Macros

Choose **Quick Menu → a position → Linked action → a saved keyboard macro**. It runs the original rule's enabled actions in order and follows its stop/continue-on-error setting. Changes to the original name and actions apply on subsequent use. A custom display title remains unchanged.

Enable the original rule and its preset, and select the preset if your configuration requires it. App-specific scope must match the app where the menu opened. Deleted or disabled rules, unavailable presets, and rules with no enabled actions do not run; the editor shows an explanation. A rule containing **Open Quick Menu** cannot run from a menu slot.

Selecting a slot executes the saved action list rather than simulating the rule's trigger. Keyboard activation and Quick Menu therefore use the same action configuration when you edit the macro.

### Open with a key or a rule

- **Activation key:** In the app you want to work with, hold the key, move toward an item, and release. With 5 or 9 positions, releasing without moving can run the center action; check its assignment first.
- **Trackpad or keyboard rule:** Add **Open Quick Menu** to the rule's actions. Choose an item by clicking. This route works without enabling the dedicated activation key.
- **Cancel:** Press Escape or switch to another app. Clicking, dragging, or scrolling also cancels a menu opened by holding a key.

The chosen action targets the app that was active when the menu opened and uses that action's permission and confirmation requirements. Nesting **Open Quick Menu** inside another Quick Menu item is not supported.

### Fn and activation-key conflicts

**Window Layout takes priority** if both features use the same activation key. For example, use Fn for Quick Menu and Option for Window Layout. Ordinary character keys also reach the app you are using.

Fn is different from a function key such as F1. macOS may also open emoji or change input sources when Fn / 🌐 is pressed. To stop that behavior, choose **System Settings → Keyboard → Press fn / 🌐 key to → Do Nothing**. Flicklane does not change this system preference automatically. [Apple keyboard settings](https://support.apple.com/guide/mac-help/keyboard-settings-kbdm162/mac)

## Window tiling

Enable **Window Layout** and choose an activation key. Select the target window, hold the key, move toward a position in the circular menu, then release. Fn / 🌐, modifiers, and a custom key are supported.

The default center maximizes; cardinal directions use halves and diagonals use quarters. Click a position in the settings preview and change its layout to configure all nine slots. Turn off **Show action names in menu** for an icon-focused view; the selected action and apply/restore hint remain in the center. Appearance follows macOS light/dark mode.

Options include halves, a centered half, quarters, thirds and two-thirds, four columns, six cells, maximize, almost maximize, maximize height, center/edge/corner movement, larger/smaller, and restore. A position can also be left unassigned.

**Repeat the same placement on the same window to restore its earlier position and size.** For example, run Left Half twice to return to the original window frame. Larger and Smaller adjust the size each time; use **Restore** to undo those changes.

The settings preview does not move real windows. Starting a click, drag, or scroll cancels the live menu. An app's minimum window size can affect the final dimensions.

## Mouse Sensitivity

Open **Mouse Sensitivity** in the main window's top navigation bar. Defaults preserve scrolling and leave pointer customization off. Separate mouse and trackpad profiles apply to connected devices of that type, including devices connected later.

1. Choose **Mouse** or **Trackpad**, then select **Follow macOS / Natural scrolling / Standard scrolling** scrolling.
2. Enable **Automatically reverse scrolling for external devices** to reverse identified external mice and trackpads relative to macOS. It overrides the profile's manual direction without reversing twice. The built-in trackpad retains its own setting.
3. Enable **Customize pointer settings** on supported devices to adjust speed/acceleration or disable acceleration. Supported linear mode keeps speed adjustable. Legacy acceleration-off modes ignore the speed multiplier, so the speed control is disabled.
4. If **Not applied** appears, choose **Open macOS pointer settings** to adjust system tracking speed. Direct control does not apply to the built-in Apple trackpad tested locally; this release does not fix that limitation. Scroll direction is a separate feature.
5. Reset the profile or turn customization off to restore values changed by Flicklane. Normal quit also attempts restoration; after an interrupted exit, the next launch attempts recovery of remaining changes.

New devices connected through a dock or USB receiver are discovered automatically. Use **Refresh devices** if the list has not updated.

Unidentified devices and scrolling events are passed through without guessing their origin. Available settings depend on the driver and macOS. Using another utility to adjust the same settings can change the result.

## Hands-on guides

Open **How to Use** in Gesture, Keyboard Macros, Window Layout, or Quick Menu to try the examples directly. Practice does not modify saved rules or move another app's windows. Configure permissions and activation keys separately before using the real feature.

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
| A linked macro does not run | Check the original rule, preset, app scope, and enabled actions. Reassign a deleted rule. |
| Capture fails after allowing permission | Check **Input Status and Permissions → Screen Recording**, then follow [permission recovery](installation.en.md#if-permission-is-allowed-but-not-detected). |
| Actions after a cancelled capture do not run | This behavior was introduced in 0.1.3: the remaining actions in that execution stop. |
| Fast or slow key sequences are not recognized | Release the first key before the next and adjust the maximum interval. |
| Changing speed has no effect | Check that pointer customization is enabled. For “Not applied”, use macOS pointer settings. Legacy acceleration-off modes ignore speed adjustments. |
| External scroll reversal has no effect | Update to 0.1.6, then refresh devices and check the device list and permissions in Mouse Sensitivity. Events whose origin cannot be identified are unchanged. |
| Trackpad input remains pending | Place two fingers on the selected trackpad, then lift both. Check permissions and the device connection. |

If the problem remains, [report a bug](https://github.com/zamk-DAV/trackpad/issues/new?template=bug_report.yml) with the feature and steps. Attach only diagnostics you have reviewed, if needed.

[Home](../README.en.md) · [Installation](installation.en.md) · [Privacy](../PRIVACY.en.md)

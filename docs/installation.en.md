# Installation

[한국어](installation.md) · **English**

[**Download Flicklane 0.1.1 Beta 1**](https://github.com/zamk-DAV/trackpad/releases/download/v0.1.1-beta.1/Flicklane-0.1.1-20-universal.zip) · build 20 · Apple silicon + Intel

## Install in three steps

1. Download and unzip the app.
2. Move `Flicklane.app` to **Applications** and open it. Quit the existing copy before updating.
3. Follow the permission prompts and create a rule. If prompted to check input, **place two fingers briefly, then lift both fingers.** Reopen the app if macOS requests it.

On first launch, macOS may ask whether to open an app downloaded from the internet. If a security check blocks the app, report your macOS version and the message in [Issues](https://github.com/zamk-DAV/trackpad/issues).

## Compatibility

Targets are Apple silicon and Intel Macs using a **built-in trackpad or external Apple Magic Trackpad** on macOS **14, 15, or 26**. Contact and click input must be attributable to the same device, and startup input validation must pass. Trackpad input remains disabled on other macOS versions or when the device cannot be verified.

An eligible external Magic Trackpad takes priority; otherwise Flicklane uses the built-in trackpad. Only one device is active at a time. External devices are discovered over USB and Bluetooth, but connections and features have not been physically tested across every generation. Pressure-based gestures are unavailable on devices without Force Touch.

Existing local hardware validation covers Apple silicon on builds `25F84` and `25G83`. Other target environments check live contact data at startup. **Including an Intel executable and checking live input does not mean Intel hardware validation is complete.** See the [compatibility table](../README.en.md#compatibility).

The input check completes after two-finger contact and lifting all fingers. Connected actions remain inactive during the check. Repeat it on the selected trackpad if prompted after restarting, waking your Mac, or changing device connections. If validation fails, check permissions and the macOS version, then use diagnostics when reporting the issue.

## Permissions

![Flicklane permission screen](../assets/flicklane-permissions.png)

*Actual app UI with example settings, input monitoring and action execution disabled. These images do not demonstrate physical trackpad testing.*

- **Input Monitoring:** Detect trackpad and keyboard input.
- **Accessibility:** Window, keyboard, and mouse actions.
- **Screen Recording / Automation:** When needed for screenshots or control of another app you configure.

See the [privacy guide](../PRIVACY.en.md) for details.

### If permission is allowed but not detected

Check **Input Status and Permissions** in the app. A development build or an earlier signature can leave an outdated permission entry in macOS.

1. Quit Flicklane and open the relevant permission list under System Settings → Privacy & Security.
2. Remove the old Flicklane entry with `−`, then use `+` to add the **current Flicklane.app in Applications** and allow it.
3. Complete any Touch ID or password request yourself, then reopen the app.

You do not need to delete settings or backups. Do not run the former GestureForge app and Flicklane at the same time.

## Updates

Select **Check for Updates** in settings to query GitHub releases. If a new version is available, download it from the linked release page, quit Flicklane, and replace the app. Flicklane does not install updates automatically or upload your settings.

Rules and recorded gestures retain their existing storage location. Earlier betas remain listed under [all releases](https://github.com/zamk-DAV/trackpad/releases).

<details>
<summary>Optional: verify the download checksum</summary>

Download the ZIP and `SHA256SUMS` from the [same release](https://github.com/zamk-DAV/trackpad/releases/tag/v0.1.1-beta.1) into one folder, then run in Terminal:

```sh
shasum -a 256 -c SHA256SUMS
```

Check that the ZIP is reported as `OK`.

</details>

[User guide](usage.en.md) · [Home](../README.en.md)

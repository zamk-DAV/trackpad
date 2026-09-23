# Privacy and permissions

[한국어](PRIVACY.md) · **English**

Flicklane processes input recognition and stores rules on your Mac.

## Permissions

| Permission | Used for |
| --- | --- |
| Input Monitoring | Detecting trackpad and keyboard input, and scroll settings |
| Accessibility | Window, keyboard, and mouse actions |
| Screen Recording | Screenshot actions |
| Automation | Controlling other apps through actions you configure |

Required permissions depend on the features you use. Revoke them in macOS System Settings. If a permission is not detected correctly, see the [permission repair guide](docs/installation.en.md#if-permission-is-allowed-but-not-detected).

## Local settings

Rules and recorded gestures are stored in `~/Library/Application Support/GestureForge/configuration.json`. Up to 10 rotating backups are kept in the same folder. Uninstalling the app does not automatically delete this folder.

Quick Menu layouts, activation keys, item titles and actions, linked keyboard macro identifiers, Window Layout slot bindings and label visibility, mouse/trackpad sensitivity and scroll settings, and language selection are stored separately in macOS app preferences. The JSON file and rotating backups above do not include these preferences. Replacing the app reuses the existing preferences.

A linked macro’s actions are read from the rules JSON. Preserve both the rules and app preferences to restore menu links; the rules JSON alone is not a complete Quick Menu backup.

Settings may contain rule names, key combinations, app identifiers, URLs, text, file paths, and commands. Do not put passwords or API keys in action settings.

Pointer restoration temporarily stores changed device service identifiers and their original/applied property values in app preferences. Completed entries are removed; failed restorations remain for recovery. This journal contains no typed content or browsing history and is not uploaded.

## Manual update checks

Pressing **Check for Updates** requests this repository’s public release list from `api.github.com`. Flicklane does not check periodically in the background or install updates automatically.

GitHub receives your connection IP address and ordinary request metadata. The request includes the `Flicklane-Update-Check` User-Agent and API format/version headers. Rules, configuration files, input history, and clipboard contents are not uploaded. Comparing your installed version with the available releases happens locally on your Mac.

Opening a release page or downloading a file creates the usual browser and GitHub network requests.

## Copying diagnostics

**Preview Diagnostics** includes only these defined fields:

- App version and build.
- macOS version/build, CPU architecture, and Mac model identifier.
- App language.
- Input Monitoring, Accessibility, and Screen Recording permission states, and trackpad input status.

It excludes rule names and contents, key input history, URLs, personal file paths, commands, and raw detailed error messages. Review the preview and select **Copy Diagnostics** to put it on the clipboard. Nothing is sent automatically; you choose whether to paste it into a report.

## External actions and reports

Websites, apps, and commands you configure may connect to the network. Clipboard, screenshot, and file actions affect the targets you select.

GitHub Issues are public. Do not upload complete settings files, private URLs, passwords, or personal information from your screen. Share only the information needed to reproduce the issue.

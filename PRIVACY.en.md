# Privacy and permissions

[한국어](PRIVACY.md) · **English**

Flicklane processes input recognition and stores rules on your Mac.

## Permissions

| Permission | Used for |
| --- | --- |
| Input Monitoring | Detecting trackpad and keyboard input |
| Accessibility | Window, keyboard, and mouse actions |
| Screen Recording | Screenshot actions |
| Automation | Controlling other apps through actions you configure |

Required permissions depend on the features you use. You can revoke them in macOS System Settings.

## Local settings

Rules and recorded gestures are stored in `~/Library/Application Support/GestureForge/configuration.json`. Up to 10 rotating backups are kept in the same folder. Uninstalling the app does not automatically delete this folder.

Settings may contain rule names, key combinations, app identifiers, URLs, text, file paths, and commands. Do not put passwords or API keys in action settings.

## External actions and reports

Websites, apps, and commands you configure may connect to the network. Clipboard, screenshot, and file actions affect the targets you select.

GitHub Issues are public. Do not upload complete settings files, private URLs, passwords, or personal information from your screen. Share only the information needed to reproduce the issue.

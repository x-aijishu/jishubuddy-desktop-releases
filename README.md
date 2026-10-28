# JishuBuddy Desktop

A desktop workspace for conversations with your AI models, tools, and local JishuBuddy runtime.

[Download releases](https://github.com/x-aijishu/jishubuddy-desktop-releases/releases)

This repository provides product information, signed installers, release notes, and update metadata.
Application source code is maintained separately.

## What you can do

- Chat with configured model providers and restore conversation history.
- Rename, pin, archive, search, and manage conversations.
- Review tool approval requests and answer follow-up questions.
- Add supported attachments and switch models through the desktop interface.
- Configure providers, inspect connection status, and open local diagnostic logs.

## macOS installation

JishuBuddy currently supports Apple Silicon Macs running macOS 13 or later.

1. Download the DMG from a release marked stable.
2. Open the DMG and copy JishuBuddy to Applications.
3. Launch JishuBuddy and configure your model provider when prompted.

The installer bundles its required local runtime. Signed releases use the shared AIJISHU publisher
identity and Apple notarization. SHA-256 checksums accompany the release assets.

## Updates

Update-enabled versions check for new releases and show their status under **Settings → About**.
Downloading and restarting to install require your action. The application checks for active work
before quitting. Closing a window does not quit the macOS application.

A local acceptance build may have automatic updates disabled. Its About page reports that state;
install an update-enabled release to join the stable channel.

## Preferences and data

Login startup is off by default and can be enabled under **Settings → General**.
Desktop telemetry and crash uploads are disabled. Requests to a configured model provider follow
that provider's connection settings; disabling telemetry does not turn a cloud model into a local model.

Keep a backup of your local data before manual downgrade or recovery. Older runtimes may reject data
written by newer versions. Follow the recovery notes for the exact release instead of replacing files
inside an installed application bundle.

## Release assets

- `JishuBuddy-<version>-arm64.dmg`: manual macOS installer.
- `JishuBuddy-<version>-arm64.zip`: updater payload.
- ZIP blockmap: differential download metadata.
- `latest-mac.yml`: stable update metadata.
- `SHA256SUMS`: checksums for the published assets.

Prereleases are for acceptance testing. Use stable releases for normal installation.

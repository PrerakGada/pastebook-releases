# Pastebook

A clipboard manager for macOS. Everything you copy goes on a shelf one shortcut away (⌃⌥X by default): search
it, pin it to pinboards, and paste any of it back. It also has an encrypted vault for passwords, bank details and
documents (unlocked with a password or Touch ID), pause and incognito modes, optional sync between your Macs
through iCloud Drive, and a one-off import of an existing clipboard history.

This repository only holds the signed downloads. Website: <https://pastebook.prerakgada.in/>

## This is an alpha

Pastebook 0.1.2 is the third alpha. It is signed and notarized by Apple and passes its own automated checks,
and has been used day to day by one person so far. Expect rough edges, and keep a second copy of anything you cannot lose.
There is no in-app updater in this version.

## Requirements

- A Mac with Apple Silicon (M1 or later)
- macOS 26 or newer

## Install

With Homebrew:

```sh
brew install --cask prerakgada/tap/pastebook
open -a Pastebook
```

Homebrew also links the `pastebook` command-line tool.

Or [download the DMG](https://github.com/PrerakGada/pastebook-releases/releases/download/v0.1.2/Pastebook-0.1.2.dmg):

1. Open the downloaded disk image.
2. Drag **Pastebook** onto the **Applications** shortcut.
3. Open Pastebook from Applications, then eject the disk image.

Checksums (SHA-256) are attached to every [release](https://github.com/PrerakGada/pastebook-releases/releases).

## Permissions

Pastebook asks for nothing when it starts. Each permission is requested only when you press its button in the
welcome window or in Settings:

- **Clipboard access** ("Paste from Other Apps" in System Settings), so it can save what you copy.
- **Accessibility**, only if you want it to paste straight into the app you were using. Without it, Pastebook
  copies the item and you press ⌘V yourself.

## Privacy

Your history stays on your Mac, in `~/Library/Application Support/Pastebook`. Pastebook has no account, no
analytics and no telemetry. It only uses the network for features you switch on (iCloud Drive sync, link titles), and
when you send feedback yourself: a message goes only when you press Send, with what you typed plus the app and macOS
versions and the Mac model. The server notes a rough location (country, region and city) from your connection and
stores no IP address.

## Uninstall

```sh
brew uninstall --cask pastebook          # or drag Pastebook.app to the Bin
brew uninstall --zap --cask pastebook    # also removes its saved history and settings
```

---

© 2026 Engaze

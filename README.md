# Shortcut Map

**[shortcut-map.epel.us →](https://shortcut-map.epel.us/)**

A macOS menu bar app that shows every keyboard shortcut currently mapped on your Mac, grouped by
application, and exports the lot to PDF or PNG. No Dock icon, no main window — one menu bar icon
and an overlay you summon with <kbd>⌥⌘/</kbd>.

## Install

```sh
curl -fsSL https://github.com/dharmaje/shortcut-map/releases/download/latest/install.sh | sh
```

Shortcut Map is ad-hoc signed rather than notarized, because there is no paid Apple Developer
account behind it. Anything a *browser* downloads gets macOS's quarantine flag, and for an
unnotarized app that ends in a Gatekeeper dialog with no way through. Files fetched by `curl` are
never quarantined, so installing from Terminal avoids the problem rather than fighting it.

On first launch, grant Accessibility access — the app reads the menu bars of running applications
to find their shortcuts, and shows very little without it.

**Requirements:** macOS 14 or later, Apple silicon.

## Update

Run the install command again — it always installs the newest build.

## Uninstall

```sh
curl -fsSL https://github.com/dharmaje/shortcut-map/releases/download/latest/uninstall.sh | sh
```

Or use **Uninstall Shortcut Map…** in the menu bar icon's menu, or just drag the app to the Trash
(which leaves behind `~/Library/Application Support/ShortcutMap/` and
`~/Library/Preferences/us.epel.ShortcutMap.plist` — the uninstaller removes both).

## What it reads

Menu item titles and their key equivalents, from running applications, over the Accessibility API;
the system hotkeys in `com.apple.symbolichotkeys`; and your own customizations from System
Settings. It does not read keystrokes and does not watch what you type.

The one network request it makes is a daily check for a newer release, which can be switched off in
the menu bar — with it off, the app makes no network requests at all.

## Releases and feedback

This repository carries the published builds and the website. Bug reports and feature requests are
welcome here — note that **GitHub requires a free account to open an issue**; anonymous reports
are not possible.

- [Report a bug](https://github.com/dharmaje/shortcut-map/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/dharmaje/shortcut-map/issues/new?template=feature_request.yml)

MIT licensed.

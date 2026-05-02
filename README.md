<div align="center">

<a href="https://github.com/Bonevil-ca/runyard-releases/releases/latest"><img src="https://bonevil.ca/assets/runyard-icon.png" width="180" height="180" alt="Runyard" /></a>

<h1>Runyard</h1>

<p><strong>Your entire dev stack, one menu bar click away.</strong></p>

<p>A macOS menu bar app that orchestrates your local development environment. Start, stop, and monitor all your services — backends, frontends, databases, proxies — from a single dropdown. No more juggling terminal tabs.</p>

<p>
  <a href="https://github.com/Bonevil-ca/runyard-releases/releases/latest"><img src="https://img.shields.io/github/v/release/Bonevil-ca/runyard-releases?style=for-the-badge&label=Download&color=06b6d4" alt="Download latest release" /></a>
</p>

<sub>
Requires macOS 14 Sonoma or later · Apple Silicon &amp; Intel · <a href="https://github.com/Bonevil-ca/runyard-releases/releases">Browse all releases</a>
</sub>

<br /><br />

<a href="https://github.com/Bonevil-ca/runyard-releases/releases"><img src="https://img.shields.io/github/downloads/Bonevil-ca/runyard-releases/total.svg?style=flat&color=blue" alt="Total downloads" /></a>
<a href="https://github.com/Bonevil-ca/runyard-releases/releases/latest"><img src="https://img.shields.io/github/v/release/Bonevil-ca/runyard-releases.svg?style=flat&color=blue&label=latest" alt="Latest version" /></a>
<a href="https://bonevil.ca/runyard"><img src="https://img.shields.io/badge/platform-macOS-lightgrey.svg?style=flat&color=blue" alt="Platform: macOS" /></a>
<a href="https://bonevil.ca/runyard"><img src="https://img.shields.io/badge/locales-EN%20%7C%20FR-blue?style=flat" alt="Locales: English, Français" /></a>

</div>

<br />

## About Runyard

Runyard runs in your menu bar (no dock icon) and manages the processes that make up your dev stack. You describe your tools in a single `config.json` file, and Runyard handles the rest: spawning processes in the right order, polling HTTP/TCP health checks, surfacing live status, and shutting everything down cleanly when you're done.

It's not Electron, not a wrapper, not a webview — just native Swift and AppKit, designed to stay out of your way until you need it.

<div align="center">
<a href="https://bonevil.ca/runyard"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-1-full.jpg" alt="Runyard menu bar — start, stop, and monitor your dev stack" width="560" /></a>
</div>

## Key Features

- **One-click orchestration** — start your entire stack with one click; sequential startup with `waitFor` dependencies makes sure services launch in the right order.
- **Health monitoring** — HTTP and TCP health checks with a real-time state machine (running, starting, stopped, failing, paused).
- **Auto port detection** — Runyard reads each process's listening port from the OS and shows it next to the tool name; URLs and health checks support `{{port}}` placeholders so your config works regardless of which port the dev server picks.
- **Probes** — standalone HTTP/TCP watchers that surface failures in the menu without managing a process.
- **Custom actions** — open URLs, run shell commands, execute AppleScripts, or reveal files. Scope each action to `running`, `stopped`, or `always` visibility.
- **Shortcuts and groups** — flat quick-action lists or nested submenus to organize your stack the way you think about it.

  <div align="center"><a href="https://runyard.app"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-2-full.jpg" alt="Runyard settings — group links, actions, and services" width="560" /></a></div>

- **Install hooks** — auto-run `npm install` (or any command) when dependencies are missing.
- **Custom shutdown** — define `stopCommands` for tools that need a graceful stop (e.g. `docker-compose down`) instead of SIGTERM.

  <div align="center"><a href="https://runyard.app"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-3-full.jpg" alt="Runyard advanced settings — health checks, timeouts, and graceful shutdowns" width="560" /></a></div>

- **Per-process logs** — every process writes to `~/Library/Logs/Runyard/`, openable straight from the menu.
- **Sync across Macs** — point your config at iCloud Drive or Dropbox to share the same stack across machines.
- **Bilingual UI** — English and Français, follows your macOS language setting.
- **In-app updates** — Sparkle 2 with EdDSA-signed releases.

<div align="center">

<a href="https://runyard.app"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-4-full.jpg" alt="Runyard JSON configuration — config as code" width="560" /></a>

<sub><strong>Config as code. No magic.</strong> One JSON file to rule your entire stack.</sub>

</div>

## Installation

1. Download the [latest `.dmg`](https://github.com/Bonevil-ca/runyard-releases/releases/latest).
2. Open it and drag **Runyard** to your `Applications` folder.
3. Launch from Launchpad or Spotlight. The icon will appear in your menu bar.
4. On first launch, Runyard creates a starter `config.json` at `~/Library/Application Support/Runyard/`. Open it from the menu bar dropdown via **Edit Configuration** to define your stack.

Updates are delivered automatically through Sparkle. You can also check manually via **Check for Updates…** in the menu bar dropdown or the **About** tab.

## Documentation

The full user guide lives at **[runyard.app/docs](https://runyard.app/docs/)**.

- [Getting Started](https://runyard.app/docs/getting-started)
- [Menu Bar Guide](https://runyard.app/docs/menu-bar-guide)
- [Settings Window](https://runyard.app/docs/settings-window)
- [`config.json` Reference](https://runyard.app/docs/config-reference)
- [Troubleshooting](https://runyard.app/docs/troubleshooting)

Français : **[runyard.app/fr/docs](https://runyard.app/fr/docs)**

## Compatibility

- **macOS 14 Sonoma or later** (Apple Silicon and Intel).
- Distributed with Developer ID signing, notarized by Apple, and Hardened Runtime enabled.
- Not sandboxed — Runyard spawns user-supplied binaries (npm, docker, mix, fly, etc.), which is structurally incompatible with the App Sandbox. It is not available on the Mac App Store for the same reason.

## Support & Feedback

- **Bug reports & feature requests** — [open an issue](https://github.com/Bonevil-ca/runyard-releases/issues) on this repo.
- **Email** — [support@bonevil.ca](mailto:support@bonevil.ca).
- **Website** — [runyard.app](https://runyard.app).

## About this repository

This repository is the **public release channel** for Runyard. It hosts:

- Signed, notarized `.dmg` builds attached to each [GitHub Release](https://github.com/Bonevil-ca/runyard-releases/releases).
- The issue tracker for bug reports and feature requests.

## Legal

- [Privacy Policy](https://runyard.app/privacy-policy)
- [Terms of Use](https://runyard.app/terms-of-use)

<div align="center">
<sub>© 2026 Bonevil. Made in Montréal.</sub>
</div>

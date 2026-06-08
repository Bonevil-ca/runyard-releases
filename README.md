<div align="center">

<a href="https://github.com/Bonevil-ca/runyard-releases/releases/latest"><img src="https://bonevil.ca/assets/runyard-icon.png" width="180" height="180" alt="Runyard" /></a>

<h1>Runyard</h1>

<p><strong>Your entire dev stack, one menu bar click away.</strong></p>

<p>A macOS menu bar app that orchestrates your local development environment. Start, stop, and monitor all your services — backends, frontends, databases, proxies — from a single dropdown. No more juggling terminal tabs.</p>

<p>
  <a href="https://github.com/Bonevil-ca/runyard-releases/releases/latest/download/Runyard.dmg"><img src="https://img.shields.io/github/v/release/Bonevil-ca/runyard-releases?style=for-the-badge&label=Download&color=06b6d4" alt="Download latest release" /></a>
</p>

<p>
  <a href="https://developer.apple.com/documentation/security/notarizing-macos-software-before-distribution"><img src="https://img.shields.io/badge/notarized-Apple-success?logo=apple" alt="Notarized by Apple" /></a>
</p>

<sub>
Requires macOS 14 Sonoma or later · Apple Silicon &amp; Intel · <a href="https://github.com/Bonevil-ca/runyard-releases/releases">Browse all releases</a>
</sub>

</div>

<br />

## About Runyard

Runyard runs in your menu bar (no dock icon) and manages the processes that make up your dev stack. You describe your tools in a single `config.json` file, and Runyard handles the rest: spawning processes in the right order, polling HTTP/TCP health checks, surfacing live status, and shutting everything down cleanly when you're done.

It's not Electron, not a wrapper, not a webview — just native Swift and AppKit, designed to stay out of your way until you need it.

<div align="center">
<a href="https://bonevil.ca/runyard"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-1.webp" alt="Runyard menu bar — start, stop, and monitor your dev stack" width="320" /></a>
</div>

## Key Features

### Orchestration

- **One-click orchestration** — start your entire stack with one click; sequential startup with `waitFor` dependencies makes sure services launch in the right order.
- **Install hooks** — auto-run `npm install` (or any command) when dependencies are missing.
- **Custom shutdown** — define `stopCommands` for tools that need a graceful stop (e.g. `docker-compose down`) instead of SIGTERM.

### Monitoring & health

- **Health monitoring** — HTTP and TCP health checks with a real-time state machine (starting, running, failing, stopped, and more).
- **Auto port detection** — Runyard detects each service's real listening port automatically — no hardcoding — and shows it next to the tool name; use `{{port}}` in URLs and health checks.
- **Probes** — standalone HTTP/TCP watchers that surface failures in the menu without managing a process.
- **Per-process logs** — every process writes to `~/Library/Logs/Runyard/`, openable straight from the menu.

### Workflow & control

- **Keep Awake** — built-in `caffeinate` integration. Toggle a timed or indefinite session manually from the popover, or set `keepSystemAwake` on any service or probe so macOS only stays awake while it's actually running. Optionally keep the display awake too.
- **Custom actions** — open URLs, run shell commands, execute AppleScripts, or reveal files. Scope each action to `running`, `stopped`, or `always` visibility.
- **Shortcuts and groups** — flat quick-action lists or nested submenus to organize your stack the way you think about it.
- **Export & import** — share or back up a tool's full setup as a `.runyard` file, with secrets scrubbed and a review step on import.

### Sync, localization & updates

- **Sync across Macs** — store your config in iCloud Drive (or any synced folder like Dropbox) to share the same stack across machines.
- **Bilingual UI** — English and Français, follows your macOS language setting.
- **Safe & up to date** — Developer ID–signed, notarized by Apple, and auto-updating, so you always run the latest trusted build.

## A look inside

<div align="center">

<a href="https://bonevil.ca/runyard"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-2.webp" alt="Runyard settings — group links, actions, and services" width="560" /></a>

<a href="https://bonevil.ca/runyard"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-3.webp" alt="Runyard advanced settings — health checks, timeouts, and graceful shutdowns" width="560" /></a>

<a href="https://bonevil.ca/runyard"><img src="https://bonevil.ca/assets/screenshots/en/screenshot-4.webp" alt="Runyard JSON configuration — config as code" width="560" /></a>

<sub><strong>Config as code. No magic.</strong> One JSON file to rule your entire stack.</sub>

<sub>👉 <a href="https://bonevil.ca/runyard/examples/">Browse ready-to-copy config examples</a> — Docker Compose, Node version managers, direnv/mise, and more.</sub>

</div>

## Installation

1. Download the [latest `.dmg`](https://github.com/Bonevil-ca/runyard-releases/releases/latest/download/Runyard.dmg).
2. Open it and drag **Runyard** to your `Applications` folder.
3. Launch from Launchpad or Spotlight. The icon will appear in your menu bar.
4. On first launch, a welcome screen lets you load example tools, add a tool in Settings, or edit `config.json` directly to define your stack.

Updates are delivered automatically. You can also check manually via **Check for Updates…** in the menu bar dropdown or the **About** tab.

## Documentation

The full user guide — getting started, the `config.json` reference, copy-paste config examples, purchases, and troubleshooting — lives at **[bonevil.ca/runyard/docs](https://bonevil.ca/runyard/docs/)**.

Français : **[bonevil.ca/fr/runyard/docs](https://bonevil.ca/fr/runyard/docs/)**

## Pricing

Runyard is **free to use**, with an optional **Unlimited Tools** upgrade for bigger stacks and a tip jar if you'd like to support development. See [Purchases](https://bonevil.ca/runyard/docs/purchases) for details.

## Compatibility

- **macOS 14 Sonoma or later** (Apple Silicon and Intel).
- Distributed with Developer ID signing, notarized by Apple, and Hardened Runtime enabled.
- Not sandboxed — Runyard spawns user-supplied binaries (npm, docker, mix, fly, etc.), which is structurally incompatible with the App Sandbox. It is not available on the Mac App Store for the same reason.

## Support & Feedback

- **Bug reports & feature requests** — [open an issue](https://github.com/Bonevil-ca/runyard-releases/issues) on this repo.
- **Email** — [support@bonevil.ca](mailto:support@bonevil.ca).
- **Website** — [bonevil.ca/runyard](https://bonevil.ca/runyard).

## About this repository

This repository is the **public release channel** for Runyard. It hosts:

- Signed, notarized `.dmg` builds attached to each [GitHub Release](https://github.com/Bonevil-ca/runyard-releases/releases).
- The issue tracker for bug reports and feature requests.

## Legal

- [Privacy Policy](https://bonevil.ca/runyard/privacy-policy)
- [Terms of Use](https://bonevil.ca/runyard/terms-of-use)

<div align="center">
<sub>© 2026 Bonevil. Made in Québec.</sub>
</div>

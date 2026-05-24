# Changelog

All notable changes to anyDeploy will be documented in this file.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.9] — 2026-05-24

### Added
- Clear expired-trial messaging in the plan picker — when your 2-day trial is over, the app tells you exactly that instead of showing a generic status.
- Checkout reliability: the browser now opens every time you click a paid plan, with visible feedback while it loads.

### Improved
- Plan cards no longer allow accidental text selection — more polished, app-like feel.
- Plan picker visual polish: badges render correctly, colours consistent with the app's dark theme.

## [1.0.8] — 2026-05-21

### Improved
- Cleaner first-run experience. Activate or start a free trial without configuring anything — the app already knows where to phone home.
- Smoother handoff after purchase.
- General reliability polish.

## [1.0.7] — 2026-05-21

### Added
- Free 2-day trial flow is live in the in-app plan picker — machine-locked, no payment required.

### Improved
- Stronger backend hardening across the licensing pipeline.
- General reliability polish.

## [1.0.6] — 2026-05-21

### Added
- Broader GitHub repository compatibility — works with any repository regardless of its default branch name.

### Improved
- Smarter first-deploy detection: anyDeploy figures out the right starting point for your repository and remembers it for next time.
- General polish across the deploy pipeline.

## [1.0.5] — 2026-05-21

### Improved
- Faster, more reliable first-launch experience — the app starts cleanly the moment you install it.
- Smoother startup on cold-boot Windows installs.

### Fixed
- Resolved an installer-related startup issue affecting some Windows machines on first launch.

## [1.0.4] — 2026-05-21

### Added
- Faster, more reliable deploys across all target types — connection handling is more resilient on slow or unstable networks.
- Improved app startup time on first launch.

### Improved
- More consistent deploy progress reporting — status updates arrive sooner and stay accurate for the full duration of a deploy.
- General stability improvements throughout the app.

## [1.0.3] — 2026-05-20

### Added
- In-app Cloudflare onboarding wizard (first-run + Settings).
- Multi-domain support — connect more than one Cloudflare domain.
- Auto-detect system modifications and configure the optimal setup for any Android phone during onboarding.

### Improved
- Cleaner deploy progress UI.
- More reliable deploys across all target types.

## [1.0.2] — 2026-05-19

### Added
- Redesigned plan picker with clearer tier differences.
- New deploy progress view with named phases and elapsed-time counter.

### Changed
- Cleaner deploy experience — no transient "ERROR" state on successful deploys.
- Sidebar stays stable during deploys.

### Fixed
- More reliable health detection across all supported target types.

## [1.0.1] — 2026-05-19

### Added
- In-app subscription picker — choose between trial, monthly Pro, or
  lifetime, all without leaving the app.
- Automatic license key activation after checkout.

### Changed
- Reliability and polish improvements across the deployment pipeline.

## [1.0.0] — 2026-05-19

### Added
- Initial public release.
- Windows (.exe) and Linux (.AppImage) installers.
- 6 deploy target types: Android phone (Termux), Linux server / VPS,
  Raspberry Pi, another Linux computer, Windows + WSL2, local machine.
- Auto-configuration of nginx, PM2, Cloudflare Tunnel + DNS, Let's Encrypt SSL.
- First-class support for Discord, Telegram, and Slack bot projects.
- 7-day offline license grace period.
- Auto-deploy on GitHub push (poll-based, no webhook setup required).
- Per-project environment variables (encrypted at rest).
- Cron job management from the dashboard.
- Storage tab showing live database file sizes.

# Changelog

All notable changes to anyDeploy will be documented in this file.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

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

# Changelog

All notable changes to anyDeploy will be documented in this file.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.1] — 2026-05-19

Security + privacy hardening pass.

### Fixed
- Removed hardcoded phone IP fallback that shipped in v1.0.0
- Local dev DB no longer ships inside the installer
- Build-time AES key is no longer in plaintext — now split across two V8 bytecode files (the .build-key.json file is gone)
- Dev-mode bypass envs are gated behind a packaged-app check, so they cannot be activated in installed builds

### Added
- In-app plan picker: Trial (2 days) / Pro (€6.99/mo) / Lifetime (€99.99)
- `anydeploy://` custom protocol — LemonSqueezy checkout success auto-fills the license key inside the app
- Trial endpoint on licproxy (one machine-locked trial per device)
- Pre-release safety scanner refuses to build on rule violations

### Changed
- Sensitive backend services compiled to V8 bytecode
- Docs reorganized — contributors start at `docs/AGENTS.md`

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

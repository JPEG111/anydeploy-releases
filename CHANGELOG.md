# Changelog

All notable changes to anyDeploy will be documented in this file.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.43] — 2026-06-01

### Improved
- The empty dashboard now guides new users with a two-step checklist (connect a device, then deploy) so the first deploy never dead-ends because no device is connected yet.

## [1.0.42] — 2026-06-01

### Improved
- Settings now uses the same one-command target setup as everywhere else — the old manual SSH form is gone, so adding a device is consistent no matter where you start from.

## [1.0.41] — 2026-06-01

### Improved
- Adding a device from the dashboard now uses the same one-command setup as first-time onboarding — no more manual SSH host/port/password forms.
- Buying a domain auto-detects the moment it appears in your account — no need to keep refreshing.
- Active domains are pre-selected so you can continue in one click.

## [1.0.40] — 2026-06-01

### Improved
- When connecting a domain, anyDeploy now detects your registrar (Porkbun, GoDaddy, Namecheap, Squarespace, Name.com, Hostinger) and shows exact step-by-step instructions for that one with a direct link, instead of a generic list. Falls back to the full list if it can't detect.

## [1.0.39] — 2026-06-01

### Improved
- Clearer wording on the domain connection screen so it's obvious the nameservers go at your domain registrar (Porkbun, GoDaddy, etc.), not inside Cloudflare.

## [1.0.38] — 2026-06-01

### Fixed
- Domains added to Cloudflare but not yet active are now tappable in the domain list — they reopen the nameserver setup so you can finish connecting them, instead of being stuck as a greyed-out row.

## [1.0.37] — 2026-06-01

### Improved
- After connecting a domain, anyDeploy now watches for activation automatically and shows a live status — once your nameservers update it lights up 'active' on its own, no need to keep refreshing.

## [1.0.36] — 2026-06-01

### Fixed
- Connecting a domain no longer fails with an account-detection error — adding a domain now works with the standard API token, no extra permissions needed.

## [1.0.35] — 2026-05-31

### Fixed
- Cloudflare setup now shows the real reason when something fails (e.g. an API token missing a permission) instead of a generic 'HTTP 400' error.

## [1.0.34] — 2026-05-31

### Improved
- After buying a domain, the next step is now obvious: Cloudflare buyers refresh, and anyone who bought elsewhere is taken straight into the one-step connect flow — no more dead-end refreshes.

## [1.0.33] — 2026-05-31

### Added
- No domain yet? Setup now offers a clean two-path guide — buy a fresh domain (with links to the cheapest registrars) or connect one you already own.
- Connecting an existing domain is now mostly automatic: type it in and anyDeploy adds it to Cloudflare for you, then shows the exact nameservers to set at your registrar with one-click copy and direct links to GoDaddy, Namecheap, Porkbun and Google.

## [1.0.32] — 2026-05-31

### Fixed
- Cloudflare connection no longer fails with a 'no accounts found' message when the API token is set up correctly — your domains now load reliably.

### Improved
- Reliability and polish improvements.

## [1.0.31] — 2026-05-31

### Improved
- Cloudflare setup now shows a specific error and direct edit link if a token permission is missing — no need to delete and recreate the token.
- Token setup instructions clarify which text to copy (the token value, not the curl test command below it).
- Reliability and polish improvements.

## [1.0.30] — 2026-05-31

### Improved
- Cloudflare setup now shows an exact table of which permissions and levels to select when creating an API token — no guesswork required.
- Reliability and polish improvements.

## [1.0.29] — 2026-05-31

### Improved
- Target selection cards now clearly indicate whether a device needs to be on the same WiFi as your computer, or can be reached from any network.
- Setup wizard shows an upfront warning for devices that require a local network connection — no more mysterious setup failures.
- Reliability and polish improvements.

## [1.0.28] — 2026-05-31

### Added
- Phone setup now shows scannable QR codes for the two apps required — point your phone camera to go straight to the download.

### Improved
- Reliability and stability improvements across the deployment pipeline.

## [1.0.27] — 2026-05-31

### Added
- Setup wizard now guides you through getting a domain when you don't have one yet — two clear options with step-by-step instructions and a refresh button to check once it's ready.
- Phone setup step now shows direct download links for the apps needed on your device and explains what gets installed automatically.
- Public URL for instant auto-deploy on every GitHub push can now be configured during initial setup.

### Improved
- External links now open reliably in your system browser from all setup screens.
- Setup flow ordering is now clearly explained so the connection between each step makes sense.
- Reliability and stability improvements across the deployment pipeline.

## [1.0.26] — 2026-05-30

### Added
- Terminal output text can now be selected and copied.

## [1.0.25] — 2026-05-30

### Added
- Admin panel now shows a clear "Blocked" status for any trial user that has been suspended, so you can instantly see who is blocked at a glance.

### Improved
- Trial management controls in the admin panel are more intuitive and clearly labeled.

### Fixed
- Status badge in the Trials tab now correctly reflects real-time block state instead of always showing "Active".

## [1.0.24] — 2026-05-30

### Added
- Explicit "Offline" and "Trial Expired" banners on the launch screen if the app cannot validate the license or if the trial period has ended.
- Unified Security Validation: Trial keys are now subject to strict real-time server validation on every launch. If a trial machine is blocked via the proxy admin panel, the desktop app will instantly revoke access.

### Fixed
- Resolved an infinite loop rate-limit issue ("Too many attempts") that occurred when starting a new free trial.
- Fixed a silent pipeline crash where WSL GPU teardown processes would halt Linux AppImage generation.

## [1.0.23] — 2026-05-30

### Changed
- Removed the offline grace period. The app now requires an internet connection on launch to validate licenses and trial status in real-time, preventing blocklist bypasses.

## [1.0.22] — 2026-05-30

### Fixed
- Hardened trial security to prevent machine ID spoofing when a device is renamed.
- Resolved an issue where blocked devices could bypass the blocklist under certain conditions.

## [1.0.21] — 2026-05-30

### Improved
- Smoother terminal experience with inline typing directly on the prompt line instead of a separate input box.
- Visual polish: blinking block cursor, cleaner terminal view, and animated execution indicators.

### Fixed
- Terminal window no longer jumps up and down while typing.
- Crash fix when terminal commands exit unexpectedly.

## [1.0.20] — 2026-05-29

### Added
- Terminal tab on every project — run commands directly on your deployment device from inside the app. Scoped to the project directory. Blocks destructive system operations while leaving you free to inspect files, check logs, and debug.

## [1.0.19] — 2026-05-29

### Improved
- Environment variables added or changed via the Settings panel now reliably take effect when you hit Sync or Restart — for every project type and every device, on the first try.

## [1.0.18] — 2026-05-29

### Fixed
- Dashboard metric values now match the Target Health panel from the very first load.
- RAM and Disk cards show a percentage immediately while absolute values are still loading.

## [1.0.17] — 2026-05-29

### Fixed
- Dashboard CPU, RAM, and Disk cards no longer show zero on first load.
- Values in the dashboard cards now match the Target Health panel.

## [1.0.16] — 2026-05-29

### Added
- Target Health panel now shows disk usage per device alongside CPU and RAM.

### Fixed
- CPU and RAM metrics no longer disappear when switching between pages — values stay visible instantly when returning to the dashboard.

## [1.0.15] — 2026-05-29

### Added
- Target Health panel now shows live CPU and RAM for each connected device.
- When multiple deployment targets are configured, the CPU, RAM, and Disk cards on the dashboard each display a separate coloured bar per device for at-a-glance comparison.
- Target Health audit view now lists leftover config directories from deleted projects, with a per-entry Clean button.

### Improved
- Environment variables added via the Settings panel now take effect immediately on the next deployment across all project types.
- Improved reliability when the licensing server is temporarily unreachable.

## [1.0.14] — 2026-05-29

### Added
- Target Health audit view (Settings → Advanced) now shows leftover config directories from deleted projects and lets you clean them up without SSH access. Works for all device types.

## [1.0.13] — 2026-05-29

### Improved
- Environment variables added or changed in the Settings panel now reliably take effect when redeploying, regardless of when the variable was first added.
- Clearer messaging when the licensing server is temporarily unavailable.

## [1.0.12] — 2026-05-25

### Improved
- Cleaner, less cluttered Deploy screen — the in-progress view now sits flush on the page instead of being wrapped in nested cards.
- Smoother progress radial — removed visual artifacts around the ring for a more polished, app-native look.

## [1.0.11] — 2026-05-25

### Fixed
- Pro and Lifetime checkout now opens reliably across all Windows configurations.

## [1.0.10] — 2026-05-24

### Fixed
- Pro and Lifetime checkout buttons now open the correct payment page every time.

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

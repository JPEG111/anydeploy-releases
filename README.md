<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=timeGradient&height=200&section=header&text=anyDeploy&animation=fadeIn&fontColor=ffffff" alt="anyDeploy Banner" />

  <br />

  ![Version](https://img.shields.io/badge/version-1.0.28-6366f1?style=for-the-badge)
  ![Downloads](https://img.shields.io/github/downloads/JPEG111/anydeploy-releases/total.svg?style=for-the-badge&color=10b981)
  ![Windows](https://img.shields.io/badge/Windows-0078D4?style=for-the-badge&logo=windows)
  ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
  ![macOS](https://img.shields.io/badge/macOS%20soon-ECF0F1?style=for-the-badge&logo=apple&logoColor=black)
  ![License](https://img.shields.io/badge/License-Proprietary-ef4444?style=for-the-badge)

  <br />
  <br />
</div>

**Self-hosted PaaS desktop app.** Deploy any GitHub repo to your own hardware — old phone, Linux server, Raspberry Pi, Windows PC. License-activated, no accounts, no telemetry, no monthly bills.

## Download

Latest release: [v1.0.28](../../releases/latest)

| Platform | Download |
|---|---|
| Windows 10+ (64-bit) | [anyDeploy Setup 1.0.28.exe](../../releases/latest/download/anyDeploy.Setup.1.0.28.exe) |
| Linux x64 (Ubuntu 16.04+, Debian 9+, Fedora 25+, any glibc 2.17+ distro) | [anyDeploy-1.0.28.AppImage](../../releases/latest/download/anyDeploy-1.0.28.AppImage) |
| macOS | *Coming soon — email support@anydeploy.app for early access* |

> **Verify integrity:** the SHA-256 checksum in `latest.yml` (Windows) or
> `latest-linux.yml` (Linux) must match your download.

## What you can deploy

- **Web apps:** Next.js, Vite/React, Vue, Svelte, plain HTML, Astro
- **APIs:** Express, Fastify, Python (Flask/FastAPI), Go, Rust
- **Bots:** Discord (discord.js / discord.py), Telegram (telegraf), Slack
- **Static:** any framework that produces a `dist/` or `build/` folder

## Where you can deploy (6 target types)

| Target | Set-up time | Use case |
|---|---|---|
| Android phone (Termux) | ~10 min | Your old phone as a server |
| Linux server / VPS | ~5 min | DigitalOcean, Hetzner, etc. |
| Raspberry Pi | ~5 min | Pi 3/4/5, Pi Zero |
| Another Linux computer | ~5 min | Desktop, laptop, friend's box |
| Windows + WSL2 | ~10 min | Another Windows PC on your LAN |
| This computer | instant | The machine running anyDeploy itself |

All set up via one `curl` command from the app — no manual config files,
no nginx tutorials, no PM2 docs.

## How it works (3 steps)

1. Activate with your license key
2. Click **Add Target** → pick your device → run the one-line `curl` command it gives you
3. Click **Deploy** → paste any GitHub URL → done

<!-- TODO: add screenshots/GIFs here once you have them -->

## What gets automated for you

- nginx vhost configuration
- PM2 process management with auto-restart on crash + boot
- Cloudflare Tunnel + DNS (if you connect a Cloudflare account)
- Let's Encrypt SSL certificates
- Environment variables (encrypted at rest)
- Cron jobs
- Database file tracking (storage tab shows live size)

## System requirements

**Windows:** Windows 10 (64-bit) or newer. ~150 MB disk.  
SmartScreen will flash "Windows protected your PC" on first install — click **More info** → **Run anyway**. This is expected for unsigned installers.

**Linux:** glibc 2.17+ (any distro from the last 8 years). ~200 MB disk.  
Mark the AppImage executable first:
```bash
chmod +x anyDeploy-1.0.28.AppImage
```
Then double-click, or run `./anyDeploy-1.0.28.AppImage`.

**macOS:** coming soon.

## Support

- **Bug reports** → [GitHub Issues](../../issues) (this repo)
- **Feature requests** → [GitHub Discussions](../../discussions)
- **Sales / licensing** → support@anydeploy.app

## License

Proprietary. Commercial use requires a valid license key. The desktop app
binary is closed-source. See [LICENSE](./LICENSE) for full terms.

---

*anyDeploy — your hardware, your data.*

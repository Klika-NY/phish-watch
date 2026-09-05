# Autobot · Phish Watch

Landing page for the hourly Grok Phish concert monitor.

**Live URL:** https://klika-ny.github.io/phish-watch/

Official Grok Bot profile: [GROK-BOT.md](GROK-BOT.md)
Phone alerts: [NTFY.md](NTFY.md) — subscribe iOS ntfy to topic `Phish-Watch`.

## Deploy

The site files are on `main`. GitHub Actions cannot publish until Pages is enabled.

1. Open https://github.com/Klika-NY/phish-watch/settings/pages
2. Build and deployment → Source → **GitHub Actions**
   - Alternate: Deploy from a branch, `main`, folder `/`
3. Open https://github.com/Klika-NY/phish-watch/actions/workflows/pages.yml and click **Run workflow**
4. When green: https://klika-ny.github.io/phish-watch/

Hourly watch runs on Grok (**Phish AutoBot 2.0**), not GitHub. GitHub hosts the dashboard and mirrors material changes to ntfy.

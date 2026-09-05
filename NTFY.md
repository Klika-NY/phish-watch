# ntfy · Phish Watch

Phone alerts for official date drops, site changes, and rumor-desk changes.

## Subscribe (do this once on your iPhone)

1. Install **ntfy** from the App Store.
2. Tap **+** / Subscribe.
3. Topic name exactly: `Phish-Watch`
4. Server: `https://ntfy.sh` (default).
5. Allow notifications.

Anyone who knows the topic can read it. It is a tour-alert channel, not a secrets channel.

Web backup: https://ntfy.sh/Phish-Watch

## What fires a push

| Source | When | Topic |
|---|---|---|
| Grok **Phish AutoBot 2.0** (hourly) | Light is green or yellow, or official/rumor claim changed | Phish-Watch |
| Grok AM desk / PM sweep | Same rule | Phish-Watch |
| Grok **Phish X Live Webhook** | New confirmed @phish / @Phish_FTR post | Phish-Watch |
| Grok GitHub push trigger | `index.html` or `last-sweep.json` lands on `main` | Phish-Watch |
| GitHub Action `ntfy.yml` | Same file paths, or manual Run workflow | Phish-Watch |

Red / Nothing Yet does **not** hit ntfy. Those still go to the Grok app if you left Autobot on APP_ONLY.

## Manual test

```bash
curl -H "Title: Phish Watch · test" -H "Priority: high" -H "Tags: guitar" \
  -H "Click: https://klika-ny.github.io/phish-watch/" \
  -d "Test from laptop. Subscribe topic Phish-Watch." \
  https://ntfy.sh/Phish-Watch
```

Or GitHub → Actions → **ntfy on Phish Watch change** → Run workflow.

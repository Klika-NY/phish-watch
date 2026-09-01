# Autobot · Phish Watch

Landing page for the hourly Grok Phish concert monitor.

**Live URL after Pages is enabled:** https://klika-ny.github.io/phish-watch/

## Deploy (one click you have to do)

The site files are already on `main`. GitHub Actions cannot publish until Pages is enabled on this repo.

1. Open https://github.com/Klika-NY/phish-watch/settings/pages
2. Under **Build and deployment → Source**, choose **GitHub Actions**
   - Alternate that also works for this static site: **Deploy from a branch**, branch `main`, folder `/`
3. Open https://github.com/Klika-NY/phish-watch/actions/workflows/pages.yml and click **Run workflow**
4. When the run is green, open https://klika-ny.github.io/phish-watch/

The hourly Grok automation already runs on Grok (not GitHub). GitHub only hosts this dashboard. Every Grok push includes the live URL above.

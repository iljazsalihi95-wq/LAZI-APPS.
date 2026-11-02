# LAZI APPS Premium

Official multilingual Android application catalog (Albanian, German, English).

## Publishing

This repository is intended to hold the static website files at the repository root: `index.html`, `apps.json`, and `assets/`.

The GitHub Actions workflow `.github/workflows/deploy-cloudflare.yml` deploys this directory to the existing Cloudflare Worker `lazi-apps` when the repository receives a push to `main`, **once** the following GitHub Actions secrets have been configured:

- `CLOUDFLARE_API_TOKEN` — Cloudflare token with Workers Scripts edit permissions for the relevant account.
- `CLOUDFLARE_ACCOUNT_ID` — Cloudflare account identifier.

The workflow is also manually triggerable. **Do not run until the site files and assets are committed**. Never commit API tokens or private credentials.

Live address: https://lazi-apps.lazisalihi.workers.dev/

Cloudflare Git integration connected on 2026-11-02. Trigger first deployment from main.

# instabox-keepalive

Keeps an Instabox free-plan VM (machine `main`) awake — the free plan auto-pauses
after 30 idle minutes, and GitHub Actions cron (every 15 min) calls Instabox's
`wake` endpoint so the VM never goes idle long enough to pause.

Secrets (set in repo Settings → Secrets and variables → Actions):

- `INSTABOX_API_KEY` — Instabox API key (`ibk_...`). Never commit the key.

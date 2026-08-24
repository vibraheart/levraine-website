# LEVRAINE

Static corporate/brand website for **LEVRAINE**, operated by **Marship Vibraheart Inc.**

Designed for deployment on **Cloudflare Pages** with `levraine.com` registered at Namecheap.

## Before publishing

1. Confirm product claims and dimensions in `index.html` are current.
2. Confirm `contact@levraine.com` is monitored.
3. Review `privacy.html` for any required policy updates.

## Cloudflare Pages settings

This is a plain static site. No build command is required.

- Framework preset: **None**
- Build command: **leave blank**
- Build output directory: **/** (repository root)
- Root directory: **/**

See `DEPLOY_CLOUDFLARE.md` for the full Namecheap + Cloudflare setup.

## Local preview

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

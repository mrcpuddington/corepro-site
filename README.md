# CorePro Coming Soon Site

Simple Astro placeholder website for CorePro.

## Run locally

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## Deploy (GitHub Actions)

This repo includes a GitHub Actions workflow that deploys the static build to Hostinger via rsync.

Add these GitHub repository secrets:

- `HOSTINGER_HOST`: `185.232.14.67`
- `HOSTINGER_PORT`: `65002`
- `HOSTINGER_USER`: `u942145300`
- `HOSTINGER_PATH`: `/domains/corepro.fit/public_html/`
- `HOSTINGER_SSH_KEY`: your private SSH key for the Hostinger user
- `HOSTINGER_KNOWN_HOSTS`: (recommended) output of `ssh-keyscan -H -p 65002 185.232.14.67`

After pushing to `main`, the workflow builds and deploys `dist/` using rsync.

# scarescore
a computer vision demo for face landmark tracking

Right now it mirrors the webcam; MediaPipe face landmarks go in `onFrame` in `public/index.html`.

## Deploy

In the Cloudflare dashboard: Workers & Pages → Create → Import a repository, and pick this repo.
It reads `wrangler.toml` and redeploys on every push.

The camera only works over HTTPS or on localhost, so the `*.workers.dev` URL is fine.

## Run locally (optional, needs Node)

```bash
npx wrangler dev
```

Open http://localhost:8787 and click **Start camera**.

## Files

- `wrangler.toml` – Worker config (serves `public/` as static files)
- `public/index.html` – the whole app: page, styles and script
- `README.md` – this file

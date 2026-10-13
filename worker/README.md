# VelvetFeed API proxy

Deploy with Cloudflare Workers:

```bash
cd worker
npx wrangler login
npx wrangler deploy
```

Copy the HTTPS worker URL into `redgifs.js` as `PROXY_BASE` (without trailing slash), then push the frontend to GitHub Pages.

This worker retrieves RedGIFs public API metadata with a temporary token. It does not bypass restrictions or proxy video bytes. Validate RedGIFs API terms and playback permissions before production use. The worker's ability to reach the upstream service is unverified.

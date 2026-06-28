# Cloudflare Worker Deployment Guide

## Purpose
This Worker proxies your GitHub Pages portfolio and adds custom cache headers plus security headers.

## Required files
- `worker.js`
- `wrangler.toml`
- `.github/workflows/deploy-worker.yml`
- `package.json` (optional)

## Step 1: Update the origin
Open `worker.js` and replace:

```js
const ORIGIN_HOST = "your-username.github.io";

# SmartNexLink Landing Page

Landing page statis untuk **SmartNexLink** — platform SaaS OLT Management (ZTE C320 & C300).

## Deploy

Otomatis via GitHub Actions ke Cloudflare Workers setiap push ke `main`.

### Setup secrets (sekali saja)

Di **Settings → Secrets and variables → Actions**, tambahkan:

| Secret | Isi |
|---|---|
| `CLOUDFLARE_API_TOKEN` | API token Cloudflare (Workers + Zone DNS untuk custom domain) |
| `CLOUDFLARE_ACCOUNT_ID` | Account ID Cloudflare |

### Custom domain

Domain `smartnexlink.com` diatur di Cloudflare sebagai custom domain Worker
`smartnexlink-landing` (Workers & Pages → Custom domains).

## Struktur

```
public/index.html   → landing page (satu file, tanpa dependency)
wrangler.json       → konfigurasi Cloudflare Workers (static assets)
.github/workflows/  → CI/CD deploy otomatis
```

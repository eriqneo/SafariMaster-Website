# 🦁 SafariMaster Website

SafariMaster is a tour operations platform engineered for safari operators, Destination Management Companies (DMCs), and luxury travel agencies across East Africa and global markets.

---

## 🚀 Quick Start (Local Development)

**Prerequisites:** Node.js 18+ or 20+

```bash
# 1. Install dependencies
npm install

# 2. Start local development server
npm run dev
```

The application will be running locally at `http://localhost:3000`.

---

## ⚡ Deploying to Cloudflare Pages

SafariMaster is fully configured for deployment on **Cloudflare Pages** with single-page application (SPA) routing, edge security headers, and static asset caching.

### Option A: Cloudflare Dashboard (Recommended for Git CI/CD)

1. Push your code to GitHub / GitLab.
2. Log into the [Cloudflare Dashboard](https://dash.cloudflare.com/) and navigate to **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**.
3. Select your repository `safarimaster-website`.
4. Configure your build settings:
   - **Framework preset**: `Vite`
   - **Build command**: `npm run build`
   - **Build output directory**: `dist`
   - **Node.js Version**: `20` (auto-detected via `.nvmrc`)
5. Click **Save and Deploy**.

### Option B: Cloudflare Wrangler CLI Direct Deployment

To build and deploy directly from your local terminal or CI runner using Wrangler:

```bash
# Build the project
npm run build

# Deploy directly to Cloudflare Pages
npx wrangler pages deploy dist --project-name=safarimaster-website
```

Or run the pre-configured script:
```bash
npm run pages:deploy
```

### Option C: Preview Cloudflare Pages Locally

Test Cloudflare edge execution locally with Wrangler:
```bash
npm run preview:cf
```

---

## 📁 Infrastructure & Configuration Files

- [`wrangler.toml`](file:///home/neo/Desktop/RafikiProjects/safarimaster%20Website/wrangler.toml) — Cloudflare Pages project configuration & runtime compatibility date.
- [`public/_redirects`](file:///home/neo/Desktop/RafikiProjects/safarimaster%20Website/public/_redirects) — SPA fallback routing rule (`/* /index.html 200`).
- [`public/_headers`](file:///home/neo/Desktop/RafikiProjects/safarimaster%20Website/public/_headers) — Edge security headers (HSTS, frame options, nosniff) and 1-year asset caching rules.
- [`.nvmrc`](file:///home/neo/Desktop/RafikiProjects/safarimaster%20Website/.nvmrc) — Node 20 environment specification for Cloudflare build workers.

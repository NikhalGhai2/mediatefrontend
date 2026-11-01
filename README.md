# Mediate — marketing site

Static site: `index.html` plus assets. No build step, no dependencies.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole page (HTML, CSS and JS in one file) |
| `logo.svg` / `favicon.svg` | Logo mark (vector) |
| `logo.png` (512px) / `logo@2x.png` (1024px) | Logo mark (transparent PNG) |
| `favicon-32.png`, `apple-touch-icon.png` | Browser tab and iOS home-screen icons |
| `fonts/` | Inter, Newsreader, JetBrains Mono (self-hosted — no requests to Google) |
| `netlify.toml` | Publish folder, security headers (CSP etc.) and font caching |

## Push to GitHub
```
cd mediate-site
git init
git add .
git commit -m "Mediate marketing site"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

## Deploy on Netlify
1. Netlify → **Add new site → Import an existing project** → pick the repo.
2. Build command: leave empty. Publish directory: `.`
3. Deploy.

## Make demo requests arrive by email (one-time, 30 seconds)
The form is a Netlify Form named `demo-request`. Netlify detects it on the first deploy.
1. Netlify → your site → **Forms** → confirm `demo-request` is listed.
2. **Forms → Form notifications → Add notification → Email notification.**
3. Form: `demo-request`. Email to notify: `nikhalghai01@gmail.com`. Save.

Visitors only ever see the on-page "Submitted" message; the email address is set in
Netlify, not in the page source. Submissions are also stored under **Forms → Submissions**.
The free plan includes 100 submissions a month.

To test after deploying: fill in the form on the live site, check **Forms → Submissions**,
then check the inbox (and spam folder, the first time).

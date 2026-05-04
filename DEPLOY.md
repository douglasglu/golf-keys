# Deploy Doug's Golf Keys to GitHub Pages

## One-time setup (5 minutes)

### 1. Create a GitHub repo
- Go to [github.com/new](https://github.com/new)
- Name it `golf-keys`
- Set it to **Public** (required for free GitHub Pages)
- Do NOT initialize with a README
- Click **Create repository**

### 2. Push this folder to the repo
Open Terminal on your Mac and run these commands exactly:

```bash
cd ~/path/to/Golf/golf-keys-pwa
rm -rf .git
git init
git branch -M main
git add .
git commit -m "Initial commit: Doug's Golf Keys PWA"
git remote add origin https://github.com/douglasglu/golf-keys.git
git push -u origin main
```

(Replace `~/path/to/Golf/golf-keys-pwa` with wherever your Golf folder is on your Mac.)

### 3. Enable GitHub Pages
- Go to https://github.com/douglasglu/golf-keys
- Click **Settings** > **Pages** (left sidebar)
- Under "Source", select **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Click **Save**
- Wait 1-2 minutes, then your site is live at:
  **https://douglasglu.github.io/golf-keys/**

## Add to your phone's home screen

### iPhone (Safari)
1. Open the URL in Safari
2. Tap the **Share** button (square with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**
5. Done — it's now an app icon on your home screen

### Android (Chrome)
1. Open the URL in Chrome
2. Tap the **three dots** menu
3. Tap **Add to Home Screen** or **Install App**
4. Tap **Add**

## Updating content
Edit `index.html` in the repo, commit, and push. GitHub Pages updates automatically in ~1 minute. The service worker will serve the new version on next app open.

## Works offline
Once you've visited the site, the service worker caches everything. You can open it with no cell service and it loads instantly from cache.

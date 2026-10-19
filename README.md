# Oconomowoc Weather PWA

A static, installable Progressive Web App based on your existing weather dashboard.

## Deploy on GitHub Pages

1. Create a new **public** GitHub repository (for example `weather`).
2. Upload the **contents of this folder** to the repository root: `index.html`, `manifest.webmanifest`, `sw.js`, and the `icons` folder.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**; select `main` and `/ (root)`, then **Save**.
5. When deployment completes, visit `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.
6. In Chrome, use **Install app** (from the address bar or browser menu), if offered.

All local paths are relative, so the app works on GitHub Pages project sites and user sites.

## Behavior and limitations

- The app shell is cached for repeat visits and can open without a network connection after the first successful visit.
- **Live weather forecasts and Windy radar require internet access.** The app does not claim to provide offline weather data.
- Theme preference is stored in the browser; Fahrenheit/Celsius and Refresh work as before.
- Windy radar is a third-party iframe; the `marker=false` setting is retained, but Windy controls its own embedded UI.
- HTTPS is supplied by GitHub Pages. Service workers will not install when opening `index.html` as a local `file://` URL.
- After updating deployed files, refresh the page to receive the latest app shell. Bump the `CACHE` version in `sw.js` when you change cached assets.

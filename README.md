# StudyFlow (installable app)

Files
- index.html            the app (your STUDYFLOW file, plus the install and offline wiring)
- manifest.webmanifest  name, colours and icons used when installed
- sw.js                 service worker (offline support)
- icons/                app icons (normal, maskable, Apple touch icon, favicon)

## Host it (free, 2 minutes)
A PWA only installs and works offline from a secure web address (https). Opening index.html straight from your
files still works as a normal web page, but it cannot be installed.

Easiest options:
1. Netlify Drop: go to app.netlify.com/drop and drag this whole folder in. You get an https link right away.
2. GitHub Pages: upload these files to a repo, then Settings > Pages > deploy from the main branch.
3. Cloudflare Pages or Vercel: create a project and upload the folder.

Keep every file in the same folder structure. Do not rename index.html.

## Install it
- Android / desktop Chrome or Edge: open your link, then use the Install icon in the address bar,
  or Settings > Install app inside StudyFlow.
- iPhone / iPad (Safari): tap Share, then Add to Home Screen.

## Moving your data (important)
Your study data is stored in the browser, per web address. The hosted link starts empty.
Before you switch: in your old version go to Settings > Export backup, then on the new link use
Settings > Import backup.

## Updating
Replace index.html on your host. The app checks the network first when online, so the new version appears on the next open.
If you add or rename files, change CACHE = 'studyflow-v1' to 'studyflow-v2' in sw.js so old caches are cleared.

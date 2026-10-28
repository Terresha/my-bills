MY BILLS — INSTALLABLE WEB APP PACKAGE (v3)

UPLOAD INSTRUCTIONS FOR GITHUB PAGES
1. Extract this ZIP on your computer.
2. Upload the CONTENTS of this folder to the root of your existing GitHub repository, replacing the older index.html, manifest.webmanifest, and sw.js. Include the icons folder and its two PNG files. Do not upload the ZIP itself.
3. Commit the changes. GitHub Pages should publish from main / (root).
4. Open https://YOUR-USERNAME.github.io/my-bills/ in Chrome on Android. Refresh the page after deployment. Use Chrome's menu and look for Install app or the equivalent install option; wording varies by device/browser.

INCLUDED
- index.html: bill tracker
- manifest.webmanifest: app identity and install metadata
- sw.js: offline caching service worker
- icons/: 192px and 512px install icons

IMPORTANT LIMITATIONS
- This improves installability but cannot guarantee that every browser/device will offer installation. Browser requirements and menu wording vary.
- Data remains local to each browser/device. Installing the app does not synchronize bills. Use Export Backup / Import Backup to transfer a copy. Do not place backups in a public repository.
- Notifications are checked while the app is open. This package does not provide guaranteed scheduled reminders while closed.
- The app is free to host on GitHub Pages in a public repository, but repository source files are publicly visible. Never upload private bill backups or credentials.

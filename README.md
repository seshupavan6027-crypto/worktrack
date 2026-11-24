# Pavan Chaitanya WorkTrack

Personal Engineering Work Management PWA.

## Files to publish
Upload these three application files directly into the ROOT of the existing GitHub Pages repository:
- `index.html`
- `manifest.webmanifest`
- `sw.js`

`README.md` is documentation only; it is not required for the app to run.

## Important deployment steps
1. Back up the current repository files and export a WorkTrack JSON backup from Settings & backup.
2. In GitHub, open the repository root and choose Add file → Upload files.
3. Upload the three application files above. They must be at the repository root, not inside a nested folder.
4. Commit the changes and wait for the Pages build/deployment workflow to finish successfully.
5. Open the published site and hard-refresh with Ctrl+Shift+R. If an installed PWA still shows the old build, close it fully and reopen it; if necessary clear that site's stored cache and reload.

## Data and cloud sync
The app uses browser-local storage as its working cache and retains the Google Apps Script / Google Drive sync implementation in `index.html`. Your Apps Script deployment, private access token, and Drive JSON data are not included in this package. Do not delete or redeploy them. After publishing, check Settings & backup and press Update Now to verify cloud sync.

## Scope
This package contains the full app source files needed for GitHub Pages. No README history files are required for runtime.

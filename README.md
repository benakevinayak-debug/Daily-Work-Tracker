# Daily Work Tracker — Google Drive edition

Static GitHub Pages tracker with optional Google sign-in and per-account Google Drive storage. No admin account or Supabase required. Each Google account stores its own `DailyWorkTracker-data.json` file in Drive. This is personal-per-account storage, not a shared team database.

## Setup

1. Open https://console.cloud.google.com/ and create/select a project.
2. Enable **Google Drive API**.
3. Configure **Google Auth Platform / OAuth consent screen**. Add app name and contact details. While in Testing mode, add the Google accounts that will test the app as test users.
4. Create **Credentials → Create credentials → OAuth client ID → Web application**.
5. Under **Authorized JavaScript origins**, add the origin for your deployed site, e.g. `https://YOUR-USERNAME.github.io` (no repository path).
6. Copy the OAuth Client ID and replace `PASTE_GOOGLE_OAUTH_CLIENT_ID_HERE` in `index.html`. Do not add a client secret to HTML.
7. Commit `index.html` to your GitHub repository and wait for Pages to redeploy.
8. Open your site and click **Continue with Google**. Grant access when Google asks.

## How data works

The app requests the `drive.file` permission. It creates/reads/updates a file named `DailyWorkTracker-data.json` in the signed-in user's Google Drive. Each account gets a separate file. Signing in with the same Google account on another device loads that account's records.

## Important notes

- Google login and Drive access require Google Cloud configuration; GitHub Pages alone cannot enable them.
- This package uses a browser-based OAuth token flow. Do not store tokens or client secrets in your source code.
- OAuth consent/testing and verification requirements are set by Google and can change.
- Drive file synchronization is a starter implementation. Test with non-critical data and keep CSV backups. Concurrent editing on multiple devices may cause one save to overwrite another.
- If you want all members' data in one combined team dashboard, use a shared database or explicitly designed shared Drive model instead.

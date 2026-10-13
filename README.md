# Daily Work Tracker

## Features
- Add, edit, and delete entries, including entries on previous dates.
- Daily 8-hour balance with task-work and idle-hour breakdown.
- Idle-time entry type with a required reason and optional explanation.
- Quick log prompt parser, including basic idle-time phrasing.
- Paste or upload a screenshot and run browser OCR to extract visible text into the quick-log prompt. Review and correct OCR output before parsing/saving; OCR can misread small text, numbers, and tables.
- Monthly summaries, charts, and CSV export.
- Google sign-in / Drive integration starter. Configure OAuth as described below before expecting Google sync to work.

## Google OAuth setup
1. In Google Cloud Console, enable the Google Drive API and configure OAuth consent.
2. Add your Google account under Audience > Test users while the app is in Testing.
3. Create a Web application OAuth client. Add the deployed origin (for example `https://YOUR-USERNAME.github.io`) as an authorized JavaScript origin.
4. Replace `PASTE_GOOGLE_OAUTH_CLIENT_ID_HERE` in `index.html` with the client ID.
5. Deploy `index.html` to GitHub Pages.

OCR uses Tesseract.js from a CDN, so screenshot reading requires an internet connection. The screenshot is processed in the browser; OCR output is not guaranteed exact. Always verify the extracted date, task names, and hours before saving.

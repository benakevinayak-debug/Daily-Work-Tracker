# Daily Work Tracker

**A proprietary daily work tracker owned by Vinayak Benake.**

A responsive, browser-based work log for tracking tasks, clients, projects, assets, estimated (bid) hours, and actual hours worked. Built with plain HTML, CSS, and JavaScript; no backend or build step is required.

## Features

- Parse a natural-language task description into editable entry fields.
- Record work date, work type, client, project, asset/task, bid hours, actual hours, and notes.
- View, edit, and delete entries for a selected date.
- Compare daily bid hours with actual hours in a monthly chart.
- Calculate daily and monthly totals, hour differences, and actual-to-estimated efficiency.
- Review monthly totals by project.
- Export all recorded entries to CSV.
- Save entries in browser `localStorage`.
- Responsive layout for desktop and mobile screens.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.

No dependencies, package manager, server, or API key are required.

## Deploy to GitHub Pages

1. Create a GitHub repository and upload these files to the repository root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch and `/(root)` folder, then save.
5. Wait for deployment and use the site URL shown in Pages settings.

**Visibility note:** If you want to keep the source code private, make the repository private and confirm that your GitHub plan supports your intended Pages setup. A published website is accessible to visitors you allow to access the site, and client-side HTML/CSS/JavaScript can be inspected by visitors who can open it.

## Data and privacy notes

- Entries are stored in the local storage of the browser and device being used. They are not automatically synced between devices or browsers.
- Clearing browser site data may remove saved entries. Use **Export CSV** regularly to keep a backup.
- The natural-language parser uses simple pattern matching. Review parsed fields before saving, especially hours, names, and notes.
- The tracker does not send your entries to a server.

## Copyright and permissions

Copyright (c) 2026 Vinayak Benake. All rights reserved. This is proprietary software. No permission to use, copy, modify, or redistribute the source code is granted without prior written permission, except where applicable law provides otherwise. See [`LICENSE`](LICENSE).

This is a copyright notice template, not legal advice. Ensure you have the rights to all code and assets you include, and consider professional legal advice if you plan to commercialize or enforce these rights.

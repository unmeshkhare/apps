# Graviton Apps — setup guide (no command line needed)

What you have in this folder:

- `index.html` — the public index page
- `apps.json` — the list of categories and apps (the editor changes this file)
- `editor/index.html` — your private editor
- `fonts/` — the fonts, stored here so visitors make no outside requests

---------------------------------------------------------------
## Part 1 — Put it on GitHub (about 10 minutes)

1. Sign in at github.com as **unmeshkhare**. Click **+** (top right) → **New repository**.
2. Repository name: `apps`. Choose **Public**. Do not tick any extra boxes. Click **Create repository**. (Your `nudge` repository is not touched.)
3. On the empty repository page click **uploading an existing file**.
4. Unzip `graviton-apps.zip` on your PC. Open the unzipped folder, select **everything inside** (`index.html`, `apps.json`, `editor`, `fonts`) and drag it all into the GitHub page. Folders are kept.
5. Also drag in your **Stillpoint** folder: make a folder named `stillpoint`, put your Stillpoint file inside renamed to `index.html`, and add its icon as `icon.png` (about 256×256). Drag that folder in too.
6. Scroll down, click **Commit changes**.

## Part 2 — Switch on GitHub Pages

1. In the repository click **Settings** → **Pages** (left menu).
2. Under **Build and deployment** → Source: **Deploy from a branch**. Branch: **main**, folder **/ (root)**. Click **Save**.
3. Wait a minute. The page shows your temporary address: `https://unmeshkhare.github.io/apps/`. Open it to check.

## Part 3 — Your own address: apps.gravitonmultimedia.com

Do this BEFORE you share the link with anyone (saved progress in apps belongs to one address; changing the address later would lose it).

1. In Wix open **Domains** → gravitonmultimedia.com → **Manage DNS records**.
2. Under **CNAME** click **Add record**:
   - Host name: `apps`
   - Points to / Value: `unmeshkhare.github.io`
3. Save. Leave all existing records alone.
4. Back in GitHub: repository **Settings → Pages → Custom domain**, type `apps.gravitonmultimedia.com`, click **Save**.
5. Wait until GitHub shows a green tick (can take from a few minutes to a few hours). Then tick **Enforce HTTPS**.
6. Test: open https://apps.gravitonmultimedia.com

## Part 4 — The button on Wix

Add a button called **Free Apps** and set its link to `https://apps.gravitonmultimedia.com` (open in a new tab is fine). Publish your Wix site.

---------------------------------------------------------------
## Adding a new app later

1. Make a folder name in lowercase, e.g. `pendulum`. Put the app file inside as `index.html`, with an `icon.png` (about 256×256).
2. On GitHub: **Add file → Upload files**, drag the folder in, **Commit changes**.
3. Open your editor: `https://apps.gravitonmultimedia.com/editor/`
4. Choose the category → **Edit** → **+ Add app**. Fill in the name, a short description, folder (`pendulum/`) and icon (`pendulum/icon.png`). Tick "New" if you want the badge.
5. Press **Download list**. A file `apps.json` lands in Downloads.
6. On GitHub: **Add file → Upload files**, drag in `apps.json`, **Commit changes**. It replaces the old one. The site updates in about a minute.

Removing an app: delete it in the editor, download, upload `apps.json`. (The folder can stay on GitHub, or delete it there.)
Reordering: drag the ⠿ handle, or use the ↑ ↓ buttons (best on a phone).
Site name, the line below it and the YouTube link are at the top of the editor.

Tip: the editor is not linked anywhere on the site, but it is not secret either. It can only prepare a file; nobody can change your site without your GitHub login.

## Rules to keep apps from clashing

All apps share one address, so they share browser storage. In every app:
- Start each saved key with the app's name, e.g. `pendulum.save.v1` (Stillpoint already does this).
- Keep a version number in the key. When the format changes, upgrade old saves instead of discarding them.
- Keep an Export / Import progress button as a safety net.

## Later (not needed now)

- Stillpoint: add a "← All apps" link back to `../`, and switch its Google Fonts to the local fonts so it is also tracking-free. Ask and I will prepare it.
- Offline use (installable app) and the Android app can read the same `apps.json`.

# EAM301 — History of Eastern Medicine Study Materials

Four linked study tools for EAM301, built from the actual textbook (*Naked History
of Acupuncture and Herbal Medicine*) and the photographed course schedule.

- **index.html** — the interactive Study App (Socratic Dojo with 154 questions,
  reading tracker, timeline, exam prep, installable as a real offline-capable app)
- **studyguide.html** — narrative study guide, one section per chapter
- **workbook.html** — print-friendly reference workbook (24 pages)
- **worksheet.html** — active-recall practice worksheet with a full answer key
- **manifest.json** and **sw.js** — what make the Study App an actual installable,
  offline-capable PWA once hosted. Upload these two alongside the HTML files —
  don't skip them, the app works without them but loses offline support and the
  one-tap Android install prompt.

All four HTML files are cross-linked, so once hosted you can click between them.

## Put this on GitHub Pages (free hosting, ~5 minutes)

1. Go to **github.com**, sign in (or create a free account).
2. Click the **+** in the top right → **New repository**.
3. Name it something like `eam301` (name doesn't matter). Keep it **Public**.
   Don't add a README from GitHub's side — you already have one. Click **Create repository**.
4. On the new repo's page, click **uploading an existing file** (or drag files
   into the box that says "Drag files here to add them to your repository").
5. Drag in **all six files** from this folder — `index.html`, `studyguide.html`,
   `workbook.html`, `worksheet.html`, `manifest.json`, `sw.js` — plus this `README.md`.
   Click **Commit changes**.
6. Go to the repo's **Settings** tab → **Pages** (left sidebar).
7. Under "Build and deployment," set **Source** to **Deploy from a branch**,
   branch **main**, folder **/ (root)**. Click **Save**.
8. Wait about a minute, then refresh that Pages settings page — it'll show you
   a live URL like `https://yourusername.github.io/eam301/`.

## Is it actually a PWA once hosted?

Yes — with `manifest.json` and `sw.js` uploaded alongside the HTML files, and
served over HTTPS (which GitHub Pages does automatically), it meets the real
criteria for an installable Progressive Web App:

- **Android/Chrome**: tapping **📲 Install** in the top bar triggers a genuine
  one-tap install prompt, adds a home-screen icon, and opens full-screen with
  no browser bar.
- **iOS/Safari**: Apple doesn't allow the one-tap prompt for any website — use
  Safari's Share button → **Add to Home Screen** instead. You still get a real
  icon and full-screen launch.
- **Offline**: the service worker caches all four pages after your first visit,
  so the app keeps working with no signal. Your checkboxes and notes are saved
  in the browser's local storage on that device (doesn't sync across devices).

If you only upload the four `.html` files and skip `manifest.json`/`sw.js`, the
site still works fine — you just lose the one-tap install prompt and offline
caching, and fall back to manual "Add to Home Screen."

## Updating later

If you want changes made later, come back to this chat (or a new one, mentioning
these files), get the updated files, and drag the new versions into the same
GitHub repo the same way — overwrite the old ones and commit. GitHub Pages
updates automatically within a minute or two.

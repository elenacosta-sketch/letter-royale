# Letter Royale — Vocabulary Arena

A Fortnite-inspired classroom vocabulary game for 1st–4th ESO and Bachillerato. Each topic board shows all its words in two columns, with scrambled missing letters in the middle. Includes Spanish clues, keyboard controls, hints, XP, a timer and full-screen mode.

## Upload to GitHub and publish

1. Create a new GitHub repository. Use `main` as its default branch.
2. Extract the ZIP. Upload **the contents of `letter-royale/`** to the repository root, rather than uploading the ZIP or an enclosing folder. `index.html` must be at the root.
3. Choose one of the following publishing methods.

### Option A: Publish directly from the main branch (simplest)

In the repository, open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, then **main** and **/(root)**. Save. GitHub displays your website URL after deployment.

This method only needs `index.html`, `style.css`, `app.js`, `data.js`, and `.nojekyll`; the workflow is optional. GitHub's web uploader may omit hidden folders. You can use this option without uploading `.github/`.

### Option B: Publish with GitHub Actions

Upload the included `.github/workflows/pages.yml` as well. Open **Settings → Pages** and set the source to **GitHub Actions**. Open the **Actions** tab, select **Deploy Letter Royale to GitHub Pages**, and choose **Run workflow** on `main`. Future pushes to `main` deploy automatically.

If using the GitHub web interface, choose **Add file → Create new file**, enter `.github/workflows/pages.yml` as its name, and paste the contents of the included workflow if the hidden folder was skipped during upload.

Your usual project site URL will be `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`. No custom domain is required. GitHub Pages availability for private repositories depends on your GitHub plan. Standard public Pages sites can be visited by students with the URL.

## Files

- `index.html`: game page
- `style.css`: responsive game styling
- `app.js`: game logic
- `data.js`: vocabulary, clues, levels and topics
- `.github/workflows/pages.yml`: optional GitHub Pages deployment workflow
- `.nojekyll`: serves these static files directly

## Run locally

Open `index.html` in a browser. No installation, build step, API key or server is required. Google Fonts requires internet access; system fonts are used if unavailable.

## Vocabulary and levels

- ESO: four supplied BurlingtonEnglish wordlists, mapped in order to 1st–4th ESO. Topic groupings were created for the game.
- Bachillerato: 446 entries from the supplied Oxford **Idiomatic 1** Spanish wordlist, arranged into its 32 original unit/topic sections. This is one Bachillerato section based on that supplied list, not separate 1st/2nd Bachillerato curricula.
- Edit vocabulary in `data.js`. Keep each entry's `word` and Spanish `clue` fields and the level/topic structure.
- Vocabulary includes expressions and repeated entries across source topics. One spelling error in the supplied list was corrected: “unpredicatable” → “unpredictable”.

The source PDFs are not included. Vocabulary and translations originate from the supplied publisher materials; this package does not grant a licence to those materials. Check your permissions before publishing the vocabulary in a public repository. No official Fortnite artwork, logos or assets are included.

## Student use and storage

Select a level and topic, choose a gap, then click a scattered letter or type it. Correct words lock automatically. Hints cost 25 XP; completed words earn 100 XP. Complete every word to win. Large boards scroll vertically; narrow screens can scroll sideways to view both columns.

Completed-board counts are stored in this browser's local storage. There are no accounts, server-side student records or shared teacher dashboard. Moving the site to GitHub Pages does not carry over browser progress from its previous address. Full-screen availability depends on the browser.

## Verification

Game logic was checked across all 1,760 vocabulary entries and 60 boards, including letter counts, completion, XP and hints. Visual browser testing was unavailable in the creation environment.

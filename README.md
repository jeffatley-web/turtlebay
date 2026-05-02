# Turtle Bay Case Study — Deployment Files

Files for shipping the Turtle Bay case study via the GitHub Pages + Webflow embed split pattern.

## Files

| File | Purpose | Size |
|---|---|---|
| `index.html` | Standalone HTML, served by GitHub Pages at the public preview URL | 46,356 chars |
| `turtle-bay.css` | Stylesheet — referenced by both the standalone and the Webflow embed | 33,168 chars |
| `webflow-embed.html` | Drop-in code for the Webflow Embed block on aquarevwater.us | 46,233 chars |

## Repo

`https://github.com/jeffatley-web/turtlebay` — dedicated repo for this case study.

## Public URLs (after upload + GitHub Pages enabled)

- Standalone preview: `https://jeffatley-web.github.io/turtlebay/`
- CSS direct: `https://jeffatley-web.github.io/turtlebay/turtle-bay.css`

## Deployment steps

### 1. Push to GitHub

Upload `index.html`, `turtle-bay.css`, `webflow-embed.html`, and this `README.md` to the **root** of `https://github.com/jeffatley-web/turtlebay`.

### 2. Enable GitHub Pages

In the GitHub repo: **Settings → Pages → Source → Deploy from a branch → main → / (root) → Save**

GitHub will provision the URL within 1–2 minutes:
```
https://jeffatley-web.github.io/turtlebay/
```

### 3. Verify the standalone preview

Open `https://jeffatley-web.github.io/turtlebay/` in a browser and confirm the case study renders correctly. CSS will load from the same folder.

### 4. Create the Webflow page

- Add a new page in Webflow at e.g. `aquarevwater.us/case-studies/turtle-bay`
- Drop a single **Embed** block onto the page (full-width, no container constraints)
- Paste the entire contents of `webflow-embed.html` into the block
- Publish

The Webflow page will load the CSS from GitHub Pages and render the body content inline.

## Update workflow

Whenever the master case-study HTML is edited:
```
/Users/jatley/Documents/Jeff Atley/Aquarev Water /Case Study/Turtle Bay/Turtle Bay HDC - Visual Report.html
```
re-run the build script to regenerate these three files, then re-upload to GitHub. The Webflow embed block never needs to be re-pasted (it references the CSS URL, which doesn't change).

## Source

Master file: `Aquarev Water /Case Study/Turtle Bay/Turtle Bay HDC - Visual Report.html`

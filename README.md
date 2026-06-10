# CarOracle — Final Project Presentation Website

**COMP 3350 · Summer 2026 · Group a01-g07 · Ctrl Alt Defeat**

---

## How to View Locally

The website is a single self-contained HTML file. No build step, no dependencies, no server required for the basic site.

### Option A — Open directly in a browser (simplest)

1. Navigate to the `website/` folder in your file manager.
2. Double-click `index.html`.
3. It opens in your default browser.

> **Note:** The background video (`bg.mp4`) will load correctly this way in most browsers. If Chrome blocks local video autoplay, use Option B.

### Option B — Serve locally with Python (recommended)

Serving over HTTP avoids browser restrictions on local `file://` video autoplay.

```bash
cd website
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080) in any browser.

If Python 3 is not available:

```bash
# Python 2 fallback
python -m SimpleHTTPServer 8080
```

Or use Node:

```bash
npx serve .
```

---

## Adding the Demo Video

1. Record your screen-capture demo (any tool — OBS, QuickTime, ShareX, etc.).
2. Export as `demo.mp4` (H.264, web-optimised).
3. Copy `demo.mp4` into the `website/` folder.
4. Open `index.html`, find the comment block labelled `OPTION A – Local mp4`, and uncomment it:

```html
<video class="demo-video" controls poster="">
  <source src="demo.mp4" type="video/mp4" />
</video>
```

5. Delete or comment out the `<div class="demo-placeholder">` block above it.

---

## Customising Content

All content lives in `index.html`. Search for these markers to find what to update:

| Marker | What to change |
|--------|---------------|
| `Member One` … `Member Five` | Real team member names, roles, and skills |
| `80%+` stat boxes | Actual test coverage, iteration count, etc. |
| Stats row | Real numbers from your project |
| Reflection cards | Confirm the specific details match your iteration notes |
| Tech debt table | Add or remove rows as needed |
| `bg.mp4` | Replace with a different background video if desired |

---

## File Structure

```
website/
├── index.html   ← entire site (HTML + CSS inline)
├── bg.mp4       ← hero background video
├── demo.mp4     ← your screen-recording demo (add this)
└── README.md    ← this file
```

# Afrinova Pharmaceuticals — Website

This is the Afrinova Pharmaceuticals website. It is a **static site**: everything the
browser needs (layout, styling, animations, and all three languages) lives in one
HTML file, plus a folder of images. There is no server, database, or backend code —
which means it's simple to host almost anywhere for free.

## What's in this folder

- `index.html` — the entire website: every section, all the text, the CSS styling,
  and the small bit of JavaScript that runs the language switcher, the sticky
  header, and the scroll animations.
- `images/` — the 17 photos and graphics used across the site (hero cards, logo,
  team photos, partner image, etc.), referenced by `index.html`.

## What already works, with no setup needed

- **Language switcher** (EN / FR / ES) — runs entirely in the browser.
- **WhatsApp buttons** — open a pre-filled chat to the Kenya (+254 728 780 196) or
  Tanzania (+255 713 445 251) numbers.
- **"Email both branches" link** — opens the visitor's email app addressed to
  info@afrinovapharma.com.
- **Responsive layout** — adapts to phones, tablets, and desktops automatically.

Because none of this depends on a server, the site is "fully functional" the
moment the file is opened in a browser or uploaded anywhere that serves static
files.

## Preview it on your own computer (no coding required)

1. Download/clone this folder so `index.html` and `images/` sit next to each other.
2. Double-click `index.html`. It opens in your default browser and works, though
   the browser's security rules can occasionally block small things when opened
   this way (rare, but if the language switcher looks odd, use step 3 instead).
3. For the most accurate preview, use a tiny local web server:
   - **VS Code**: install the free "Live Server" extension, right-click
     `index.html`, choose "Open with Live Server."
   - **No editor at all**: if you have Python installed, open a terminal in this
     folder and run `python3 -m http.server 8000`, then visit
     `http://localhost:8000` in your browser.

## Making changes (no coding background needed)

- **Text**: open `index.html` in any plain text editor (Notepad, TextEdit, or
  VS Code — avoid Word). Use `Ctrl+F` / `Cmd+F` to find the sentence you want to
  change (e.g. search for a phrase you see on the live page), edit the words
  between the `>` and `<` symbols, save, and refresh the browser.
- **Images**: replace a file inside `images/` with a new one **using the exact
  same file name**, and it updates everywhere it's used. To add a genuinely new
  image, drop it into `images/` and reference it as `images/your-file.webp` in
  the matching `<img src="...">` tag.
- **Phone numbers / email**: search `index.html` for `wa.me/` (WhatsApp numbers)
  or `mailto:` (email address) and edit the digits/address directly.

## Publishing it live (free options)

Since this is a static site, any of these work with no backend setup:

- **GitHub Pages** (uses this repository directly):
  1. On GitHub, go to the repo's **Settings → Pages**.
  2. Under "Build and deployment," choose the branch this code lives on and
     `/ (root)` as the folder, then save.
  3. GitHub gives you a live URL (e.g. `https://<org>.github.io/<repo>/`) within
     a minute or two.
- **Netlify / Vercel**: drag-and-drop this whole folder onto netlify.com/drop (no
  account needed for a quick preview) or connect the GitHub repo for automatic
  redeploys whenever you push a change.
- **Custom domain**: once hosted on any of the above, you can point
  `afrinovapharma.com` (or similar) at it — each host has a "custom domain"
  settings page with copy-paste DNS instructions.

## Notes on the design source

This file was rebuilt from the original design export: the 17 images that were
embedded directly in the HTML (as base64 text) have been extracted into the
`images/` folder and linked by normal file paths. This keeps the page visually
and functionally identical while making the file ~90% smaller and far easier to
edit, host, and version in git.

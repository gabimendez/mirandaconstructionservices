# Miranda Constructions Service LLC — Website

This is the source for the Miranda Constructions Service LLC site, converted
from PHP-style filenames to a static site that works on GitHub Pages.

## What changed from your original code

- **`.php` → `.html`**: GitHub Pages only serves static files, so `index.php`
  became `index.html`, and all internal links (`about.php`, `services.php`,
  `contact.php`) now point to `.html` versions.
- **Missing stylesheets created**: your original HTML linked to
  `css/styles.css`, `css/core.css`, and `css/responsive.css`, but none were
  included, so the page had almost no actual visual design. I wrote starter
  versions of all three so the site looks complete out of the box. Colors,
  fonts, and spacing live in `css/core.css` (CSS variables at the top) and
  `css/styles.css` (component styling) — edit those to restyle the site.
- **Missing `css/swiffy-slider.min.css` and `js/swiffy-slider.min.js`**:
  these weren't included either, so I pointed the `<link>`/`<script>` tags
  at the public CDN version instead (`unpkg.com/swiffy-slider@1.6.6`).
- **Fixed broken markup**: replaced the non-standard `<fa>` tags with real
  `<i class="fa-solid ...">` Font Awesome icons (the originals wouldn't have
  rendered), closed mismatched `<h3>`/`</h1>` tags, fixed a stray tab
  character in an image filename (`dumpster_3\t.jpeg`), and fixed the
  WhatsApp floating button so it actually works (`https://wa.me/...` instead
  of a broken `web.whatsapp.com` link with an invalid `class` attribute).
- **Added placeholder pages**: `about.html`, `services.html`, and
  `contact.html` exist so the nav/footer links don't 404. They're bare —
  fill in real content for each.

## ⚠️ Images you still need to add

Your original code references these image files, but none were included in
what you sent me, so the page currently shows broken image icons in their
place. Drop matching files into these exact paths:

```
img/favicon/favicon.ico
img/miranda_logo.png
img/close.svg
img/menu.svg
img/dumpsters/dumpster_1.jpeg
img/dumpsters/dumpster_2.jpeg
img/dumpsters/dumpster_3.jpeg
img/iconos/truck.png
img/iconos/calendar.png
img/iconos/time.png
img/iconos/support.png
img/iconos/1.png
img/iconos/2.png
img/iconos/3.png
img/iconos/4.png
img/social/whatsAppWhite.png
```

The folders already exist in this repo (`img/dumpsters`, `img/iconos`,
`img/social`, `img/favicon`) — just drag your image files into them, matching
the names above exactly (case-sensitive).

## Other details worth double-checking

- **Phone numbers**: the site currently shows `(678) 615-1304` and
  `(770) 547-8420` in a few places. Your original also had `+92 666 888 0000`
  in the header, which looked like a placeholder test number, so I replaced
  it — confirm the right number is used everywhere.
- **Email address**: I corrected `concat@mirandaconstrunctionscompany.com`
  (typo'd) to `contact@mirandaconstructionscompany.com` — verify this is the
  actual domain/inbox you want listed.
- **WhatsApp number**: the original WhatsApp link and the `data-number`
  attribute referenced two different numbers (`+4871023962` vs
  `14045571420`). I used `14045571420` for the working link — confirm that's
  correct.
- **Address spelling**: "Alpharetta" was spelled two different ways in the
  original (header vs. footer). I standardized on "Alpharetta" throughout.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `miranda-constructions-site`).
2. Push this folder's contents to the repository root:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to "Deploy from a branch,"
   pick the **main** branch and **/ (root)** folder, then save.
5. GitHub will give you a URL like
   `https://YOUR-USERNAME.github.io/YOUR-REPO/` within a minute or two.

## Making edits after that

- Any time you edit a file and push to `main`, GitHub Pages automatically
  rebuilds the live site (usually within a minute).
- You can edit files directly on GitHub.com (pencil icon on any file) for
  small text changes, or clone the repo locally for bigger edits.
- If you want a custom domain (e.g. `mirandaconstructions.com` instead of
  the github.io URL), add a `CNAME` file at the repo root with just your
  domain name in it, and point your domain's DNS at GitHub Pages — GitHub's
  docs walk through the exact DNS records needed.

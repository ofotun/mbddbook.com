# mbddbook.com

Site for **MbDD: Modernisation by Default, Modernisation by Design** by Fikayo Otun. Static HTML/CSS/JS, ready for GitHub Pages.

Status shown on the site: **Coming 2026, currently in production**.

## Preview locally

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

To mimic the GitHub Pages project URL (`/mbddbook.com/`):

```bash
mkdir -p /tmp/mbdd-preview/mbddbook.com
rsync -a --exclude .git ./ /tmp/mbdd-preview/mbddbook.com/
python3 -m http.server 8080 --directory /tmp/mbdd-preview
```

Then visit `http://localhost:8080/mbddbook.com/`.

## GitHub Pages setup

1. Repo **Settings → Pages**.
2. Source: **Deploy from a branch**.
3. Branch: `main`, folder: **/ (root)**.
4. Save. Project site URL:

   `https://ofotun.github.io/mbddbook.com/`

5. For the custom domain (`mbddbook.com`), add a `CNAME` file later, set the custom domain in Pages settings, and point DNS at GitHub Pages. Enable **Enforce HTTPS** once the certificate provisions.

`.nojekyll` is present so GitHub Pages serves files as-is (no Jekyll processing). Internal links use relative paths so the site works under `/mbddbook.com/` and later at the domain root. Canonical URLs and the sitemap use `https://mbddbook.com/`.

## Structure

| Path | Purpose |
|------|---------|
| `index.html` | Book overview (`/`) |
| `master-template/index.html` | Master Template companion placeholder |
| `author/index.html` | Author (`/author/`) |
| `contact/index.html` | Get notified placeholder (`/contact/`) |
| `404.html` | Custom not-found page |
| `sitemap.xml` / `robots.txt` | Sitemap and crawler rules |
| `css/styles.css` | Site styles |
| `js/main.js` | Nav + reveal motion |
| `fonts/` | Self-hosted Instrument Serif + Outfit |
| `favicon.*` / `apple-touch-icon.png` | Brand mark favicons |
| `assets/og-cover.png` | Open Graph image |
| `assets/mbdd-mark.png` | Brand mark |

No build step required. No analytics or trackers.

## Links

- Author site: https://otunfikayo.com
- LinkedIn: https://linkedin.com/in/ofotun

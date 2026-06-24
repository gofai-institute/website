# Institute of GOFAI — Website

The public website for the **Institute of GOFAI** — an independent research body
developing machine-oriented symbolic methods at the intersection of proof theory,
formal logic, and the engineering of trustworthy AI.

*Symbolic methods for the age of neural AI.*

## What this is

A small static site — a landing page plus one page per section. No build tools,
no frameworks, no npm. The only external resources are Google Fonts (EB Garamond,
Inter, JetBrains Mono).

- `index.html` — landing page (hero, mission with the three pillars, links out).
- `mission.html` — the three pillars in full (the institute's mission/manifesto),
  each with an explanatory paragraph and refined research questions.
- `people.html` — the people behind the institute (with headshots in `images/`).
- `blog.html` — placeholder posts (lorem ipsum) until real essays are published.
- `support.html` — partnerships, grants, contact.
- `style.css` — shared stylesheet (design tokens live in the `:root` block).
- `nav.js` — shared mobile-nav toggle.
- `images/` — headshots and other assets.
- `favicon.svg` — site icon (the turnstile glyph).
- `robots.txt`, `sitemap.xml` — SEO crawl directives.
- `_config.yml` — tells GitHub Pages to serve the raw HTML directly.
- `README.md` — this file.

### SEO

Each page carries a unique title/description, canonical URL, Open Graph and
Twitter Card tags, and JSON-LD structured data (Organization + WebSite on the
landing page; AboutPage on Mission; Person entries on People; Blog/WebPage on
the rest). **All canonical and `og:url` values point at the current GitHub Pages
URL (`https://gofai-institute.github.io/website/`)** — update them, plus
`sitemap.xml` and `robots.txt`, when the site moves to its standalone domain.

## Local preview

Just open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

then visit <http://localhost:8000>.

## Deploying with GitHub Pages

1. Push to the `main` branch of this repository.
2. In GitHub: **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose branch **`main`** and folder **`/ (root)`**, then **Save**.
5. The site goes live at `https://gofai-institute.github.io/website/` within a
   minute or two.

### Custom domain

To serve from a standalone domain, add a `CNAME` file containing the domain
(e.g. `instituteofgofai.org`), then point the domain's DNS at GitHub Pages and
set the custom domain under **Settings → Pages**.

## Editing

Notable spots:

- **People** (`people.html`) — two placeholder entries are marked with
  `<!-- TODO -->` comments; replace with real names, roles, and links.
- **Contact** — `institute@gofai.org` is a placeholder address used across the
  pages and footers; swap in the real one.
- **Blog** (`blog.html`) — post links currently point to `#`; wire them to real
  articles when they exist.
- **Nav/footer** are repeated in each page (no templating); keep them in sync
  when you add or rename a page.

The design tokens (colours, type scale) are defined as CSS custom properties in
the `:root` block at the top of `style.css`.

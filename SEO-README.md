# SEO Setup — What's Included & What To Do

## Files added
- `robots.txt` — tells search engines what they can crawl, points to your sitemap.
- `sitemap.xml` — lists every section of the site for search engines.
- `site.webmanifest` — app icons/name, used by Google and mobile "add to home screen".
- `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` — browser tab and mobile icons, generated from your photo.
- `og-image.jpg` — the 1200×630 image shown when your site is shared on Facebook, LinkedIn, Twitter/X, WhatsApp, etc.

## Built into index.html
- Unique `<title>` and `<meta name="description">` (under 160 characters)
- `<link rel="canonical">` — prevents duplicate-content issues
- Open Graph tags (`og:*`) for Facebook/LinkedIn link previews
- Twitter Card tags (`twitter:*`) for X/Twitter link previews
- JSON-LD structured data (`Person`, `WebSite`, `BreadcrumbList`) — helps Google understand who you are and may enable rich results
- One `<h1>` per page, logical `<h2>`/`<h3>` hierarchy
- `<main>`, `<header>`, `<footer>`, `aria-labelledby` on sections — semantic HTML helps both SEO and screen readers
- `alt` text on all images, `width`/`height` set to avoid layout shift
- `rel="noopener noreferrer"` on external links

## ⚠️ Before you go live — replace this placeholder
Every file above uses a placeholder domain:

```
https://www.dristyshrestha.com.np/
```

Find-and-replace this with your real domain in:
- `index.html` (canonical link, all `og:` and `twitter:` tags, JSON-LD blocks)
- `robots.txt`
- `sitemap.xml`

## After deploying
1. **Google Search Console** (search.google.com/search-console) — add your domain, submit `sitemap.xml`.
2. **Bing Webmaster Tools** (bing.com/webmasters) — same idea, Bing has meaningful search share.
3. Test your link preview with the **Facebook Sharing Debugger** and **Twitter Card Validator** to confirm `og-image.jpg` shows correctly.
4. Run the site through **Google PageSpeed Insights** / **Lighthouse** — the layout is already lightweight, but check after you add real project links or extra images.
5. If you add more pages later (e.g. a blog or case-study pages), add each URL to `sitemap.xml`.

## Optional next steps
- Register **Google Analytics** or **Plausible** for traffic data (not included, since it requires an account/tracking ID).
- Add real `href` links to your Projects section once you have live demos or case studies — search engines rank pages with outbound proof of work more favorably.
- Keep the `<title>` and meta description updated if your role/focus changes.

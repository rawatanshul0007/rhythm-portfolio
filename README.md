# Rhythm Arya Portfolio

Static site (HTML/CSS/vanilla JS). No build step, no backend.

## Structure
index.html · css/style.css · js/main.js · assets/images/ (rhythm-arya.webp, rhythm-arya-original.jpeg, og-image.jpg) · robots.txt · sitemap.xml

## Run locally
    cd portfolio
    python3 -m http.server 8000
Open http://localhost:8000

## Update the portrait
Replace `assets/images/rhythm-arya.webp` (4:5 ratio, 800x1000 recommended). Update `og-image.jpg` (1200x630) for link previews.

## Add real writing samples
Edit the `samples` array at the top of `js/main.js`. Fill `title`, `summary`, and `url` (only a genuine, verified link). A card with no title stays a "coming soon" placeholder; it only becomes a link when `url` is set.

## Contact and social links
Edit the `mailto:` / `tel:` links in the Contact section of `index.html` and the JSON-LD block in `<head>`. Add social links only with real URLs.

## Before launch: replace `https://YOUR-DOMAIN.example/` in
- `index.html`: canonical, og:url, og:image, twitter:image
- `robots.txt` (Sitemap line)
- `sitemap.xml` (loc)

## Deploy: Cloudflare Pages (free)
1. Push this folder to a GitHub repo (or use Direct Upload in the dashboard).
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Select the repo. Framework preset: None. Build command: empty. Output directory: `/`.
4. Deploy. You get a free `*.pages.dev` URL. Then update the placeholders above and redeploy.

## Deploy: Netlify (free)
Drag the folder onto app.netlify.com/drop, or connect the Git repo with no build command and publish directory `.`.

## Custom domain (optional, paid)
Buying a domain costs money (roughly $10–15/year). Add it under Custom domains in Cloudflare Pages or Domain management in Netlify and follow the DNS prompts; HTTPS is free.

## Notes
Content comes from the supplied résumé. Fonts load from Google Fonts with serif/sans fallbacks.

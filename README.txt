MySpot — Deploy bundle (static) for GitHub/Vercel

Files:
- index.html       -> Main landing page (SEO-enhanced)
- robots.txt       -> Allows indexing and points to sitemap
- sitemap.xml      -> Sitemap for Google
- vercel.json      -> Redirects to apex domain + security headers

How to deploy (Static via GitHub + Vercel):
1) Push all these files to your repository root (main branch).
2) In Vercel, link the repo. Framework Preset: "Other".
3) Output directory: (leave empty). Build command: none (static).

If using Next.js instead:
- Move robots.txt and sitemap.xml to /public/
- Merge the <head> tags from index.html into your layout (app or pages)
- Keep vercel.json at the project root

Domain:
- Set globalmyspot.com as primary in Vercel.
- Ensure www.globalmyspot.com redirects to apex (vercel.json already handles it).
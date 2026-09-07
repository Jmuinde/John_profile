# John Muinde — Portfolio

A lightweight, static professional portfolio built with semantic HTML, CSS and a tiny amount of vanilla JavaScript.

## Why this architecture

- No framework or runtime dependency
- No database or backend to secure
- Fast static delivery
- Easy to deploy on Cloudflare Pages or GitHub Pages
- Easy to maintain: project copy lives directly in `index.html`

## Local preview

From the project directory:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Editing projects

The homepage separates work into two sections:

1. **Featured Projects** — high-signal professional/public-facing systems.
2. **Independent Projects** — projects owned end-to-end or used to explore technical ideas.

Each project is a semantic `<article>` in `index.html`. Duplicate an existing card and replace the title, description, tags and links.

Avoid turning the portfolio into a repository catalogue. Keep 3–4 featured projects and 3–6 independent builds; link GitHub for the long tail.

## Resume

The legacy resume has intentionally been removed from the deployable site so an outdated CV is not publicly exposed. Add a current PDF only when you want a resume CTA on the homepage.

## Recommended deployment: Cloudflare Pages

1. Push this folder to a GitHub repository.
2. In Cloudflare, open **Workers & Pages** → **Create application** → **Pages** → connect the GitHub repository.
3. Framework preset: **None**.
4. Build command: `exit 0` (or leave blank).
5. Build output directory: the repository root (`.`).
6. Deploy.
7. Add a custom domain under the Pages project's **Custom domains** settings if desired.

The `_headers` file adds conservative browser security headers when deployed through Cloudflare Pages.

## Alternative: GitHub Pages

Because this site is fully static, GitHub Pages also works well. Configure the repository under **Settings → Pages** and deploy from the main branch/root (or a GitHub Actions workflow).

## Deployment design decisions

- No contact form: reduces spam, external form dependencies and server-side attack surface.
- No external JS libraries: fewer third-party dependencies and faster loading.
- No “disable right click/devtools” code: it does not protect public source and degrades usability.
- No portrait-led hero: the homepage leads with professional positioning and evidence of work.

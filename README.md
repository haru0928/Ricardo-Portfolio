# Ricardo Escalante — IT & Cloud Support Portfolio

A production-ready, responsive portfolio and printable résumé for Ricardo Escalante, focused on remote IT support, help desk, cloud support, and systems administration opportunities.

## Pages

- `index.html` — portfolio, education, certifications, projects, skills, and contact details
- `resume.html` — responsive résumé with a print-optimized PDF layout

## Run locally

Install the pinned Tailwind build dependency and compile the production stylesheet:

```bash
npm install
npm run build
```

Then serve the directory:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Stack

- Semantic HTML
- Tailwind CSS compiled to a static production asset
- Small vanilla JavaScript enhancements
- Font Awesome icons

## Deployment

Run `npm run build`, then deploy the repository as static files with GitHub Pages, Netlify, Cloudflare Pages, or any standard web host. The checked-in stylesheet allows the deployed site to run without a Tailwind CDN dependency.
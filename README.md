# static-pages

A personal collection of self-contained HTML reports and interactive tools, hosted via GitHub Pages.

🌐 **Live**: <https://ghp.krsz.in/> (custom domain)

## What lives here

Each sub-folder is one self-contained web page — open the URL and it works, no build, no server, no upload step. Everything ships inside the HTML itself.

## Routing rules

| | |
|---|---|
| **URL** | `https://ghp.krsz.in/<slug>/` |
| **Folder name** | kebab-case slug, no spaces, no uppercase. E.g. `qwen3-8-27b`, `avif-crf-compare` |
| **Entry file** | `index.html` at the folder root |
| **Localization** | Optional. Single bilingual HTML using `<en>…</en>` / `<zh>…</zh>` tags + JS toggle. Choice saved in `localStorage`, switchable via `?lang=zh` URL param. |
| **Capabilities** | Self-contained — no build step, no external dependencies, no JS bundlers. CDN libraries (e.g. D3.js) are pulled at runtime. |
| **Adding a new page** | `mkdir my-new-page` → drop `index.html` → add a card to the root `index.html` → `git push` |
| **Custom domain** | `ghp.krsz.in` (CNAME) |
| **Source branch** | `main`, root path |

## Layout

```
/
├── index.html              ← Landing page (links to all sub-pages)
├── README.md
├── CNAME                   ← ghp.krsz.in
└── <page-slug>/            ← Each page lives in its own folder
    └── index.html          ← Self-contained HTML
```

## Conventions

- All pages are **self-contained** — open from `file://` or any host, no setup
- Each page lives in its own folder so URLs are stable and namespaced
- For interactive tools, prefer inlining sample data so the page works offline
- For data-heavy reports, inline raw data so the file works offline
- Use semantic kebab-case folder names; never rename a folder after launch (URLs are permanent)

## Deployment

Pushes to `main` auto-deploy via GitHub Pages. CDN cache may take 1–2 minutes to invalidate after a push.

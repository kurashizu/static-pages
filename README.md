# static-pages

A personal collection of self-contained HTML reports, hosted via GitHub Pages.

🌐 **Live**: <https://ghp.krsz.in/> (custom domain)

## Pages

### 📄 Qwen3.8 27B Competitive Intelligence Report
- **URL**: <https://ghp.krsz.in/qwen3-8-27b/>
- **Date**: 2026-08
- **Inputs**: All 610 models on Artificial Analysis Intelligence Index v4.1.1
- **Languages**: EN + 中文 (single bilingual file with in-page toggle)

## Routing rules

| | |
|---|---|
| **URL** | `https://ghp.krsz.in/<slug>/` |
| **Folder name** | kebab-case slug, no spaces, no uppercase. E.g. `qwen3-8-27b` |
| **Entry file** | `index.html` at the folder root |
| **Localization** | Single bilingual HTML using `<en>…</en>` / `<zh>…</zh>` tags + JS toggle. Choice saved in `localStorage`, switchable via `?lang=zh` URL param. |
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
└── qwen3-8-27b/            ← Each report lives in its own folder
    └── index.html          ← Bilingual report (EN + 中文)
```

## Notes

- All pages are **self-contained** — no build step, no dependencies
- Reports include raw data tables and methodology notes
- Served via GitHub Pages from the `main` branch, root path

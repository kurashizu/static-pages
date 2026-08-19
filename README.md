# static-pages

A personal collection of self-contained HTML reports and interactive charts,
hosted via GitHub Pages.

🌐 **Live**: <http://ghp.krsz.in/> (custom domain)

## Pages

### 📄 Qwen3.8 27B Competitive Intelligence Report
- **URL**: <http://ghp.krsz.in/qwen3-8-27b-report/>
- **Date**: 2026-08
- **Inputs**: All 610 models on Artificial Analysis Intelligence Index v4.1.1
- **Files**:
  - `index.html` — English report
  - `index_zh.html` — 中文报告
  - `chart.html` — Interactive D3 scatter chart with hover, filters, no-cost strip

## Layout

```
/
├── index.html              ← Landing page (links to all sub-pages)
├── README.md
└── qwen3-8-27b-report/     ← Each report lives in its own folder
    ├── index.html          ← English report
    ├── index_zh.html       ← 中文报告
    └── chart.html          ← Interactive chart
```

## How to add a new page

1. Create a folder under the repo root: `mkdir my-new-page`
2. Drop your self-contained HTML inside as `index.html`
3. Optionally add `index_zh.html` for Chinese version
4. Add a card to the root `index.html` linking to `./my-new-page/`
5. `git push` — GitHub Pages picks up the change within ~1 minute

## Notes

- All pages are **self-contained** — no build step, no dependencies
- CDN libraries (D3.js) are pulled from jsdelivr at runtime
- Reports include raw data tables and methodology notes
- Served via GitHub Pages from the `main` branch, root path
- Custom domain: `ghp.krsz.in` (CNAME)

# Blog Listing Page Implementation

## Summary

Add blog navigation to the website and create a blog listing page at `/articles/index.html`.

## Background

### Current State
- One article exists: `articles/plan-commit-ai-documentation.md`
- Header has: Docs, GitHub
- Footer has: GitHub, Documentation
- No blog navigation exists

### Reference
- `docs/plans/20260112_landing_page_redesign.md` - Design system reference

## Implementation

### 1. Footer Update (index.html)

Add "Blog" link to footer navigation:

```html
<div class="footer-links">
    <a href="https://github.com/planstack-ai/planstack">GitHub</a>
    <a href="/articles">Blog</a>
    <a href="https://github.com/planstack-ai/planstack/blob/main/docs/getting-started.md">Documentation</a>
</div>
```

### 2. Blog Listing Page (articles/index.html)

Create new page with:
- Same header/footer as index.html
- Reuse existing CSS variables and styles
- Article cards with title, date, description
- Link to individual article pages

**Page Structure:**
```
Header (same as index.html)
├── Logo
└── Nav: Docs, Blog, GitHub

Main
├── Section Label: "Blog"
├── Title: "Articles"
├── Description: Brief intro
└── Article Grid
    └── Article Card
        ├── Date
        ├── Title
        └── Description

Footer (same as index.html)
```

**Article Card Styling:**
- Reuse `.stat-card` pattern from index.html
- Add hover effect for clickability

### 3. Files Modified

| File | Change |
|------|--------|
| `index.html` | Add Blog link to footer |
| `articles/index.html` | New file - blog listing page |

## CSS Notes

Reuse from index.html:
- CSS variables (colors, fonts)
- `.container`, `.section`, `.section-label`, `.section-title`
- Header/footer styles
- `.btn`, `.btn-secondary`

New styles in articles/index.html:
- `.article-grid` - Grid layout for articles
- `.article-card` - Individual article styling

## Articles Data

Current article:
- Title: "planをcommitせよ：AI時代のドキュメンテーション"
- Path: `/articles/plan-commit-ai-documentation`
- Status: Draft (published: false)
- Topics: ai, claude, documentation, workflow

## Verification

1. Open index.html - verify footer has Blog link
2. Click Blog link - navigates to /articles
3. articles/index.html displays correctly
4. Header navigation works (Docs, Blog, GitHub)
5. Responsive design on mobile
6. Article card links work

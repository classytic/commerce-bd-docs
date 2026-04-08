# Commerce BD Docs

Learning guides for the BigBoss Commerce ERP backend. Served as raw markdown — the frontend fetches directly from GitHub and renders in the dashboard.

## Structure

```
{module}/
  _index.json     ← table of contents for this module
  {slug}.md       ← individual guide page (markdown)
```

## How it works

1. FE calls `https://raw.githubusercontent.com/classytic/commerce-bd-docs/main/{module}/_index.json`
2. Renders a table of contents with clickable cards
3. User clicks a guide → FE fetches `{module}/{slug}.md` and renders the markdown
4. React Query caches for 5 minutes — push to `main` and users see updates within 5 min

## Adding a guide

1. Create or edit a `.md` file in the relevant `{module}/` directory
2. Add an entry to `{module}/_index.json` with `slug`, `title`, `description`, `order`
3. Push to `main`

## _index.json shape

```json
{
  "module": "accounting",
  "title": "Accounting Guides",
  "subtitle": "Learn how to use the double-entry accounting module",
  "pages": [
    {
      "slug": "getting-started",
      "title": "Getting Started",
      "description": "One-time setup: chart of accounts, opening balances, fiscal periods",
      "order": 1
    }
  ],
  "updatedAt": "2026-04-08T00:00:00Z"
}
```

## Supported markdown

Headings, paragraphs, bold, italic, inline code, code blocks, blockquotes, links, images, ordered/unordered lists, horizontal rules. Internal links (starting with `/`) navigate within the dashboard. Video embeds via `videoUrl` in `_index.json` entries.

## Modules

- `accounting/` — Chart of accounts, A/P, A/R, day close, reports
- `inventory/` — Stock management, transfers, purchases (planned)
- `pos/` — Point of sale operations (planned)

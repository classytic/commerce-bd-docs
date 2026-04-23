# Commerce BD Docs

Learning guides for BigBoss Commerce. Rendered as a public Nextra docs site at **https://classytic.com/commerce-bd/docs** — the FE fetches MDX directly from this repo, no rebuild required.

## Structure

```
_meta.js                ← top-level sidebar order (index, accounting, inventory, …)
index.mdx               ← landing page

{module}/
  _meta.js              ← sidebar order + labels for this section
  {slug}.mdx            ← individual guide page (MDX)
```

## How rendering works

1. The Next.js app on `classytic-fe` fetches the GitHub tree (`api.github.com/.../trees/main?recursive=1`) at request time, cached via Next's `fetch({ next: { tags: ['commerce-bd-docs'] } })`.
2. Each `_meta.js` is downloaded and parsed for sidebar labels + ordering.
3. Each requested page's `.mdx` is fetched, compiled with `nextra/compile`, and rendered through `nextra-theme-docs`.
4. Push to `main` → fire the revalidate webhook (`POST https://classytic.com/api/revalidate/commerce-bd-docs` with `x-revalidate-secret`) → readers see updates instantly.

**No build-time pre-compile.** Compiled output isn't stored. The cache is the raw MDX text, ~5 KB per page.

## Adding a guide

1. Create or edit an `.mdx` file in the relevant `{module}/` directory
2. Add the slug to `{module}/_meta.js`: `'my-slug': 'Display Title'`
3. Optional: add YAML frontmatter for `title` + `description` (used in `<title>` + meta tags)
4. Push to `main` and trigger the revalidate webhook (or wait for the next cache miss)

### MDX frontmatter

```mdx
---
title: Getting Started
description: First-time setup when you launch your store
---

# Getting Started

…content…
```

### `_meta.js` shape

```js
export default {
  'getting-started': 'Getting Started',
  'next-page': 'Next Page',
  'advanced-topic': 'Advanced Topic',
}
```

The order in `_meta.js` is the order in the sidebar.

## Modules

- `platform/` — Store config, branches, users, payment methods, VAT
- `products/` — Catalog, variants, categories, size guides, reviews
- `customers/` — Profiles, addresses, credit terms, A/R ledger, segmentation
- `suppliers/` — Vendors, BD tax compliance, A/P ledger, opening balance
- `inventory/` — Stock, transfers, purchases, lots, RMA, warehouse tasks
- `warehouse-advanced/` — Cycle counting, lots, procurement, replenishment, cost layers, dispatch, quality
- `sales/` — Quotations: draft → send → accept → convert to order
- `pos/` — Point of sale terminal — shifts, sales, closing, troubleshooting
- `accounting/` — Chart of accounts, A/P, A/R, Mushak/VAT, day close, reports
- `promotions/` — Discount programs, vouchers, cart evaluation
- `loyalty/` — Members, earning rules, tiers, redemption, referrals
- `crm/` — Leads, opportunities, accounts, pipelines (SDK only, dashboard UI in development)

## Versioning strategy

We follow a **branch-per-major-release** model. Most contributors only ever touch `main`.

| Branch | Purpose |
|--------|---------|
| `main` | The current docs — always reflects what the latest production app does |
| `vN.M` | A frozen snapshot for a previous major release (e.g. `v1.0`, `v1.5`) |

### When to cut a version branch

When the production app makes a **breaking UX or workflow change** (e.g. the cart evaluation API is reshaped, the chart of accounts seed changes meaning):

```bash
# from main, before merging the breaking change
git checkout -b v1.5
git push origin v1.5
```

Now `main` continues with the new behaviour and `v1.5` is the last snapshot of the old one.

### How readers pin to a version

The Nextra renderer reads the branch from `COMMERCE_BD_DOCS_BRANCH` (env var on the FE app). Default: `main`.

To preview docs from `v1.5`:

```bash
# in classytic-fe
COMMERCE_BD_DOCS_BRANCH=v1.5 npm run dev
```

For production, you can deploy a **secondary route** (e.g. `/commerce-bd/v1.5/docs`) that hard-codes the branch, so old customers can keep reading their snapshot.

### Hotfixes to old versions

Apply the fix on the version branch directly, then cherry-pick to `main` if the issue exists there too:

```bash
git checkout v1.5
# fix the typo, push
git push origin v1.5

# if main has the same issue
git checkout main
git cherry-pick <commit>
git push origin main
```

### Don't

- Don't tag releases — tags can't be force-revalidated through the webhook the way branches can.
- Don't rewrite `main` history (force push, rebase) once an entry is published — readers may have bookmarked the file paths.
- Don't keep more than 2 active version branches. If `v1.0` is unsupported, archive it (read-only) instead of cutting `v1.6`, `v1.7`, …

## Local preview

To preview docs locally before pushing:

```bash
cd d:/projects/classytic/apps/classytic-fe
COMMERCE_BD_DOCS_BRANCH=<your-branch> npm run dev
# open http://localhost:3000/commerce-bd/docs
```

The fetcher always pulls from GitHub — there's no offline mode. Push to a branch first, then preview.

# Quality Inspection

Set up rules for inspecting goods and handle pass/fail results.

> This feature requires **Enterprise** mode. Contact your admin if you don't see the Quality tab.

---

## How It Works

1. You define **Quality Points** — rules that say "check this on receipt" or "check this on transfer"
2. When goods arrive, quality checks are generated automatically
3. Inspectors record pass/fail results
4. Failed items get a **disposition** — scrap, return to supplier, or hold for review

---

## Create a Quality Point

1. Go to **Warehouse > Quality**
2. Click **New Point**
3. Fill in:
   - **Name** — what you're checking (e.g. "Weight Check", "Visual Inspection")
   - **Type** — Pass/Fail, Measurement, Text Note, or Photo
   - **Trigger** — when to check: Receipt, Transfer, Shipment, or Return
4. Click **Create**

### Types explained

| Type | What the inspector does |
|------|------------------------|
| **Pass/Fail** | Clicks pass or fail |
| **Measurement** | Enters a number (e.g. weight in kg). You set min/max range. |
| **Text Note** | Types a description of the finding |
| **Photo** | Attaches a picture of the item |

### Scope

- Leave **SKU** blank to check all products
- Enter a specific SKU to check only that product

[Go to Quality](/dashboard/warehouse/quality)

---

## Inspect Goods

When a receipt or transfer comes in, checks are generated for matching quality points.

For each check:
1. Open the check
2. Enter the result (pass/fail, measurement value, or note)
3. Submit

Passed items continue to storage. Failed items need a disposition.

---

## Apply a Disposition

For failed checks, choose what happens to the goods:

| Disposition | What happens |
|-------------|-------------|
| **Accept** | Override — move to storage anyway |
| **Scrap** | Move to scrap location (written off) |
| **Return to Supplier** | Move to returns location |
| **Hold** | Keep in quality hold for further review |
| **Rework** | Send for rework (external process) |

Each disposition creates a stock move, so the audit trail is complete.

---

## What's next?

- [Warehouse Tasks & Scanning](/dashboard/inventory/learn/warehouse-tasks) — direct your team with scan-based tasks
- [Reports](/dashboard/inventory/learn/reports) — stock health and aging analysis

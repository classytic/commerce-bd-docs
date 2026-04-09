# Warehouse Tasks & Scanning

Use scanner-directed tasks to guide your warehouse team through picking, putaway, and counting.

> This feature requires **Enterprise** mode.

---

## How It Works

Instead of giving your team a paper list, the system tells each worker **exactly what to do**, step by step:

1. Worker **starts a session** on their device (phone, tablet, or scanner)
2. System assigns a **task** from the queue (pick item X from location A)
3. Worker follows **scan prompts** (scan location, scan item, confirm quantity)
4. Worker marks the task as **complete** or reports an **exception**
5. System assigns the **next task**

---

## Start a Session

1. Go to **Warehouse > Tasks**
2. Click **Start Session**
3. The system creates a session linked to you and the default queue

Once active, click **Next Task** to get your first assignment.

[Go to Tasks](/dashboard/warehouse/tasks)

---

## Follow Scan Prompts

Each task gives you step-by-step instructions:

| Step | What you see | What you do |
|------|-------------|-------------|
| 1 | "Go to location A-03-02-B" | Walk to that bin and scan its barcode |
| 2 | "Scan item SKU-WIDGET (5 remaining)" | Scan each item as you pick it |
| 3 | "Scan destination location PACK-01" | Scan the packing station barcode |

The prompts change based on task type:
- **Pick** — go to source, scan items, bring to destination
- **Putaway** — take received items, scan destination bin
- **Count** — go to location, count what's there, enter quantity

---

## Complete or Report Exception

### Complete
When all items are picked/placed, click **Complete**. The stock movement is posted automatically.

### Exception
If something goes wrong, click **Exception** and select a reason:

| Code | When to use |
|------|------------|
| **Short pick** | Not enough items at the location |
| **Damaged** | Items found damaged |
| **Wrong item** | Different item found than expected |
| **Location empty** | Nothing at the scanned location |
| **Barcode mismatch** | Scanned barcode doesn't match expected |

Exceptions are flagged for a supervisor to review.

---

## End Session

Click **End** to close your session. The system records how many tasks you completed.

---

## What's next?

- [Reports](/dashboard/inventory/learn/reports) — track warehouse performance
- [Quality Inspection](/dashboard/inventory/learn/quality-inspection) — inspect before shelving

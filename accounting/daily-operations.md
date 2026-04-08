# Daily Operations

What happens every business day.

---

## POS Day Close

At the end of each shift:

1. Go to **Day Close** in the sidebar
2. Select the business date (defaults to yesterday)
3. Click **Close Day**

This creates a summary entry for all POS sales that day.

> **Auto-close:** If you forget, the system catches up automatically the next time any request comes from that branch. No manual intervention needed.

> **Backfill:** If a branch was offline for multiple days, use the Backfill tool on the Day Close page. Select a date range (up to 90 days) and the system closes each missing day.

[Go to Day Close](/dashboard/accounting/posting)

---

## Record a Vendor Bill

When goods arrive from a supplier:

- Bills are posted **automatically** when a purchase is marked as received
- You can also post manually from the **Vendor Bills** page

The bill records what you owe the supplier and when it's due (based on their credit terms).

---

## Pay a Supplier

1. Go to **Vendor Bills** (or a supplier's **A/P Ledger** tab)
2. Find the open bill → click **Pay**
3. Enter the amount, select the source (Cash / Bank / Mobile Banking), add a reference
4. Click **Post payment**

**Partial payments** are supported — pay any amount up to the open balance. The bill stays open until fully paid.

**Over-payment protection** — the system rejects any amount exceeding the remaining balance.

[Go to Vendor Bills](/dashboard/accounting/vendor-bills)

---

## Post a Credit-Sale Invoice

For wholesale or business customers buying on credit:

1. Go to **Customer Invoices** (or a customer's **A/R Ledger** tab)
2. Post the invoice for the order

If the customer has a credit limit set and this invoice would push them over, the system **blocks the invoice** and shows the current balance vs limit.

> Cash sales (POS, online payments) are handled by Day Close and don't go through invoicing.

---

## Record a Customer Receipt

When a credit customer pays:

1. Go to **Customer Invoices** → find their open invoice
2. Click **Receive**
3. Enter amount, select destination account, add a reference
4. Click **Post receipt**

Partial receipts work the same as partial supplier payments.

[Go to Customer Invoices](/dashboard/accounting/customer-invoices)

---

## What's next?

- [Credit & Debit Notes](/dashboard/accounting/learn/credit-debit-notes) — handling returns and allowances
- [Reports](/dashboard/accounting/learn/reports) — aging, statements, financials

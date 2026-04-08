# Credit & Debit Notes

Handling returns, allowances, and price adjustments.

---

## Vendor Credit Note

When you return goods to a supplier or receive a price allowance:

1. Go to **Vendor Bills** → find the open bill
2. Click **Credit note**
3. Fill in:
   - **Amount** (BDT) — cannot exceed the bill's remaining balance
   - **Reference** (e.g. CN-001) — required
   - **Reason** (e.g. "Damaged goods returned") — required, minimum 3 characters
4. Click **Post credit note**

This reduces the amount you owe. The original bill stays unchanged in the records.

---

## Customer Debit Note

When a customer returns goods or you grant a price adjustment:

1. Go to **Customer Invoices** → find the open invoice
2. Click **Debit note**
3. Fill in amount, reference, and reason (same rules)
4. Click **Post debit note**

This reduces what the customer owes you.

---

## Required fields

Every credit/debit note requires:

- **Reference number** — used to prevent duplicates. If you submit the same reference + amount combination twice, the system returns the original result without creating a duplicate
- **Reason** — for audit trail. Must be at least 3 characters

---

## Effect on balances

Notes reduce the open balance on a bill or invoice. When the total of all payments + notes equals the original amount, the bill/invoice is automatically marked as settled.

**Example:**

| Event | Open balance |
|-------|-------------|
| Bill created: ৳50,000 | ৳50,000 |
| Credit note: ৳10,000 | ৳40,000 |
| Payment: ৳40,000 | ৳0 → settled |

---

## What's next?

- [Reports](/dashboard/accounting/learn/reports) — see how notes affect aging and statements
- [How Settlement Works](/dashboard/accounting/learn/settlement-model) — the full mechanics

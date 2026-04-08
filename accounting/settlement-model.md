# How Settlement Works

Bills and invoices are settled automatically when fully paid. This page explains what that means for you.

---

## The basics

When you post a bill for ৳100,000, it shows as "open" in your Vendor Bills list and A/P Aging report. As you make payments and post credit notes against it, the open balance decreases. When the balance reaches **zero**, the bill is automatically marked as **settled** and disappears from the open items list.

---

## Partial payments

You don't have to pay a bill in full at once. Make as many partial payments as needed:

| Action | Open balance |
|--------|-------------|
| Bill posted: ৳100,000 | ৳100,000 |
| Payment: ৳40,000 | ৳60,000 |
| Credit note: ৳10,000 | ৳50,000 |
| Payment: ৳50,000 | ৳0 → **Settled** |

The same applies to customer invoices — partial receipts reduce the open balance until it's zero.

---

## What "settled" means

Once settled:
- The bill/invoice **disappears** from the open items list and A/P/A/R aging
- All related items (the original + all payments + all notes) are **matched together**
- The **Partner Statement** still shows the full history — both matched and unmatched items

> You can't partially settle a bill. It's either fully open (has a balance) or fully settled (balance = zero). This keeps your books clean.

---

## Safety checks

- **Over-payment blocked** — you can't pay more than the remaining open balance
- **Over-reversal blocked** — credit/debit note amount can't exceed the remaining balance
- **Duplicate protection** — submitting the same payment or note twice is harmless (the system recognizes duplicates)
- **Concurrent users** — if two people pay the last portion simultaneously, both payments go through and the settlement still happens correctly

---

## Where to check

| What you want to see | Where to go |
|---------------------|-------------|
| All open (unsettled) supplier bills | **Vendor Bills** page |
| All open customer invoices | **Customer Invoices** page |
| Open items for a specific partner | Supplier/Customer detail → **Ledger** tab |
| Both open and settled history | **Partner Statement** |
| Aging breakdown of open items | **A/P Aging** or **A/R Aging** |

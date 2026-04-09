# Getting Started

First-time setup when you start using inventory management.

---

## 1. Make Sure Your Branches Are Set Up

Each branch (store, warehouse, outlet) needs to exist in the system before it can hold stock. Branches are created in **Settings > Branches**.

When you switch to a branch in the top bar, everything you see (stock levels, movements, transfers) is scoped to that branch only.

[Manage Branches](/dashboard/settings/branches)

---

## 2. Your Warehouse Is Created Automatically

The first time you open any inventory page for a branch, the system automatically creates:

- **1 warehouse node** (the branch's storage area)
- **4 locations**: Stock (main storage), Vendor (incoming), Customer (outgoing), Adjustment (corrections)

You don't need to set this up manually. It just works.

---

## 3. Add Your First Stock

There are two ways to get stock into the system:

### Option A: Record a Purchase

1. Go to **Inventory > Purchases**
2. Click **New Purchase**
3. Select a supplier, add products and quantities
4. Click **Create**
5. When goods arrive, click **Receive** on the purchase

This is the recommended way because it creates a full paper trail.

[Go to Purchases](/dashboard/inventory/purchases)

### Option B: Manual Adjustment

For existing stock you already have in the store:

1. Go to **Inventory > Stock Levels**
2. Find the product
3. Click **Set Stock** and enter the current quantity

This creates an adjustment record. Use it for initial stock setup or corrections.

[Go to Stock Levels](/dashboard/inventory)

---

## 4. Check Your Stock

After adding stock, you should see it on the **Stock Levels** page. The cards at the top show:

- **Total Products** with stock
- **Low Stock** items (below threshold)
- **Out of Stock** items

Click any card to filter the table.

---

## What's next?

- [Daily Stock Management](/dashboard/inventory/learn/daily-stock) — checking stock, handling alerts, scanning barcodes
- [Purchases & Receiving](/dashboard/inventory/learn/purchases-receiving) — ordering from suppliers

# Branch Transfers

Move stock between your branches (stores, warehouses, outlets).

---

## How Transfers Work

A transfer moves stock from one branch to another. It goes through these stages:

**Draft** > **Approved** > **Dispatched** > **Received**

- **Dispatching** decrements stock from the sending branch
- **Receiving** increments stock at the receiving branch
- Both sides see the transfer in their movements history

---

## Create a Transfer

1. Go to **Inventory > Transfers**
2. Click **New Transfer**
3. Select the **destination branch** (where stock is going)
4. Add products and quantities
5. Click **Create**

> You must be logged into the **sending branch** to create a transfer.

[Go to Transfers](/dashboard/inventory/transfers)

---

## Approve and Dispatch

1. Open the transfer
2. Click **Approve** (manager permission required)
3. Click **Dispatch** when goods leave the warehouse

At this point, the sending branch's stock goes down.

---

## Receive at Destination

1. Switch to the **receiving branch** in the top bar
2. Go to **Inventory > Transfers**
3. Find the incoming transfer
4. Click **Receive**

The receiving branch's stock goes up. The transfer is now complete.

---

## Stock Requests

Sub-branches can request stock from the head office:

1. Go to **Inventory > Requests**
2. Click **New Request**
3. Add the products and quantities you need
4. Submit the request

The head office sees the request and can approve/reject or create a transfer to fulfill it.

[Go to Stock Requests](/dashboard/inventory/requests)

---

## What's next?

- [Lots, Serials & Packages](/dashboard/inventory/learn/lots-packages) — tracking batches and containers
- [Daily Stock Management](/dashboard/inventory/learn/daily-stock) — adjustments and alerts

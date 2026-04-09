# Purchases & Receiving

How to order stock from suppliers and receive it into your warehouse.

---

## Create a Purchase Order

1. Go to **Inventory > Purchases**
2. Click **New Purchase**
3. Select a **supplier** (add one first in Suppliers if needed)
4. Add products: search by name or SKU, enter quantity and unit cost
5. Click **Create**

The purchase starts in **Draft** status.

[Go to Purchases](/dashboard/inventory/purchases)

---

## Approve a Purchase

Before goods can be received, the purchase needs approval:

1. Find the purchase in the list
2. Click **Approve** (or open it and use the action menu)

Only users with the purchase approval permission can do this.

---

## Receive Goods

When the supplier delivers:

1. Open the approved purchase
2. Click **Receive**
3. The system adds stock to your branch automatically

### What happens behind the scenes

- A receipt move is created (vendor location to your storage location)
- Stock quantities update instantly
- If the product has **lot tracking**, you'll enter lot codes during receiving
- If the product has **serial tracking**, each item gets a unique serial number

### Partial receiving

You can receive part of an order. The purchase stays open as **Partially Received** until all items arrive. Click **Receive** again for the next delivery.

---

## Pay the Supplier

If you use the accounting module:

1. Open the purchase
2. Click **Pay**
3. Enter amount, payment method (Cash / Bank / Mobile Banking), and reference
4. Click **Post Payment**

Partial payments are supported. The bill stays open until fully paid.

---

## Cancel a Purchase

You can cancel any purchase that hasn't been fully received:

1. Open the purchase
2. Click **Cancel** and enter a reason

Cancelled purchases remain visible in the list for audit purposes but cannot be edited or received.

---

## What's next?

- [Branch Transfers](/dashboard/inventory/learn/transfers) — moving stock between stores
- [Lots, Serials & Packages](/dashboard/inventory/learn/lots-packages) — batch and serial tracking

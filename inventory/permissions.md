# Roles & Permissions

Who can do what in inventory and warehouse management.

---

## Role Overview

| Role | What they can do |
|------|-----------------|
| **Superadmin** | Everything |
| **Admin** | Full stock control, purchases, transfers, warehouse management |
| **Branch Manager** | View stock, adjustments, receive transfers, create stock requests |
| **Inventory Staff** | View stock, movements, handle warehouse operations |
| **Cashier** | View stock levels only (for POS) |
| **Warehouse Staff** | Warehouse operations, task execution, scanning |
| **Warehouse Admin** | All warehouse features plus quality and dispatch management |

---

## Permission Details

### Stock & Purchases

| Action | Who can do it |
|--------|--------------|
| View stock levels | Admin, Branch Manager, Inventory Staff, Cashier |
| Adjust stock | Admin, Branch Manager |
| Create purchases | Admin (head office) |
| Approve purchases | Admin (head office) |
| Receive goods | Admin, Inventory Staff |
| Pay suppliers | Admin (head office) |

### Transfers

| Action | Who can do it |
|--------|--------------|
| Create transfers | Admin (head office) |
| Approve transfers | Admin |
| Dispatch transfers | Admin, Inventory Staff |
| Receive transfers | Admin, Branch Manager, Inventory Staff |
| View transfers | All inventory roles |

### Stock Requests

| Action | Who can do it |
|--------|--------------|
| Create requests | Branch Manager, Inventory Staff |
| Approve/reject requests | Admin (head office) |
| Fulfill requests | Admin |

### Warehouse (Standard+)

| Action | Who can do it |
|--------|--------------|
| Manage lots & serials | Admin, Warehouse Admin |
| Manage packages (pack/unpack/relocate) | Admin, Warehouse Admin |
| Create procurement orders | Admin |
| Manage replenishment rules | Admin |
| View cost & valuation | Admin |

### Enterprise Features

| Action | Who can do it |
|--------|--------------|
| Quality inspection (create points, record results) | Admin, Warehouse Admin |
| Execute tasks (pick, putaway, scan) | Warehouse Staff, Warehouse Admin |
| Dispatch management (manifests, docks) | Admin, Warehouse Admin |
| Traceability & reports | Admin |

---

## Branch Scoping

All permissions are scoped to the **active branch**. An admin at Branch A cannot see or modify stock at Branch B unless they switch branches.

The only exception is **View All** — admins can see stock across all branches from the Availability Matrix report.

---

## What's next?

- [Getting Started](/dashboard/inventory/learn/getting-started) — initial setup
- [Daily Stock Management](/dashboard/inventory/learn/daily-stock) — everyday operations

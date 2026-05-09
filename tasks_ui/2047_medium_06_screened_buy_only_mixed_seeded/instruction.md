Handle the list of live Sensor Cable Harness order demands.

- Nexus Studios North: 14 units due in 8 days (pretax budget cap $2,599)
- Trellis Architects: 26 units due in 9 days (pretax budget cap $6,485)
- Slate Studios East: 14 units due in 11 days (pretax budget cap $3,516)
- Westfield Brands: 19 units due in 11 days (pretax budget cap $4,901)
- Helix Institute: 14 units due in 12 days (pretax budget cap $3,501)
- Osprey Pictures: 23 units due in 12 days (pretax budget cap $6,012)
- Quantum Bureau: 25 units due in 14 days (pretax budget cap $6,186)
- Pivot Studios South: 18 units due in 14 days (pretax budget cap $4,616)
- Keystone Media: 18 units due in 14 days (pretax budget cap $4,415)

We have 74 finished units on hand. There is no in-house manufacturing route for the finished product, so any shortfall has to come from vendors.

Across all units covered through new purchasing or manufacturing, keep portfolio-level new-spend margin at or above 27.4% at selling price.

## Background & Policy

* The rules for which orders can be accepted are outlined below.
* Only accept orders whose budgets cover the full list-price total.
* Accepted orders must request between 15 and 22 units.
* Reject or cancel any order that fails those acceptance rules.
* For every accepted order, provide supply coverage with minimal new spend.
* The combined units covered through new purchasing or manufacturing must clear at least 27.4% portfolio-level new-spend margin at selling price.
* Accounting treats the existing stock as sunk cost.
* Some sales documents may already exist in draft; review existing documents before creating new ones.
* Cancel any already-drafted sales order that fails those acceptance rules.
* Customer budgets are pre-tax amounts.
* Link every accepted Sales Order to the related Purchase Orders for traceability.
* For finished goods POs, put the SO reference(s) (e.g. S00030 or S00030, S00031) into the origin field ('Source' in the UI).
* In the end, the lineage must be SO -> PO for every incoming customer order you accept.
* You must sell this product at List Price.
* On every accepted Sales Order, set the commitment date.
* On purchase orders, you must set the delivery date.
* Check Internal Notes/comments on stock, customers, and vendors before you release anything.

Fulfillment constraints for accepted orders:
- No in-house manufacturing capacity is available.
- For each finished-goods supplier offer used to fulfill accepted orders, respect min/max quantities as horizon-wide totals.
- Use one consolidated PO per supplier offer when fulfilling accepted orders (do not split a single offer across multiple POs).
- Check each vendor's Internal Notes in Odoo for fulfillment-side maximum order quantity limits.

## Execution Autonomy

Work with full autonomy. Do not ask the user for confirmation, approval, or preferences before acting. Make the best valid plan from the available Odoo data and execute it completely in Odoo. If multiple feasible plans satisfy the constraints, choose the one that best optimizes the stated objective.

---

# Odoo Environment

Access Odoo in the browser at:

- **URL:** http://127.0.0.1:8069
- **Database:** bench
- **Login:** admin
- **Password:** pass

Interact with Odoo only through the web UI. Do not use Odoo models, direct database access, API calls, or scripts.

## Using Odoo in the Browser

Open Odoo at `http://127.0.0.1:8069/web/login` and sign in.

Odoo is organized into apps. Use the app menu in the top-left corner to switch between Sales, Purchase, Inventory, Manufacturing, Invoicing, Contacts, Products, and other areas. Inside an app, use the top navigation, breadcrumbs, search bar, and list views to move around.

Most pages follow the same pattern: search for an existing record from a list, open it to inspect or edit it, or click `New` to create a new record. Record forms usually have their main actions at the top, such as `Save manually`, `Confirm`, `Validate`, `Create Invoice`, `Send by Email`, or `Discard changes`.

## Sales

Use Sales to manage quotations and sales orders.

Typical flow:

1. Open Sales.
2. Go to Quotations or Orders.
3. Click `New` to create a quotation.
4. Choose a customer.
5. Add products in the Order Lines table.
6. Adjust quantity, unit price, taxes, or payment terms.
7. Click `Save manually`.
8. Click `Confirm` to turn the quotation into a sales order.

## Contacts

Use Contacts to find or manage customers, vendors, and companies.

Typical tasks:

1. Open Contacts.
2. Search for a person or company by name or reference.
3. Open the contact to inspect addresses, internal notes, sales/purchase settings, and related documents.
4. Click `New` to create a new customer or vendor.

## Products

Use Products to inspect sellable or purchasable items.

Typical tasks:

1. Open Products from Sales, Inventory, or Purchase.
2. Search by product name, internal reference, or code.
3. Open the product to check pricing, availability, variants, vendors, routes, and inventory settings.
4. Edit fields and click `Save manually` when needed.

## Purchase

Use Purchase to manage vendor requests and purchase orders.

Typical flow:

1. Open Purchase.
2. Go to Requests for Quotation or Purchase Orders.
3. Click `New`.
4. Choose a vendor.
5. Add products, quantities, and prices.
6. Save the document.
7. Confirm the order when ready.

## Inventory

Use Inventory to inspect stock, deliveries, receipts, and transfers.

Typical tasks:

1. Open Inventory.
2. Use Products to check on-hand and forecast quantities.
3. Use Operations to inspect Receipts, Deliveries, or Internal Transfers.
4. Open a transfer to review move lines.
5. Use `Validate` when a receipt or delivery is ready to complete.

## Invoicing

Use Invoicing to manage customer invoices, vendor bills, and payments.

Typical tasks:

1. Open Invoicing.
2. Search invoices or bills by customer, vendor, date, status, or document number.
3. Open an invoice to review lines, taxes, totals, and payment status.
4. Use actions such as `Confirm`, `Register Payment`, or `Reset to Draft` depending on the document state.

## Manufacturing

Use Manufacturing to manage manufacturing orders, work orders, and production flow.

Typical tasks:

1. Open Manufacturing.
2. Go to Manufacturing Orders or Work Orders.
3. Search by product, reference, or status.
4. Open an order to inspect components, operations, quantities, and deadlines.
5. Use actions such as `Confirm`, `Plan`, `Mark as Done`, or work-order controls when available.

## General Tips

Autocomplete fields, such as Customer, Vendor, Product, or Payment Terms, usually work by typing a few characters and selecting the matching suggestion.

Tables often contain inline editable rows. For example, order lines may expose product, description, quantity, unit price, and taxes directly inside the table.

If a form has unsaved changes, use `Save manually` before navigating away. Use breadcrumbs to return to the parent list, such as Quotations, Products, Contacts, or Manufacturing Orders.

Use the search bar on list pages before scrolling. Odoo list views can contain many records, and search is usually faster than browsing manually.

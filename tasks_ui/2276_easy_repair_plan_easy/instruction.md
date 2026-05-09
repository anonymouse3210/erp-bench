Existing confirmed sales orders and current supply commitments for Ceiling Acoustic Baffle are already in Odoo. Vantage Consolidators has canceled on us, so that confirmed purchase order can no longer be relied on. Reuse the existing sales orders, review the commitments already in place, cancel that purchase order, keep unaffected work where it still makes sense, and adjust the plan for Eclipse Pictures, Oxide Institute, and Forge Group using the best feasible alternative source or fulfillment route.

- Sterling Cooperative: 5 units due in 6 days (pretax budget cap $1,610)
- Eclipse Pictures: 11 units due in 8 days (pretax budget cap $3,828)
- Oxide Institute: 5 units due in 9 days (pretax budget cap $1,667)
- Forge Group: 7 units due in 9 days (pretax budget cap $2,271)

We have 3 finished units on hand. The finished product is not manufactured in-house, so any shortfall has to be sourced from vendors.

Across all units covered through new purchasing or manufacturing, keep portfolio-level new-spend margin at or above 26.7% at selling price.

## Background & Policy

* Keep the committed orders on track while changing as little of the current plan as practical. If more than one feasible option preserves the same amount of prior work, keep new purchasing and manufacturing spend as low as possible.
* The combined units covered through new purchasing or manufacturing must clear at least 26.7% portfolio-level new-spend margin at selling price.
* Existing stock is a sunk cost and should not be treated as new spend.
* The listed customer sales orders are already confirmed in Odoo; work from those orders and do not create duplicates.
* Review the current purchase orders, manufacturing orders, and supplier or workcenter notes before making changes.
* Keep commitments that still work; only rework the part of the plan affected by the disruption.
* A confirmed purchase order from Vantage Consolidators is already in Odoo, but the supplier has canceled on us.
* Cancel that purchase order and cover the gap with the best feasible alternative source or fulfillment route without sending the same demand back down that supplier path.
* Link every accepted Sales Order to the related Purchase Orders for traceability.
* For finished goods POs, put the SO reference(s) (e.g. S00030 or S00030, S00031) into the origin field ('Source' in the UI).
* In the end, the lineage must be SO -> PO for every incoming customer order you accept.
* You must sell this product at List Price.
* On every accepted Sales Order, set the commitment date.
* On purchase orders, you must set the delivery date.
* Check Internal Notes/comments on stock, customers, and vendors before you release anything.

Capacity constraints:
- No in-house manufacturing capacity is available.
- For each finished-goods supplier offer, respect min/max quantities as horizon-wide totals.
- That supplier commitment has fallen through and must not be reused.
- Use one consolidated PO per supplier offer (do not split a single offer across multiple POs).
- Check each vendor's Internal Notes in Odoo for maximum order quantity limits.

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

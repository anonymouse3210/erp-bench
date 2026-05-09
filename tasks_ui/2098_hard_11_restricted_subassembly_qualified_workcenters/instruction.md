Prepare a fulfillment strategy for all listed Carport Solar Canopy Module orders to meet due dates and avoid shortages.

- Globe Forum: 16 units due in 8 days (pretax budget cap $64,128)
- Peak Systems: 20 units due in 8 days (pretax budget cap $84,151)
- Bridgeway Foundry: 18 units due in 9 days (pretax budget cap $73,408)
- Catalyst Collective: 24 units due in 10 days (pretax budget cap $96,470)
- Northbridge Manufactory: 15 units due in 11 days (pretax budget cap $60,765)
- Forge Studios East: 17 units due in 12 days (pretax budget cap $71,624)
- Horizon Clinics: 20 units due in 12 days (pretax budget cap $83,563)
- Equinox Refinery: 22 units due in 12 days (pretax budget cap $88,815)

We have 31 finished units on hand. If stock runs short, you can close the gap with finished-goods purchasing, in-house manufacturing, or a combination of the two.

Across all units covered through new purchasing or manufacturing, keep portfolio-level new-spend margin at or above 27.3% at selling price.

## Background & Policy

* Fulfill all orders while minimizing new spending on procurement and manufacturing.
* Any units you cover through new buying or manufacturing count toward one combined portfolio that must still meet a minimum 27.3% new-spend margin at selling price.
* Finance considers the existing stock as sunk cost.
* You must create and confirm the necessary sales orders, purchase orders, and/or manufacturing orders.
* Customer budgets are pre-tax amounts.
* Link Sales Orders to the related Manufacturing Orders and Purchase Orders for traceability.
* For finished goods POs, put the SO reference(s) (e.g. S00030 or S00030, S00031) into the origin field ('Source' in the UI).
* For component POs, put the MO reference(s) (e.g. WH/MO/00010 or WH/MO/00010, WH/MO/00011) into the origin field.
* For finished goods MOs, put the Sales Order reference (e.g. S00030) into the origin field ('Source' in the UI).
* For subassembly or intermediate MOs, put the immediate parent MO reference(s) that the subassembly feeds (e.g. WH/MO/00020 or WH/MO/00020, WH/MO/00021) into the origin field ('Source' in the UI).
* In the end, the lineage must be SO -> MO -> (Subassembly MO if needed) -> PO or SO -> PO.
* You must sell this product at List Price.
* On sales orders, set the commitment date.
* On manufacturing orders, you must set the start date and the due date.
* If you choose to manufacture, you must procure the components that are not in stock.
* On purchase orders, you must set the delivery date.
* Before releasing anything, read the Internal Notes/comments on stock, customers, vendors, and workcenters.

Capacity constraints:
- Treat workcenter capacity as a hard horizon-wide limit across all products that share the center.
- Check each workcenter's Internal Notes in Odoo for the exact horizon-wide minute limit.
- Assign workcenter on each manufacturing work order.
- For each finished-goods supplier offer, respect min/max quantities as horizon-wide totals.
- For each component supplier offer, respect min/max quantities as horizon-wide totals.
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

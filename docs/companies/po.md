---
title: Purchase Order
---

## Purchase Orders

Purchase orders allow to track which parts are bought from suppliers and manufacturers, therefore converting externally bought items into stock items / inventory.

To access the purchase order page, click on the <span class="badge inventree nav main"><span class='fas fa-shopping-cart'></span> Buy</span> navigation tab and click on <span class="badge inventree nav main"><span class='fas fa-list'></span> Purchase Orders</span> option in the dropdown list.

### Create Purchase Order

Once the purchase order page is loaded, click on <span class="badge inventree add"><span class='fas fa-plus-circle'></span> New Purchase Order</span> which opens the "Create Purchase Order" form.

A purchase order is linked to a specific supplier, select one in the list of existing suppliers.

!!! warning
	Only companies with the "Supplier" attribute enabled will be shown and can be selected

Fill out the rest of the form with the purchase order information then click on <span class="badge inventree confirm">Submit</span> 

### Add Line Items

On the purchase order detail page, user can link parts to the purchase order selecting the <span class="badge inventree nav side"><span class='fas fa-list'></span> Order Items</span> tab then clicking on the <span class="badge inventree add"><span class='fas fa-plus-circle'></span> Add Line Item</span> button.

Once the "Add Line Item" form opens, select a supplier part in the list.

!!! warning
    Only parts from the supplier selected for the purchase order will be shown and can be selected

Fill out the rest of the form then click on <span class="badge inventree confirm">Submit</span> 

#### Upload File

It is possible to upload an exported purchase order from the supplier instead of manually entering each line item. To start the process, click on <span class="badge inventree confirm"><span class='fas fa-upload'></span> Upload File</span> button next to the <span class="badge inventree add"><span class='fas fa-plus-circle'></span> Add Line Item</span> button and follow the steps.

!!! info "Supported Formats"
	This process only supports tabular data and the following formats are supported: CSV, TSV, XLS, XLSX, JSON and YAML

### Issue Order

Once all the line items were added, click on the <span class='fas fa-paper-plane'></span> button on the main purchase order detail panel and confirm the order has been submitted.

### Receive Line Items

After receiving all the items from the order, the purchase order will convert the line items into stock items / inventory.

There are two options to mark items as "received":

* either individually: click on <span class='fas fa-clipboard-check'></span> button on each line item
* or globally: click on the <span class='fas fa-clipboard-check'></span> button on the main purchase order detail panel and confirm all items in the order have been received.

### Received Items

Each item marked as "received" is automatically converted into a stock item.

To see the list of stock items created from the purchase order, click on the <span class="badge inventree nav side"><span class='fas fa-sign-in-alt'></span> Received Items</span> tab.

### Complete Order

Once the quantity of all __received__ items is equal or above the quantity of all line items, the order will be automatically marked as __complete__.

It is also possible to complete the order before all items were received (or if there were missing items).
To do so, click on the <span class='fas fa-check-circle'></span> button on the main purchase order detail panel and confirm the order was completed.

### Cancel Order

In the event that the order won't be processed, user has the option of cancelling the order instead.
To do so, simply click on the <span class='fas fa-times-circle'></span> button on the main purchase order detail panel and confirm the purchase order has been cancelled.

---
title: Amazon Fulfillment Workflows
description: Fulfillment for an order from an Amazon listing follows a specific sequence from order submission to shipping.
---

# Amazon fulfillment workflows

## Example: fulfilled by merchant

|**Step** | **Description** |
|----|----|
|1| **A merchant-fulfilled order is placed on Amazon.** Amazon assigns a status of `Pending` until the customer's credit card information is verified. Orders in `Pending` status automatically import into [!DNL Amazon Sales Channel] but do not display on the _Orders_ tab.|
|2| **The order is verified by Amazon.** When verified, Amazon changes the status to `Unshipped`. With this status change, the order is updated in [!DNL Amazon Sales Channel] and appears in the _Orders_ tab.|
|3| **The order details are updated.** [!DNL Amazon Sales Channel] updates the order details with the price, customer email, and customer name. During this update, the Amazon order will create the corresponding [!DNL Commerce] order in the order management page. The [!DNL Commerce] order number will display with the order information on the _Orders_ tab.|
|4| **A new customer account is created.** If configured in your order settings and the customer does not exist in your [!DNL Commerce] database, a new customer is created in your [!DNL Commerce] database using the corresponding customer information from the Amazon order. If you chose `No Customer Creation (guest)` in your order settings, the order will follow the [!DNL Commerce] guest process and not create a new customer in your database. At this point, if your [!DNL Commerce] system is integrated with an ERP/OMS/WMS, the order will be picked up per the integration of a new order being placed and created inside [!DNL Commerce].|
|5| **The order is shipped.** From the [!DNL Commerce] order processing page, you will ship the order and add a tracking number. When all items are marked in a `Shipped` status:<ul><li>The status of the [!DNL Commerce] order will change to `Complete`.</li><li>The status of the [!DNL Amazon Sales Channel] order will change to `Shipped`.</li><li>The tracking number will be synced to Amazon, and the status of the order in Amazon will change to `Shipped`.</li><li>Shipping notifications will be sent to the customer via Amazon, not from [!DNL Commerce] (per Amazon’s policies).|

## Example: fulfilled by Amazon (FBA)

|**Step** | **Description** |
|---|---|
|1| **An Amazon-fulfilled order is placed on Amazon.** |
|2| **The order is imported.** The order is not imported into [!DNL Amazon Sales Channel] until the order is assigned the `Shipped` status by Amazon. Since Amazon has the inventory for this product, this prevents interference with your warehouse/inventory management. |
|3| **The order details are updated.** If configured in your [order settings](./order-settings.md), the Amazon order will create the corresponding [!DNL Commerce] order and be created as an order with a status of `Complete`. |

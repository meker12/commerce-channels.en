---
title: "Manage [!DNL Walmart Marketplace] Orders"
description: "View and manage [!DNL Walmart Marketplace] orders with [!DNL Channel Manager] for Adobe Commerce and Magento Open Source."
exl-id: c2779c72-4793-445c-858a-867ea8389662
---
# Manage [!DNL Walmart Marketplace] orders

[!DNL Walmart Marketplace] order data for [!DNL Commerce] products synchronizes automatically to [!DNL Channel Manager] after [!DNL Walmart] processes the order.

On the Commerce side, a successful synchronization triggers the following actions:

- [!DNL Channel Manager] sends an order acknowledgment to Walmart.

- A corresponding Commerce order is created from the Walmart order.

- The updated order information displays on the [!DNL Channel Manager] Orders dashboard.

In the storefront Admin, you can view order data from [!DNL Channel Manager] by opening the sales channel store and selecting **[!UICONTROL Orders]**.

![Channel Manager Orders view to manage [!DNL Walmart Marketplace] orders](assets/orders-dashboard-view.png)

>[!NOTE]
>
>It can take up to 35 minutes for a [!DNL Walmart Marketplace] order to display in the [!DNL Channel Manager] orders list. [!DNL Walmart] requires approximately 30 minutes to process incoming orders and send them to [!DNL Channel Manager]. After Channel Manager receives the order, it takes approximately five more minutes to create and display the order in Adobe Commerce or Magento Open Source.

## Orders Controls and Column Descriptions

The following tables describe the controls and columns available for Orders.

**Controls for [!UICONTROL Orders]**
| **Control**                    | **Description**                                                                                                                                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter orders]     | Sort the view by selecting one of the [!UICONTROL Order Status] cards.                                                                                                                                                                                                           |
| Error Description              | Provides more detailed information about orders with an Error status.                                                                                                                                                                                                            |
| [!UICONTROL View order detail] | To view order details, select the [!DNL Commerce] order number in the [!UICONTROL Order] table. Then, use [!DNL Commerce] order options to process the order.                                                                                                                    |
| [!UICONTROL Channel Settings]  | To modify the channel configuration, select channel Walmart Connection credentials, mapped attributes, or shipping identifiers, settings  select the [!DNL Commerce] order number in the [!UICONTROL Order] table. Then, use [!DNL Commerce] order options to process the order. |


**Column descriptions**

| Field                              | Description                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | The purchase order number assigned to the order in the [!DNL Walmart Marketplace]. When an order is initially imported to [!DNL Channel Manager], only the [!DNL Walmart] order number displays. When the [!DNL Commerce] order is created, the [!DNL Walmart] order number is stored in the [!UICONTROL External ID] product attribute.                                  |
| [!DNL Commerce]  Order Number      | The number assigned to the [!DNL Commerce]  order created from the [!DNL Walmart Marketplace] order.                                                                                                                                                                                                                                                                      |
| Items                              | Number of items ordered on [!DNL Walmart Marketplace].                                                                                                                                                                                                                                                                                                                    |
| [!UICONTROL Order Value]           | Total cost of the ordered items.                                                                                                                                                                                                                                                                                                                                          |
| [!UICONTROL Date Ordered]          | The date the order was submitted on the [!DNL Walmart Marketplace].                                                                                                                                                                                                                                                                                                       |
| [!UICONTROL Ship By Date]          | Date the order must be shipped by to meet [!DNL Walmart Marketplace] requirements.                                                                                                                                                                                                                                                                                        |
| [!UICONTROL Deliver By Date]       | Date the order must be delivered to customer to meet [!DNL Walmart Marketplace] requirements in UTC format.                                                                                                                                                                                                                                                               |
| [!UICONTROL Ship Method]           | The [!DNL Walmart Marketplace] Shipping Method selected for the order. For details about the possible values, see [Shipping Methods and Timing Policy](https://sellerhelp.walmart.com/s/guide?article=000007893) in the _[!DNL Walmart Marketplace Seller Help]_.                                                                                                         |
| [!UICONTROL Last Update At]        | Timestamp indicating the last time the order data was updated in [!DNL Channel Manager] in UTC format.                                                                                                                                                                                                                                                                    |
| [!UICONTROL Status]                | Indicates the current order status in the [!DNL Commerce] order workflow. The initial status for an order imported from [!DNL Walmart Marketplace] is _Open_. Additional status updates occur when Commerce orders are processed and [!Channel Manager] successfully synchronizes shipment, partial shipment, and cancellation updates to the [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description]     | Provides more detailed information about orders with an _[!UICONTROL Error]_ status.                                                                                                                                                                                                                                                                                      |

## Order Status


[!UICONTROL Order Status] provides information about the current state of [!DNL Walmart Marketplace] orders managed from Adobe Commerce or Magento Open Source. Order status updates occur when [!DNL Channel Manager] receives updated order information from either the [!DNL Walmart Marketplace] or the [!DNL Commerce] order system. Orders can have the following statuses:           

- **[!UICONTROL Shipped]**–Orders that have been shipped from the [!DNL Commerce] store. When the order ships, [!DNL Channel Manager] sends an update to [!DNL Walmart Marketplace] to update the shipping status on Walmart and provide the order tracking number for the shipment.

- **[!UICONTROL Partially Shipped]**—Orders that have some items marked as shipped, and others waiting to be shipped. When items in the order ship, [!DNL Channel Manager] sends an update to [!DNL Walmart Marketplace] to update the shipping status to paritally shipped on Walmart and provide the order tracking number for the shipment. 

- **[!UICONTROL Canceled]**–Orders that have been canceled from the [!DNL Commerce] store.

  After the order cancellation completes, the [!DNL Commerce] stock quantity updates to reflect returned items. Then, [!DNL Channel Manager] syncs the update to the [!DNL Walmart Marketplace].

- **[!UICONTROL Error]**– Orders that have errors. Errors can occur when an order update operation fails. For example, errors occur if [!DNL Channel Manager] cannot receive a new order from Walmart. They can also occur if [!DNL Channel Manager] cannot send an order shipment or cancellation update to the [!DNL Walmart Marketplace]. If an operation fails, the Orders page shows an _Error_ status for the order. For details, see [Fix order errors](process-orders.md#fix-shipping-and-cancellation- errors).

- **[!UICONTROL Error description]**–Provides detailed information about order errors that occur due to issues like 
missing information or invalid values, incorrect shipment details, or a failed order cancellation. The description helps determine whether error occurred on the [!DNL Commerce] instance or on the [!DNL Walmart Marketplace].

>[!NOTE]
>
>If order items are sent in multiple shipments, the order status in [!DNL Channel Manager] reflect the last order status available. For example, if the first item ships and no errors are returned when order updates are synchronized to [!DNL Channel Manager] and [!DNL Walmart Marketplace], the [!DNL Channel Manager] order status is _[!UICONTROL Partially Shipped]_.  If a second item is shipped and [!Channel Manager] returns an error, the order status updates to _[!UICONTROL Error]_.

## Review Orders

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** to open the [!UICONTROL Channel Manager Marketplace Stores] page.

1. Open the store view by selecting the eye icon in a store entry row.

1. To view order information, select *[!UICONTROL *Orders]**.

1. Get information about the order and determine next steps by checking the **[Status](#about-order-status)** column to get information about the orders.

## View Order Detail

After an order is received from the marketplace and imported into the Adobe Commerce or Magento Open Source, use the [!DNL Commerce] Order ID to view the order in Adobe Commerce.

From **[!UICONTROL Orders]**, select the **[!UICONTROL Commerce Order Number]** to open the [!DNL Commerce] order detail.

![Commerce Order detail view for a [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

In the Commerce storefront, orders imported from [!DNL Walmart Marketplace] have the following additional information included in the order data:

- **Payment Information & Shipping Method**–Orders imported from Walmart include following values for payment and shipping fields:

  - **[!UICONTROL Offline Channel Payment]**—Indicates that order payment is processed offline by [!DNL Walmart Marketplace].

  - **[!UICONTROL External Order Number]**—Displays the [!DNL Walmart Marketplace] order number.

  - **[!UICONTROL Channel Shipping - Value]**–Indicates that shipping charges are handled through [!DNL Walmart Marketplace].

  - **[!UICONTROL Cancellation Reason]**–This field displays only if an order imported from [!Walmart Marketplace] is canceled. Cancellation reasons include:

    - Price or other listing errors.
    - The item is out of stock.
    - Unavailable carrier or shipping information.
    - Additional information is required by our Credit or Fraud Avoidance department.

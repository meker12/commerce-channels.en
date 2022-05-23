---
title: Process orders
description: Instructions for shipping and cancelling [!DNL Walmart Marketplace] orders from Adobe Commerce and Magento Open Source.
---

# Process orders

If you use Adobe Commerce and Magento Open Source Order Management to manage your [!DNL Commerce] store sales, you process [!DNL Walmart Marketplace] orders from Commerce using a similar workflow.

When you process an order in Commerce, Channel Manager synchronizes updates to [!DNL Walmart Marketplace]. This update ensures that the product inventory and order status from Commerce matches the data tracked in the [!DNL Walmart Marketplace] and notifies Walmart to send order status and shipping information to customers.

>[!NOTE]
>
> It can up to 5 minutes for the order updates to synchronize to [!DNL Walmart Marketplace]. To check the order status, return to [!DNL Channel Manager] Orders.

## Ship an order

When you ship an order from Commerce, you use the [[!DNL Commerce Order Management] shipping workflow](https://docs.magento.com/user-guide/sales/order-ship.html). After you submit the order, updates are synchronized to [!DNL Walmart Marketplace]. Then, Walmart notifies customers about the order status and shipping details.

**Prerequisite**

Before shipping orders, verify that the [channel shipping settings and carrier configuration](map-shipping-carriers.md) meet [!DNL Walmart Marketplace requirements].

## Create and submit order shipment

When you ship a [!DNL Walmart Marketplace] order from [!DNL Commerce], you must add a tracking number. Customers receive the tracking number in the shipment notification they receive from from [!DNL Walmart]. 

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** to open the [!UICONTROL Channel Manager Marketplace Stores] page.

1. Open the store view by selecting the eye icon for a sales channel store.

1. To view [!DNL Walmart Marketplace] orders, select *[!UICONTROL *Orders]**.

1. In the Orders table, open the order to ship by selecting the **Commerce Order Number**.

1. Create and submit a shipment for all or part of an order by selecting **[!UICONTROL Ship]**.

   - To choose a shipping carrier and add a tracking number, select **[!UICONTROL Add tracking number]**.
   
   - Complete the rest of shipping form as needed. See [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) for detailed instructions.

1. After submitting the shipment, track the [order status](manage-orders.md#about-order-status) in [!DNL Channel Manager] to verify that updates were sent to [!DNL Walmart Marketplace].

## Cancel an order

When you cancel a [!DNL Walmart Marketplace] order, Walmart requires a cancellation reason. When the order cancellation updates to Walmart, the cancellation reason is included in the cancellation notice sent to the customer.

The cancellation reason is also displayed in the [!DNL Commerce] order payments information.

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** to open the [!UICONTROL Channel Manager Marketplace Stores] page.

1. Open the store view by selecting the eye icon for a sale channel store.

1. To view [!DNL Walmart Marketplace] orders, select *[!UICONTROL *Orders]**.

1. In the Orders table, open the order detail page by selecting the **Commerce Order Number** for the order to cancel.

   ![Commerce Order detail view for a Walmart Marketplace order](assets/order-detail-with-external-order-id.png)

1. Cancel the order.

   - Select **Cancel** from the Order Detail menu.

   - On the Cancel Order form, select the **Cancellation reason**.

      ![Commerce Order detail view for a Walmart Marketplace order](assets/order-detail-with-external-order-id.png)

   - Select **Cancel Order**.

1. Verify that updates were sent to [!DNL Walmart Marketplace] by checking the [order status](manage-orders.md#about-order-status) in [!DNL Channel Manager].

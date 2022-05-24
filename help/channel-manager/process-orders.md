---
title: Process orders
description: Instructions for shipping and cancelling [!DNL Walmart Marketplace] orders from Adobe Commerce and Magento Open Source.
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
---
# Process orders

If you use Adobe Commerce and Magento Open Source Order Management to manage your [!DNL Commerce] store sales, you can process [!DNL Walmart Marketplace] orders from Commerce using the same workflow.

When you process an order in Commerce, Channel Manager synchronizes updates to [!DNL Walmart Marketplace]. This update ensures that the order status and shipping information from Commerce matches the data tracked in the [!DNL Walmart Marketplace].

* **Order shipments**–Walmart requires a tracking number for all shipments. You can create partial shipments if you do not have stock for all items in the order. After you submit the shipment, order updates are synchronized to [!DNL Walmart Marketplace]. Then, Walmart notifies customers about the order status and shipping details.

* **Order cancellations**–When you cancel a [!DNL Walmart Marketplace] order, Walmart requires a cancellation reason which is included in the order cancellation notice sent to the customer. The cancellation reason is also displayed in the [!DNL Commerce] order payments information.

>[!NOTE]
>
> It can up to five minutes for order updates to synchronize to [!DNL Walmart Marketplace]. To check the order status, return to the [!DNL Channel Manager] Orders page.

## Ship an order

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Open the store view by selecting the eye icon for a sales channel store.

1. To view [!DNL Walmart Marketplace] orders, select *[!UICONTROL *Orders]**.

1. In the Orders table, open the order to ship by selecting the **Commerce Order Number**.

1. Create and submit a shipment for all or part of an order by selecting **[!UICONTROL Ship]**.

   ![Commerce Order detail view for a Walmart Marketplace order](assets/order-detail-with-external-order-id.png)

   * Choose a shipping carrier and add a tracking number by selecting **[!UICONTROL Add tracking number]**.
   
   * Complete the rest of shipping form as needed. See [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) for detailed instructions.

1. After submitting the shipment, track the [order status](manage-orders.md#about-order-status) in [!DNL Channel Manager] to verify that updates were sent to [!DNL Walmart Marketplace].

## Cancel an order

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Open the store view by selecting the eye icon for a sale channel store.

1. To view [!DNL Walmart Marketplace] orders, select *[!UICONTROL *Orders]**.

1. In the Orders table, open the order detail page by selecting the **Commerce Order Number** for the order to cancel.

   ![Commerce Order detail view for a Walmart Marketplace order](assets/order-detail-with-external-order-id.png)

1. Cancel the order.

   * Select **Cancel** from the Order Detail menu.

   * On the [!UICONTROL Cancel Order] form, select the **Cancellation reason**.

   ![Commerce Order detail view for a Walmart Marketplace order](assets/cancel-order-reason-selector.png)

   * Select **Cancel Order**.

1. After submitting the cancellation, track the [order status](manage-orders.md#about-order-status) in [!DNL Channel Manager] to verify that updates were sent to [!DNL Walmart Marketplace].

---
title: Return and Refund
description: 'Instructions for issuing full or partial refunds for Return Merchandise Authorization (RMA) requests received from [!DNL Walmart Marketplace] from [!DNL Channel Manager] for Adobe Commerce and Magento Open Source.'
---
# Return and refund orders

When a customer returns order items to [!DNL Walmart Marketplace], Walmart issues a Return Merchandise Authorization (RMA) request. [!DNL Channel Manager] monitors the marketplace channel for these requests and automatically synchronizes RMA information to Channel Manager.

On the Commerce side, the RMA request initiates the following workflow:

* Channel Manager creates a corresponding return request with a received status and adds the RMA to the [!UICONTROL Returns] dashboard. On the Orders dashboard, the status detail for the order associated with the RMA updates to show that a return was requested.

* Merchants process the RMA by creating a Credit Memo, following the [Adobe Commerce refund workflow](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). All refunds are processed using the offline method.

* After the credit memo is issued, [!DNL Channel Manager] updates the order status to *[!UICONTROL Refunded]*, or *[!UICONTROL Partially refunded]* if only some order items were returned.

* [!DNL Channel Manager] sends a refund update to Walmart marketplace so the RMA status can be updated to reflect the completed refund from Adobe Commerce.

In the storefront Admin, you can view and process returns from Channel Manager by opening the sales channel store and selecting **[!UICONTROL Returns].

![Channel Manager Returns dashboard to process refunds for RMA requests received from [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>You can only process refunds for shipped orders. In [!DNL Channel Manager], the order status must be [!UICONTROL Shipped]. In [!DNL Walmart Marketplace] Seller account, the order must be [!UICONTROL Delivered].

## Returns Controls and Column Descriptions

The following tables describe the controls and columns available for [!DNL Channel Manager] returns.

**Controls for [!UICONTROL Returns]**

<table>
<tr>
<td>**Control**</td>
<td>**Description**</td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filter the view by selecting one of the [!UICONTROL Return Status] cards.</td>
</tr>
<tr>
<td>Status Details</td>
<td>For RMA entries with the [!UICONTROL Received] or [!UICONTROL Refunded] status, you can create or view the credit memo for the refund by selecting the linked text in the Status Details column.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>To view order details, select the [!DNL Commerce] order number in the [!UICONTROL Order] table. Then, use [!DNL Commerce] order options to process the order.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>To modify the channel configuration, select channel Walmart Connection credentials, mapped attributes, or shipping identifiers, settings  select the [!DNL Commerce] order number in the [!UICONTROL Order] table. Then, use [!DNL Commerce] order options to process the order.</td>
</tr>
</table>

**Column descriptions**

<table>
<tr>
<td>Field</td>
<td>Description</td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>The Return Request Authorization number received from [!DNL Walmart Marketplace]. The number is generated during the marketplace [return processing](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&article=000007176f).</td>
</tr>
<tr>
<td>[!DNL Commerce] Order #</td>
<td>The [!DNL Commerce] order number associated with the items included in the return request from Walmart Marketplace. View order details by selecting the order number.</td>
</tr>
<tr>
<td>Requested</td>
<td>The date the return was requested on the [!DNL Walmart Marketplace]
converted to local time.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>The date that the return must be refunded by to meet [!DNL Walmart Marketplace] [requirements](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&article=000007176f) converted to local time.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Lists the SKU and description for each item listed in the RMA.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>The total value of the returned item.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indicates the current RMA status in the [!DNL Commerce] return workflow–*Received*, *Refunded*, or *Error*.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>For received and refunded RMA entries, status details provide a link to access the credit memo for refund processing. If an error occurs during the [!DNL Channel Manager] synchronization process between Adobe Commerce and [!DNL Walmart marketplace], this field provides the error description.</td>
</tr>
</table>

## Return Status

[!UICONTROL Order Status] provides information about the current state of [!DNL Walmart Marketplace] return requests managed from Adobe Commerce or Magento Open Source. Return status updates occur when [!DNL Channel Manager] receives an RMA request from the [!DNL Walmart Marketplace] or when the [!DNL Commerce] credit memo is created to process the refund for the returned items. Returns can have the following statuses:           

* **[!UICONTROL Received]**–This the initial status of the RMA received from the [!DNL Walmart Marketplace] store. The merchant can process the refund for the RMA by selecting **[!UICONTROL Create credit memo]** in the [!UICONTROL Status details].

* **[!UICONTROL Refunded]**—Indicates that a credit memo has been created to process the refund for the returned items. Merchant can view refund information by selecting **[!UICONTROL View credit memo]** in the [!UICONTROL Status details].

* **[!UICONTROL Error]**—RMA requests that have errors. Errors can occur when the RMA request from Walmart has missing or incorrect data. Or, if [!DNL Channel Manager] cannot send the refund update notification to Walmart.

>[!NOTE]
>
> It can take up to five minutes for refund updates to synchronize to [!DNL Walmart Marketplace]. You can check the current RMA status from the [!DNL Channel Manager] Returns dashboard.

## Process a refund request

1. Open the Returns dashboard for your sales channel store.

   * From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Open the store view by selecting the eye icon for a sales channel store.

   * Select **[!UICONTROL Returns]**.

1. Find an RMA to process.

   * From the Returns table, find an RMA with the *[!UICONTROL received]* status.

1. From the items column, review the list of order items to refund.
 
1. Process the refund by issuing a credit memo.

   * From the [!UICONTROL Status Details] column, select **[!UICONTROL Create credit memo]**.

     If the order has not been invoiced, an error displays prompting you to [create the invoice](https://docs.magento.com/user-guide/sales/invoices.html). After you create the invoice, select **[!UICONTROL Credit Memo]**.

   * In [!UICONTROL Items to Refund] section of the [!UICONTROL Credit Memo], update the **[!UICONTROL Qty to refund]** and **[!UICONTROL Return to Stock]** information for the items included in the RMA request.
  
     Make sure that you return only the items listed in the RMA request.

   * To add a comment, enter the text in the **[!UICONTROL Credit Memo Comments]** 

   * Select **[!UICONTROL Refund Offline]**.

After completing the refund, [!DNL Channel Manager] updates the RMA status in the [!UICONTROL Returns] dashboard to *[!UICONTROL Refunded] and synchronizes updated status to Walmart to update the RMA status in marketplace.


## View refund information for an RMA

You can view information about return requests and refund processing from the [!DNL Returns] dashboard.

1. Open the Returns dashboard for your sales channel store.

   * From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Open the store view by selecting the eye icon for a sales channel store.

   * Select **[!UICONTROL Returns]**.

1. View refunded orders by selecting the **[!UICONTROL Refunded]** status card.

1. View refund details for an RMA by selecting **[!UICONTROL View credit memo]**.

   ![Commerce Order detail view for a[!DNL Walmart Marketplace]order](assets/order-detail-with-external-order-id.png)

## Cancel an order

1. From the Admin, select **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Open the store view by selecting the eye icon for a sale channel store.

1. To view [!DNL Walmart Marketplace] orders, select *[!UICONTROL *Orders]**.

1. In the Orders table, open the [order detail page](manage-orders.md#view-order-detail) by selecting the **Commerce Order Number** for the order to cancel.

   ![Commerce Order detail view for a[!DNL Walmart Marketplace]order](assets/order-detail-with-external-order-id.png)

1. Cancel the order.

   * Select **Cancel** from the Order Detail menu.

   * On the [!UICONTROL Cancel Order] form, select the **Cancellation reason**.

   ![Commerce Order detail view for a [!DNL Walmart Marketplace] order](assets/cancel-order-reason-selector.png)

   * Select **Cancel Order**.

1. After submitting the cancellation, track the [order status](manage-orders.md#about-order-status) in [!DNL Channel Manager] to verify that updates were sent to [!DNL Walmart Marketplace].

## Fix return errors

Errors can occur during the RMA synchronization process from [!DNL Walmart Marketplace], or when [!DNL Channel Manager] synchronizes status updates from [!DNL Commerce] to u[!DNL Walmart Marketplace].

If the synchronization operation for an RMA update fails, the [!DNL Channel Manager] Returns dashboard shows an _Error_ status for the RMA entry. To ensure that RMA and refund information is accurately reflected in Walmart Marketplace account, manually update the order in your [!DNL Walmart Marketplace] store.



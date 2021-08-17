---
title: Amazon Order Details
description: View details for your Amazon Marketplace orders in the Adobe Commerce or Magento Open Source Admin.
---

# Amazon order details

![](assets/amazon-order-details-header.png)
_Amazon order details_

## View Amazon order details

1. Click **View Store** on the store card.

1. In the _Recent Orders_ section, click an order number.

    The _Amazon Order Details_ page opens.

>[!NOTE]
>
>If you have order import enabled in your [Order Settings](./order-settings.md) and the order is [fulfilled by Amazon (FBA)](./fulfilled-by.md), you may see dummy data for some fields in the order details. Amazon does not send the following data for FBA orders.
>
> - AddressType
> - AddressLine1
> - AddressLine2
> - AddressLine3
> - BuyerName
> - Phone
> - PurchaseOrderNumber
> - RecipientName
> - CustomizedURL
> - GiftMessageText

### Order and Shipping Details tab

The _Order and Shipping Details_ tab shows detailed order information, as received from Amazon.

>[!IMPORTANT]
>
>Amazon accepts non-standard address information that cannot be imported into [!DNL Amazon Sales Channel], thus preventing the state/country codes from updating correctly for some orders. To correct address errors, the following fields are editable in the order details:
>
>- Shipping address 1
>- Shipping address 2
>- Shipping address 3
>- Shipping city
>- Shipping region
>- Shipping postal code
>- Shipping country
>
>Do not forget to click **Save Order** after making edits.

![](assets/amazon-order-details.png)
_Order and Shipping Details_

### Order Items tab

The _Order Items_ tab shows all items associated with the Amazon order, as received from Amazon.

![](assets/amazon-order-item-details.png)
_Order Item Details_

### Tracking tab

The _Tracking_ tab shows tracking information associated with the Amazon order.

![](assets/amazon-order-tracking-details.png)
_Tracking Details_

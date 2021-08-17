---
title: Fulfilled By
description: Use the Fulfilled By settings to determine how the orders from Amazon listings will be fulfilled (shipped).
redirect_from:
  - /sales-channels/asc/ob-fulfilled-by.html
---

# Fulfilled By

_Fulfilled By_ settings are part of your store listing settings. Listing settings are accessed from the [store dashboard](./amazon-store-dashboard.md).

These settings define who fulfills (or ships) orders. If all of your orders are fulfilled using one method, choose between merchant (you) or Amazon. If you plan on fulfilling orders from your locations and using Amazon, we recommend using the third option and configuring a [!DNL Commerce] product attribute.

- **Fulfilled by Merchant** - Choose when you, the merchant, will fulfill all orders. When an order is placed, inventory will be deducted from your [!DNL Commerce] catalog.

- **Fulfilled by Amazon** - Choose when Amazon will fulfill all orders. When chosen, product inventory is not deducted from your [!DNL Commerce] catalog when an order is placed. Inventory stock for Amazon fulfilled orders is stored and deducted from their warehouses. Before assigning this option, you must verify in your [!DNL Amazon Seller Central] account that your products are eligible for FBA fulfillment. FBA inventory is directly managed through your [!DNL Amazon Seller Central] Account. With this fulfillment method, [!DNL Amazon Sales Channel] does not share quantity updates between [!DNL Commerce] and Amazon. Therefore, not all of the marketing tools described in the Quantity Settings will be available to you in [!DNL Amazon Sales Channel].

- **Assign Fulfilled By Using Magento Product Attribute** - If your products may be fulfilled by you and Amazon, you may want to create a [!DNL Commerce] product attribute with values for Fulfilled By Merchant and Fulfilled by Amazon. Setting this value per product indicates who fulfills the orders.

The fulfillment method is a regional attribute, and based on the **[!DNL Amazon Marketplace] Country** setting defined during [store integration](./store-integration.md). When a change is made, the change will affect all Amazon listings that share that [!DNL Amazon Seller SKU] in your Amazon stores that sell in the same region (as defined in **[!DNL Amazon Marketplace] Country** during [store integration](./store-integration.md)). This means that a change to a shared [!DNL Amazon Seller SKU] in the United States will not affect your Amazon stores with a region set for a different region (as defined during the store integration).

>[!NOTE]
>
>When an order is is fulfilled by Amazon (FBA) and the order is imported, you may see dummy data for some fields in the order details. See [Amazon Order Details](./amazon-order-details.md).

## Configure the Fulfilled By settings {#configure-fulfilled-by-settings}

1. Click **Listing Settings** on the store dashboard.

1. Expand the _Fulfilled By_ section.

1. For **Product Fulfilled By**, choose who fulfills (ships) the order:

   - **Fulfilled by Merchant** - Merchant fulfills order.

   - **Fulfilled by Amazon** - Amazon warehouse fulfills order.

   - **Assign Fulfilled By Using Magento Product Attribute** - A [!DNL Commerce] attribute indicates who fulfills the order per product.

      If chosen, choose the [!DNL Commerce] attribute you want to map in **Fulfilled by Attribute**.

1. When complete, click **Save listing settings**.

![](assets/amazon-fulfilled-by.png)
_Fulfilled By_

|Field|Description|
|--- |--- |
|Product Fulfilled By|Options:<ul><li>**Fulfilled by Merchant** - (FBM) Choose if you fulfill the orders. When an order is placed, inventory will be deducted from your [!DNL Commerce] catalog. When a new product is created, the fulfillment method of Merchant Fulfilled will be assigned.</li><li>**Fulfilled by Amazon** - (FBA) Choose if Amazon fulfills the orders. With this fulfillment method, product inventory will not be deducted from your Commerce catalog when an order is placed. When a new product is created it will be created with Fulfilled by Amazon (FBA) as the fulfillment type. You must ensure that your products are eligible for FBA fulfillment within your [!DNL Amazon Seller Central] account. FBA inventory is also directly managed through your [!DNL Amazon Seller Central] account. With this fulfillment method quantity updates are not pushed out relative to your [!DNL Commerce] catalog, so you will be unable to use some of the marketing tools described in [Stock / Quantity Settings](./stock-quantity.md).</li><li>**Assign Fulfilled By Using Magento Product Attribute** - Choose if you have an existing [!DNL Commerce] attribute that determines if it is fulfilled by the merchant or fulfilled by Amazon. When chosen, **Fulfilled by Attribute** enables. |
|Fulfilled By Attribute|Choose the [!DNL Commerce] attribute used to determine the fulfillment method.</li></ul><br><br>For example, if the attribute is _Fulfilled By_ and you choose the respective attribute value to define if it is _Fulfilled By Merchant_ or _Fulfilled By Amazon (FBA)_, when a new product is created it will be created with the defined attribute as the fulfillment type. As a merchant, you will need to ensure that your products are eligible for FBA fulfillment within your [!DNL Amazon Seller Central] account. FBA inventory is also directly managed through your Amazon Seller Account.<br><br>Options depend on the attributes you set up for your Amazon products. |

**Quick Access** - Listing Settings sections

- [Product Listing Actions](./product-listing-actions.md)
- [Third Party Listings](./third-party-listing-settings.md)
- [Listing Price](./listing-price.md)
- [(B2B) Business Price](./business-pricing.md)
- [Stock / Quantity](./stock-quantity.md)
- [Fulfilled By](./fulfilled-by.md)
- [Catalog Search](./catalog-search.md)
- [Product Listing Condition](./product-listing-condition.md)

---
title: Inventory and Price Updates
description: "[!DNL Channel Manager] syncs inventory and price updates between the Commerce store and [!DNL Walmart Marketplace] so you can manage your sales channel operations from your Commerce Admin"
---

# Inventory and Price Updates

[!DNL Channel Manager] tracks inventory and pricing for products in the channel store. When inventory or pricing changes, updates sync to both [!DNL Channel Manager] and [!DNL Walmart Marketplace] to reflect current stock quantity and pricing in product listings.

## Inventory updates

When inventory levels change, Channel Manager syncs updates between the Commerce and Walmart Marketplace to ensure that Channel Manager and the Walmart Marketplace have the correct stock quantity. 

It can take up to 10 minutes for inventory updates to sync across Channel Manager and the marketplace.

* **Updates to stock quantity in product catalog**–If the Commerce stock quantity changes for a product selling on Walmart because of a [manual stock quantity change](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) or an order refund or cancellation, Channel Manager syncs the change to the connected sales channel and the [!DNL Walmart Marketplace].

* **Reduce stock quantity to reflect Walmart Marketplace orders**–After a Walmart Marketplace order syncs to Channel Manager, Channel Manager sends the update to the Commerce order system. Commerce adjusts stock quantities based on the order. Then, the updated quantity is synced to Walmart Marketplace. Until the sync operations complete, you might see qunatity differences between Channel Manager and the Marketplace.

>[!IMPORTANT]
>
> After a Walmart Marketplace order syncs to Channel Manager, inventory quantities and other order information is updated only for refunds and cancellations initiated from Commerce. If an order is refunded or canceled from the Walmart Marketplace, process the change from Commerce to ensure the accuracy of Commerce inventory quantities and order information.

## Price updates

When the product price changes in Commerce, Channel Manager syncs the update from the [!DNL Commerce] product catalog to [!DNL Walmart Marketplace]. It can take up to 5 minutes for price changes to display.

### Manage pricing for a published product

1. From the [!UICONTROL Admin], select **[!UICONTROL Catalog > Products]**.
1. In the product grid, find the product to update and select **[!UICONTROL Edit]**.
1. Review and update the price as needed.
1. **[!UICONTROL Save]** the change.

For details about manage product price configuration in Commerce, see [Manage Pricing](https://docs.magento.com/user-guide/catalog/pricing.html){target="_blank"}.

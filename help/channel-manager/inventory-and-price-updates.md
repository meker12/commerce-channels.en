---
title: Inventory and Price Updates
description: "[!DNL Channel Manager] syncs inventory and price updates between the Commerce store and [!DNL Walmart Marketplace] so you can manage your sales channel operations from your Commerce Admin"
---

# Inventory and Price Updates

Channel Manager tracks inventory and pricing for published products and syncs changes to Channel Manager and the Walmart Marketplace to reflect current stock quantity and pricing in product listings.**

## Inventory updates

When inventory levels change, Channel Manager syncs updates between the Commerce product catalog and the Walmart Marketplace so that both Channel Manager and the Walmart Marketplace display the current stock quantity. 

It can take up to 5 minutes for inventory changes to display in Channel Manager and Walmart Marketplace.

* **Updates to stock quantity in product catalog**–If the Commerce stock quantity changes for a product selling on Walmart because of a [manual stock quantity change](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) or an order refund or cancellation, Channel Manager syncs the change to the connected sales channel and the [!DNL Walmart Marketplace].

* **Reduce stock quantity to reflect Walmart Marketplace orders**–After a Walmart Marketplace order syncs to Channel Manager, Channel Manager sends the update to the Commerce order system. Commerce adjusts stock quantities based on the order. Then, the updated quantity is synced to Walmart Marketplace. might be some differences in stock quantity shown in Channel Manager and the Marketplace until the sync operations complete. 
    
>[!IMPORTANT]
>
> After a Walmart Marketplace order syncs to Channel Manager, inventory quantities and other order processing information is updated only for refunds and cancellations initiated from Commerce. If an order is refunded or canceled from the Walmart Marketplace, process the change from Commerce to make sure that Commerce inventory quantities and order information are accurate.

## Price updates

When the product price changes in Commerce, Channel Manager syncs the update from the Commerce product catalog to Walmart Marketplace. It can take up to 5 minutes for inventory changes to display.

### Manage pricing for a published product

1. From the [!UICONTROL Admin], select **[!UICONTROL Catalog > Products]**.
1. In the product grid, find the product to update and select **[!UICONTROL Edit]**.
1. Review and update the price as needed.
1. **[!UICONTROL Save]** the change.

Channel Manager syncs any price updates to the channel store and [!DNL Walmart Marketplace]. This operation can take up to 5 minutes.

For details about manage product price configuration in Commerce, see [Manage Pricing](https://docs.magento.com/user-guide/catalog/pricing.html){target="_blank"}.

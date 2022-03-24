---
title: Add Products to Channel Store
description: Create product assortment for Marketplace sales by adding products from the catalog to the sales channel
---

# Add Products to Channel Store


From Channel Manager, select products from the [!DNL Commerce] catalog for Walmart Marketplace sales.

To sync products to the sales channel, the selected products must have the following attribute configuration:

- **[!UICONTROL Publish to Channel Manager]** attribute is enabled

- At least one product attribute must match one of the [required Walmart Marketplace attributes](map-product-attributes-for-matching.md)–GTIN, ISBN, ISSN, UPC, EAN

After you save selections, the Channel Manager imports the product data the channel. This process can take up to 30 minutes.

## Add products to sales channel

1. Open the product catalog associated with your Channel Manager store.

   From a connected sales channel store, select **Add products**.
   
   ![Add products to connected channel](assets/add-initial-products-to-connected-channel.png)

   The catalog opens in a new tab.

1. From the catalog product grid, select products to sell on Walmart Marketplace.

   ![Send products to the connected channel](assets/select-products-from-catalog.png)

1. Enable the **[!UICONTROL Publish to Channel Manager]** attribute for the selected items.

   - From **[!UICONTROL Actions]**, select **[!UICONTROL Update attributes]**.

   - Scroll to the **[!UICONTROL Publish to Channel Manager]** attribute and enable it.

   - Verify that the product attributes include at least one of the required Walmart Product IDs.

   - Select **[!UICONTROL Save]**.

    A confirmation message displays.

     ![Product import from catalog to sales channel confirmation message](assets/product-import-from-catalog-confirmation.png)

     If the message indicates that the update is scheduled, use the [queue:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] command to process the update immediately.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ``` 
  
1. Return to the connected sales channel in [!DNL Channel Manager].

   After the import operation completes, view products from **[!UICONTROL Listings]**. Initially, the products are in *Draft* status. Select [!UICONTROL Refresh products]** to update the table.  

   ![Products imported to connected sales channel](assets/products-in-marketplace-sales-channel.png)

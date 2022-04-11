---
title: Manage Listings
description: Manage sales channel listings for a [!DNL Commerce] store with Channel Manager for Adobe Commerce and Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
---
# Manage Listings

Manage product listings for a connected channel from [!UICONTROL Listings] in the channel store view.

Use the *[!UICONTROL Listings]* workspace to manage the [!DNL Commerce] products offered for sale on Walmart Marketplace. The Status for an individual listing indicates where the product is in the [!DNL Channel Manager] workflow so you can determine next steps and resolve any errors.

![Listings page for a connected sales channel](assets/products-submit-for-matching.png)

## View listings

1. From the Admin, go to [!UICONTROL **Marketing** > Channels > **Channel Manager**].

1. From the Channel Store list, select the pencil icon in a store entry row to open the store view.

1. Select [!UICONTROL **Listings**].

## Add Commerce products to Channel Manager

Complete the following tasks to create the product assortment for the Walmart Marketplace channel:

* [Add products from your Commerce product catalog to Channel Manager](add-products-to-connected-channel.md)

* [Configure product matching](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## Publish products to Walmart

You can create product offers on the Walmart Marketplace using product matching or by manually uploading product listings for new products. For instructions, see [Publish Listings to Walmart Marketplace](publish-listings-to-marketplace.md) as described in the following topics:

* **[Match products on Walmart](publish-listings-to-marketplace.md)**–Publish product listings from your channel to [!DNL Walmart Marketplace] by updating existing listings selling the same product. Match criteria are determined by the [attribute mapping configuration](map-product-attributes-for-matching.md) for your channel.

* **[Manually upload new listings](publish-listings-to-marketplace.md#upload-new-product-listings)-**–For products that do not match an existing listing on Walmart Marketplace, use a Walmart product category Excel template to bulk upload product listings.

## Listing Controls and Column Descriptions

The following tables describe the controls and columns available for [!UICONTROL Listings].

**Controls for [!UICONTROL Listings]**

| **Control**                            | **Description**                                                                                                                                                                                              |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Refresh products]          | Updates the display with the most current listing and status.                                                                                                                                                |
| [!UICONTROL Add Products]              | Opens the [!UICONTROL Admin Product Catalog] page to select products to add to your [!DNL Walmart Marketplace] assortment, or to update product attributes to meet Walmart Marketplace listing requirements. |
| [!UICONTROL Match products on Walmart] | After selecting one or more products in Draft status, select Match products on Walmart to check for product offers that can be added to an existing [!DNL Walmart Marketplace] listing.                      |


**Column descriptions**

| **Field**                    | **Description**                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name]    | Name of the product from the [!DNL Commerce] store catalog.                                                                                                                                                                                                                                                                                                                                                           |
| [!UICONTROL SKU (Unique ID)] | The mapped attribute used to match products on the marketplace. This field name varies depending on the mapped attribute configuration for [!DNL Channel Manager] listings. In this case, the product matching operation uses the product SKU from the [!DNL Commerce] catalog to find a [!DNL Walmart Marketplace]  Listing with a SKU value that matches the SKU value from the [!DNL Commerce] product attributes. |
| [!UICONTROL  Quantity]       | Amount of inventory available in Adobe Commerce or Magento Open Source.                                                                                                                                                                                                                                                                                                                                               |
| [!UICONTROL Price]           | The product price from the [!DNL Commerce] store catalog. Catalog price updates are synced to Channel Manager, and then sent to [!DNL Walmart Marketplace]  so that listed items show the current price.                                                                                                                                                                                                              |
| [!UICONTROL Status]          | Indicates the current order status in the [!DNL Commerce] order workflow. The status updates when you successfully add products to [!DNL Channel Manager] and when you match products on the marketplace. If an operation fails, the listing shows an error status. After you fix the error, [!DNL Channel Manager] retries the operation and updates the status.                                                     |


### About Listing Status              

In the Listing workspace, the Status label shows where a product is in the [!DNL Channel Manager] workflow so you can determine next steps and resolve errors. Listings can have the following status labels:

*  **[!UICONTROL Draft]**–Identifies products that have not been [submitted to [!DNL Walmart] for matching](publish-listings-to-marketplace.md#match-products).

*  **[!UICONTROL Processing]**–Identifies products submitted for matching on the [!DNL Walmart Marketplace]. Products remain in *Processing* status until the [!DNL Walmart] returns an HTTP status message that indicates whether the match was successful, or if there was an error. It can take up to 30 minutes for the match operation to complete on the [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**–Identifies products that were matched successfully on [!DNL Walmart].
    
    A match occurs when the product attribute value–UPC code for example–matches the UPC value in an existing[!DNL Walmart Marketplace] listing. When a product matches, the Commerce product offer is added to the existing Walmart listing.

    Check the [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) dashboard to review the updated product listing and verify product details, price, and inventory quantity.  


* **[!UICONTROL Error]**–Identifies products that were not matched to an existing [!DNL Walmart Marketplace] listing. View error details by hovering over the *Error* status label.

  After you resolve the error, resubmit the product for matching. See [Troubleshoot product match errors](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]**–Identifies products matched on [!DNL Walmart] that cannot be published until the [!DNL Walmart Marketplace] store is live. Products with this status publish automatically when the [!DNL Walmart Marketplace] store goes live.

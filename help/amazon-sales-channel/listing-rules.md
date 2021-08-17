---
title: Listing Rules
description: Use listing rules determine the Commerce catalog products that are published as Amazon Marketplace listings.
redirect_from:
  - /sales-channels/asc/ob-listing-rules.html
  - /sales-channels/asc/ob-listing-preview.html
  - /sales-channels/asc/listing-rule-preview.html
---

# Listing rules

You can access the listing rules for store in the [store dashboard](./amazon-store-dashboard.md).

Listing rules define the rules to determine which products [!DNL Amazon Sales Channel] will publish to Amazon. These rules provide many options to create simple to complex rules to include or exclude products as listings. Each rule consists of conditions that set the requirements for product listing eligibility.

Your listing rules are continually synchronized with your [!DNL Commerce] catalog. When you add new [!DNL Commerce] products that meet eligibility requirements set by your listing rules, the products will automatically process for listing on Amazon.

- If you want all of your products to be published to an Amazon listing, do not define any conditions for your listing rules.

- If you want to limit which of your catalog products that will be published to Amazon, you will define your listing rule conditions. Defining the conditions for your Amazon listing rules follow the same logic and process as defining the conditions for [Cart Price Rules](https://docs.magento.com/user-guide/marketing/price-rules-cart.html).

- If your listing rules exclude a product, the eligibility status for that product changes to `Ineligible`. Ineligible products will not be published to Amazon.

- If an ineligible product is already listed on Amazon and you match the Amazon listing to your [!DNL Commerce] catalog product, the quantity for the Amazon listing will change to `0` to prevent sales of the product. Amazon listings can be [manually removed](./end-listings-manually.md).

Changes to quantity and eligibility status impact all listings that share the Amazon Seller SKU in marketplaces that exist for stores selling in the same region (as defined in **[!DNL Amazon Marketplace] Country** during [store integration](./store-integration.md)). However, a change to a shared [!DNL Amazon Seller SKU] in one region will not affect the product's Amazon listings in a different country.

![](assets/ob-listing-rules.png)
_Listing Rules_

## Configure Listing Rules settings

1. Click **Listing Rules** on the store dashboard.

1. Define your desired conditions for the eligibility of products to be listed on Amazon.

See [Example: Define a Condition](./ob-define-condition-example.md).

|Field|Description|
|---|---|
|Websites|The available options depend on the [websites](https://docs.magento.com/user-guide/stores/websites-stores-views.html) you have set up in your [!DNL Commerce] configuration. Select the website to represent which website to have eligible products listed on Amazon. Only one website can be selected, as each website requires a unique Amazon store created in [!DNL Amazon Sales Channel]. |
|Conditions|Used to define the [!DNL Commerce] attributes for product eligibility within your Amazon region. See [Example: Define a Condition](./ob-define-condition-example.md). |

## Conditions workspace

Any areas in the conditions that are bold can be clicked to see the various options.

- Do not add conditions if all products within the selected website(s) are eligible.
- There is a complex set of back-end processes to communicate with Amazon's systems directly. Based on the number of items you are attempting to list, and how busy Amazon's systems might be (for example, Black Friday can be a slow time to list new products), it may take time for your items to be listed on Amazon.

For more information about conditions, see [Describe the Conditions](https://docs.magento.com/user-guide/marketing/price-rules-cart.html).

## Listing rule preview

When you are modifying your condition definitions for your listing rules, you can click **Preview Changes** to apply your rules changes and view how your listings are impacted. You should verify your listings in this listing preview feature before saving your listing rule changes.

Your Amazon listings are compared against your rules and defined conditions. You can then review which products will move to an ineligible status based on your current [!DNL Amazon Seller Central] account, which products will move from an ineligible state back to eligible status and which products will be New Amazon Listings and added to your Amazon listing from your eligible [!DNL Commerce] products.

Listing Preview allows you to preview your potential Amazon listings and make any necessary adjustments to your listing rules.

Your potential Amazon listings will populate on the _Listing Preview_ page in one of three tabs:

- **Ineligible Listings** - Products listed are not eligible for Amazon listing based on your current listing rules and conditions.

   Ineligible products will not be published to Amazon. If an ineligible product is already listed on Amazon and you match the Amazon listing to your [!DNL Commerce] catalog product, the quantity for the Amazon listing will change to `0` to prevent sales of the product. To manually remove a listing, see [Ending an Amazon Listing](./end-listings-manually.md). Products that are not eligible by Amazon requirements are not listed here. Those products are listed on the [Inactive Listings tab](./inactive-listings.md).

- **Eligible Listings** - Products listed are eligible for Amazon listing based on your current listing rules and conditions and are also eligible by Amazon requirements. This list includes your existing Amazon listings that will import (if you have **Import Third Party Listings** set to `Import Listing` in [Listing Settings](./third-party-listing-settings.md)).

- **New Listings** - Products listed include your [!DNL Commerce] catalog products that are newly eligible for Amazon listing based on your current listing rules and conditions and will create and publish new Amazon listings.

### View your listing preview

1. Click **Listing Rules** on the store dashboard.

1. View or add your [listing rules](./listing-rules.md).

1. Modify your [Listing Rule Conditions](./ob-define-condition-example.md).

1. Click **Preview Changes**.

1. Review and confirm your listings in the _Ineligible Listings_, _Eligible Listings_, and _New Listings_ tabs.

1. If your listings match your expectations, click **Save and close**.

    If your listings do no not appear as expected, click **Back** and modify your rules and conditions until your listings match your expectations.

![](assets/amazon-listing-rule-preview.png)
_Listing Rule Preview_

### Listing preview workflow

|Field|Description|
|--- |--- |
|Product ID |The unique, sequential number that is assigned to a [!DNL Commerce] catalog product when it is added. |
|Thumbnail |Shows a thumbnail of the main product image. |
|Name |The name of the product, managed in the [!DNL Commerce] [products grid](https://docs.magento.com/user-guide/catalog/products.html). |
|Type |The type of product, managed in the [!DNL Commerce] products grid. |
|Attribute Set |The name of the attribute set used as a template for the product, managed in the [!DNL Commerce] products grid. |
|SKU |The unique Stock Keeping Unit that is assigned to the product, managed in the [!DNL Commerce] products grid. |
|Visibility |Indicates where the product is visible, managed in the [!DNL Commerce] products grid. Options:<ul><li>Not visible individually</li><li>Catalog</li><li>Search</li><li>Catalog, Search</li></ul>|
|Status |Indicates the current status of the product, managed in the [!DNL Commerce] products grid. Options:<ul><li>Enabled</li><li>Disabled</li></ul> |

![](assets/listing-preview-flowchart.png)
_Listing Preview Workflow_

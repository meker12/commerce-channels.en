---
title: About [!DNL Channel Manager]
description: Learn how to install and use [!DNL Channel Manager] to integrate Adobe Commerce and Magento Open Source stores with third-party marketplaces and create a sales channel to manage Marketplace listings, pricing, inventory, and sales seamlessly from your Commerce Admin.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
---

# About [!DNL Channel Manager]

Channel Manager for Adobe Commerce and Magento Open Source provides a convenient workspace in the Admin to manage channel sales on third-party marketplaces like Walmart, Amazon, and eBay. Increase sales and expand to new markets while managing sales channel operations seamlessly from your Commerce Admin.

![[!DNL Channel Manager] extension Admin view](assets/channel-manager-admin-entry-page.png)

## Beta release overview

The Beta release of Channel Manager supports Adobe Commerce or Magento Open Source sellers who want to sell on [!DNL Walmart Marketplace].

This release supports the following capabilities to manage sales channel operations:

* Establish an API connection between Adobe Commerce or Magento Open Source and Walmart Marketplace

* Publish products from Channel Manager to Walmart using product matching

* Manage product listings and track status

* Sync inventory quantities for matched products from Commerce to Walmart

* Sync catalog pricing for matched products from Commerce to Walmart

* Receive orders from Walmart Marketplace and view them in the [!DNL Commerce] order dashboard
      
### Expected latency for Channel Manager operations

The data synchronization processes between [!DNL Channel Manager] and a linked [!DNL Walmart Marketplace] store require some time to complete. Review the expected processing time for [!DNL Channel Manager] operations to help plan sales channel operations work.

**Estimated latency for Channel Manager operations**

| **Operation**                              | **Description**                                                                                                                               | **Expected delay**                                                                                                        |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Add products to Channel Manager            | Select products from the Commerce product catalog and import them into Channel Manager.                                                       | **Up to 5 minutes**–If you select many products, for example, an entire product catalog, the import process takes longer. |
| Match products on Walmart Marketplace      | Select product listings in Channel Manager and send to Walmart for matching.                                                                  | **Up to 30 minutes**–If you select many products, the matching process takes longer depending on the quantity selected.   |
| Inventory updates                          | When inventory quantity changes in Commerce, [!DNL Channel Manager] syncs update to Walmart.                                                  | **Up to 10 minutes**                                                                                                      |
| Price updates                              | When a product price changes, Channel Manager syncs the update to Walmart.                                                                    | **Up to 5 minutes**                                                                                                       |
| Order syncs from Walmart to Commerce       | Customer orders a Commerce product on the Walmart Marketplace. Walmart sends the order to Channel Manager. Order displays in order dashboard. | **Up to 30 minutes**                                                                                                      |
| Order created in Commerce Order Management | Channel Manager creates the Commerce order from the Walmart order and updates the order dashboard to include the Commerce order number.       | **Up to 5 minutes**                                                                                                       |

## Walmart prerequisites

You need the following information from Walmart to integrate Commerce with the Walmart Marketplace:

* Approval to sell on Walmart and credentials to log in to the registered Marketplace Seller account

* An API key to connect Adobe Commerce or Magento Open Source to Walmart Marketplace

  The Walmart Marketplace API key enables the integration between Channel Manager for Adobe Commerce or Magento Open Source and the Walmart Marketplace. Set up the API key in Seller Central before starting the Channel Manager onboarding process.

### Set up a Marketplace Seller account

1. [Submit your Walmart Seller application](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
2. After obtaining approval from Walmart, [set up your Walmart Seller account](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Generate a Walmart Marketplace API key

1. Go to Walmart Marketplace to generate a [solution provider production API key for Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Create the key and configure permissions:

   * Select Adobe as the solution provider.
   
   * Set the permissions as shown in the following table. For details, see [API Credentials](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) in the *[!DNL Walmart Marketplace] Seller Help*.

    **Adobe API key configuration for Walmart**

    | **Permission** | **Setting** |
    |----------------|-------------|
    | Content        | Full Access |
    | Get Feeds      | View Only   |
    | Inventory      | Full Access |
    | Items          | Full Access |
    | Lag Time       | Full Access |
    | Order          | Full Access |
    | Price          | Full Access |
    | Reports        | View Only   |
    | Returns        | Full Access |
    | Rules          | Full Access |
    | Shipping       | Full Access |

## Walmart Marketplace Store status

When you publish products to Walmart Marketplace, listing availability depends on the status of your Walmart Marketplace stores:

* For live stores, your product offers are listed and available for sale when the match operation completes. 

* For stores that are not live, your product offers are staged and not visible to customers. When the store goes live, staged listings are pushed to the live store automatically. 


![[!DNL Walmart Seller Central] staged products](assets/walmart-seller-central-staged.png)

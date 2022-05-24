---
title: About [!DNL Channel Manager]
description: Learn how to install and use [!DNL Channel Manager] to integrate Adobe Commerce and Magento Open Source stores with third-party marketplaces and create a sales channel to manage Marketplace listings, pricing, inventory, and sales seamlessly from your Commerce Admin.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
---

# About [!DNL Channel Manager]

[!DNL Channel Manager] helps you increase sales and reach new customers by integrating your Adobe Commerce or Magento Open Source product catalog with the [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] extension Admin view](assets/channel-manager-home.png)

Channel Manager supports Adobe Commerce or Magento Open Source sellers who want to sell on Walmart Marketplace.

After you install and configure [!DNL Channel Manager], the [!DNL Commerce] Admin is extended so you can manage [!DNL Walmart Marketplace] sales operations seamlessly from your Commerce environment.

* **Listing management**–Easily publish product listings by matching products from your Commerce catalog to existing Walmart Marketplace listings.

* **Inventory management**–Items in the merchant’s marketplace seller account are automatically synchronized and updated from Commerce to ensure accurate inventory levels.

* **Pricing updates**–Maintain accurate pricing for marketplace listings with automatic price synchronization. When a price changes in Adobe Commerce, the changes are reflected in the marketplace within 10 minutes.

* **Order management**–When new orders are created in a marketplace, Channel Manager synchronizes orders with Adobe Commerce and sends order acknowledgments to the marketplace to ensure inventory is reserved for each order.

* **Shipping management**–When orders are marked as shipped in Adobe Commerce, the shipment update is sent to the [!DNL Walmart Marketplace]. This notification ensures that sellers meet their fulfillment SLA requirements and that customers receive shipping update notifications for their current orders.

* **Cancellations**–When orders are canceled in Adobe Commerce, Channel Manager sends updated order information to the marketplace to replicate the action for the corresponding marketplace order.

## Expected latency for Channel Manager operations

The data synchronization processes between [!DNL Channel Manager] and a linked [!DNL Walmart Marketplace] store require some time to complete. Review the expected processing time for [!DNL Channel Manager] operations to help plan sales channel operations work.

**Estimated latency for Channel Manager operations**

| **Operation**                              | **Description**                                                                                                                               | **Expected delay**                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Add products to Channel Manager            | Select products from the Commerce product catalog and import them into Channel Manager.                                                       | **Up to five minutes**–If you select many products, for example, an entire product catalog, the import process takes longer. |
| Match products on Walmart Marketplace      | Select product listings in Channel Manager and send to Walmart for matching.                                                                  | **Up to 30 minutes**–If you select many products, the matching process takes longer depending on the quantity selected.      |
| Inventory updates                          | When inventory quantity changes in Commerce, [!DNL Channel Manager] syncs the update to Walmart.                                              | **Up to 10 minutes**                                                                                                         |
| Price updates                              | When a product price changes, Channel Manager syncs the update to Walmart.                                                                    | **Up to five minutes**                                                                                                       |
| Order syncs from Walmart to Commerce       | Customer orders a Commerce product on the Walmart Marketplace. Walmart sends the order to Channel Manager. Order displays in order dashboard. | **Up to 30 minutes**                                                                                                         |
| Order created in Commerce Order Management | Channel Manager creates the Commerce order from the Walmart order and updates the order dashboard to include the Commerce order number.       | **Up to five minutes**                                                                                                       |


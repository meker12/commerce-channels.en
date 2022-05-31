---
title: "Operations [!DNL Channel Manager]"
description: Find out about the backend operations of the Channel Manager including system architecture, source code packages and dependencies, and expected latency for Channel Manager operations like listing products, updating inventory and price, and order management
---

# Architectural overview [!DNL Channel Manager]

Channel Manager for Adobe Commerce service uses several SaaS services. The Store side includes your PWA storefront, which contains the event collector and recommendations layout template, and the backend, which includes the GraphQL endpoints, SaaS Export module, and the Admin UI.

After you install the Channel Manager extension on your store, it will start sending behavioral data to Adobe Sensei with no additional setup. Adobe Sensei processes this behavioral data along with the catalog data from the backend and calculates the product associations leveraged by the recommendations service. At this point, the merchant can create and manage recommendation units from the Adobe Commerce Admin UI then fetch those product recommendation units from their PWA storefront.


[!DNL Channel Manager] is distributed  Adobe Commerce extension of standalone packages for Adobe Commerce that replaces the standard search capabilities. The [!DNL Live Search] module is installed from the command line of the server and connects to your Commerce installation as a [service](../landing/saas.md). When the process is complete, [!DNL Live Search] appears on the *Marketing* menu under *SEO & Search* in the [!DNL Commerce] *Admin*.

The Adobe Commerce side of the architecture includes hosting the search *Admin*, synchronizing catalog data, and running the query service. After [!DNL Live Search] is installed and configured, Adobe Commerce begins sharing search and catalog data with SaaS services. At this point, Admin users can set up, customize, and manage search facets, synonyms, and merchandising rules.

![Live Search architecture diagram](assets/architecture-diagram.svg)

Review the [prerequisites](onboard.md#prerequisites) and gather required information before you install Channel Manager.




# Channel Manager packages

The [!DNL Channel Manager] extension for Adobe Commerce and Magento Open Source is distributed as a Composer metapackage.





## [!DNL Live Search] packages {#packages}

| Package                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `module-sales-channels-extension`       | Allows merchants to configure their search settings for faceting, synonyms, query rules, etc., and provides access to a read-only GraphQL playground to test queries from the *Admin*.                                                                                                                                                                                                                                                                                                                   |
| `module-order-ingestion`                | Routes search requests from the storefront to the [!DNL Live Search] service and renders the results in the storefront. <br />- Category browse - Routes requests from the storefront [top navigation](https://docs.magento.com/user-guide/catalog/navigation-top.html) to the search service.<br />- Global search - Routes requests from the [quick search](https://docs.magento.com/user-guide/catalog/search-quick.html) box in the upper-right of the storefront to the [!DNL Live Search] service. |
| `module-live-search-storefront-popover` | A "search as you type" popover replaces the standard quick search and returns dynamic product suggestions and thumbnails of top search results.                                                                                                                                                                                                                                                                                                                                                          |


Sales Channels service

ext-json *
magento/framework *
magento/module-backend *
magento/module-saas-catalog ^101.1.0
magento/module-saas-inventory ^101.1.0
magento/module-services-id *
magento/module-store *
magento/services-connector *


Inventory Service

magento/framework >=102.0.2
magento/module-data-exporter 101.*
magento/module-inventory-data-exporter 101.*
magento/module-saas-common self.version
php ~7.1.3||~7.2.0||~7.3.0||~7.4.0||~8.1.0



## [!DNL Live Search] dependencies {#dependencies}

The following [!DNL Live Search] dependencies are captured by [!DNL Composer]:

| Dependency           | Description                                                                                                                                                                                                                                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Export modules       | The following modules collect and sync catalog data:<br />`saas-export`<br />`module-bundle-product-exporter`<br />`module-catalog-data-exporter`<br />`module-catalog-inventory-data-exporter`<br />`module-catalog-url-rewrite-data-exporter`<br />`module-configurable-product-data-exporter`<br />`module-data-exporter`<br />`module-parent-product-data-exporter` |
| `services-connector` | Required to configure your connection to Commerce Services.                                                                                                                                                                                                                                                                                                             |
| `module-services-id` | Required to configure your connection to Commerce Services.                                                                                                                                                                                                                                                                                                             |

to install 



com



Channel manager is distributed as a metapackage that contains the requirements to ins



## Checking the installed version

Before updating Channel Manager, check the currently installed version.

```bash
composer show magento/module-channel-manager | grep version
```


## Upgrade Channel Manager


## Uninstall Channel Manager

n

After you install the [!DNL Channel Manager] extension, 


Keep the Channel Manager extension up-to-date. 

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




### Uninstall



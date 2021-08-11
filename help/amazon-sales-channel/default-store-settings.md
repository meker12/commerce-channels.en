---
title: Default Store Settings
---

# Default store settings

After your store is connected and you've set up your first listing rule, the sync of data between Amazon and [!DNL Commerce] starts. There are several types of store settings that allow you to customize your store for your needs. Store settings are accessed on the store [dashboard](./amazon-store-dashboard.md).

Store settings include:

- [**Listing settings**](./listing-settings.md) - Control how your product catalog interacts with the [!DNL Amazon Marketplace].

- [**Order settings**](./order-settings.md) - Control how Amazon orders are managed.

- [**Listing rules**](./listing-rules.md) - Define which catalog products are eligible to be listed on Amazon.

- [**Pricing rules**](./pricing-products.md) - Define how the Amazon list price will be altered for qualified listings.

- **Store reports** - [Competitive price analysis](./competitive-price-analysis.md) and [listing improvements](./listing-improvements.md).
- **Logs** - [Listing changes](./listing-changes-log.md) and [communication errors](./communication-errors-log.md).

- [**Store integration settings**](./store-integration-settings.md) - Review email and [!DNL Amazon Sales Channel] store name settings in the [!DNL Commerce Admin].

## Some important default settings

|Setting|Default|Description|Location|
|--- |--- |--- |--- |
|**Import Amazon Orders**|`Enabled`|Creates corresponding [!DNL Commerce] orders when new orders are received from Amazon, allowing orders to be managed in the [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html) workflow. When `Disabled`, Amazon orders import order information for review, but orders must be managed in your [!DNL Amazon Seller Central] account.|[Order Settings](./order-settings.md)|
|**Customer Creation**|`No Customer Creation (guest)`|Customer data from Amazon orders is not imported into your [!DNL Commerce] database. Imported Amazon orders are processed as a guest checkout. If you want to build your [!DNL Commerce] customer database, you will want to change this setting to `Build New Customer Account`.|[Order Settings](./order-settings.md)|
|**Automatic List Action**|`Automatically List Eligible Products`|[!DNL Commerce] catalog products (that meet Amazon's eligibility requirements) to automatically publish to Amazon and create new Amazon Listings. If you want to manually review and publish your products, you'll want to change this setting to `Do Not Automatically List Eligible Products`. Products waiting for manual publish appear on the [_Ready to List_](./ready-to-list.md) tab.|[Product Listing Actions](./product-listing-actions.md)|
|**Magento Price Source**|`Price`|Defines the price source attribute used as the base for your Amazon listings. If you do not want to use the [!DNL Commerce] `Price` attribute as your base price to which your pricing rules are based, you will want to change this setting to a different attribute.|[Listing Price](./listing-price.md)|
|**Product Fulfilled By**|`Fulfilled by Merchant`|The merchant will fulfill all orders. If you use Fulfillment by Amazon or use a mix of fulfillment methods, you will want to change this.|[Fulfilled by](./listing-price.md)|
|**Listing Product Condition**|`New`|If all your products are the same condition, you can select one of the Amazon condition options to represent all of your products. If your catalog contains products in different conditions (New, Used, Refurbished, etc.), you must change this setting to **Assign Condition Using Product Attribute** and map your [!DNL Commerce] condition attributes to your Amazon listing conditions.|[Product Listing Condition](./product-listing-condition.md)|
|Listing Rules|none|Define the rules to determine which products [!DNL Amazon Sales Channel] will publish to Amazon. These rules provide many options to create simple to complex rules to include or exclude products as listings.|[Listing Rules](./listing-rules.md)|
|Pricing Rules|none|Define your Amazon listing price attribute different than the defined **Magento Price Source** in your [Listing Price](./listing-price.md). Create rules to adjust your listing price (up or down) against your **Magento Price Source** setting.|[Pricing Rules](./pricing-products.md)|

For more information, see [Store Settings](./ob-store-review.md).

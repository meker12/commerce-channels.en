---
title: Best Practices and Limitations for Amazon Sales Channel
description: Review the the best practices and limitations when using the Amazon Sales Channel for Adobe Commerce and Magento Open Source.
---

# Best practices and limitations for [!DNL Amazon Sales Channel]

Best practices include:

- [!DNL Amazon Sales Channel] can affect your Amazon listings by increasing or decreasing prices, synchronizing product information (including available stock), and adding, updating, and ending (deleting) listings. You should review your listings by status during your setup and adjust your settings ([listing settings](./listing-settings.md), [listing rules](./listing-rules.md), [pricing rules](./pricing-products.md), [overrides](./overrides.md), etc) before completing your store setup. These settings can also be modified after setup, as needed.

- [!DNL Amazon Sales Channel] can set your pricing rules to automatically adjust your listing price. Automated pricing safeguards include the [Floor Price](./floor-price.md) and [Optional Ceiling Price](./optional-ceiling-price.md) features of [Intelligent repricing rules](./intelligent-repricing-rules.md). Use of these safeguards helps ensure that your listing prices do not go below your cost or above a defined price.

- Data syncing between [!DNL Amazon Sales Channel] and Amazon is controlled by your [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target="_blank"} settings. Built-in throttling between [!DNL Commerce] and Amazon help to ensure smooth and efficient data transmission, but during high eCommerce traffic times (such as Black Friday), Amazon’s systems may take longer than usual to update. It is recommended to set your [!DNL Commerce] cron to run once every five minutes.

- [!DNL Amazon Sales Channel] imports your Amazon order information. To manage your Amazon orders in [!DNL Amazon Sales Channel], you must ensure that your [order settings](./order-settings.md) are defined to import and create a corresponding [!DNL Commerce] order for each Amazon order. If this is not defined, you will only be able to view your Amazon order information. All taxes for sales through Amazon are still managed and remitted via your [!DNL Amazon Seller Central] account. In some states, Amazon is required to automatically collect and remit taxes. For other states, sellers have the option of calculating taxes manually or automatically. See [Amazon: Tax Policies](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&language=en_US&ref=efph_200405820_cont_521){target="_blank"}. You may be required to log into your [!DNL Amazon Seller Central] account to view Amazon tax policy documentation.

- For UK regions, it is best  practice to enroll in the [Amazon VAT Calculation Service](https://services.amazon.co.uk/vat-calculation-service.html){target="_blank"} before onboarding [!DNL Amazon Sales Channel].

   
   >[!NOTE]
   >
   >It may take 10-14 days for Amazon to verify and activate your VAT Calculation Service account.

Limitations include:

- Bundle, gift card, and grouped product types that are part of your [!DNL Commerce] catalog are not supported by [!DNL Amazon Sales Channel] for listing to Amazon.

- [!DNL Amazon Sales Channel] cannot create a listing for a product that does not have an existing or previous Amazon listing. If a product does not already exist in [!DNL Amazon Seller Central] with an ASIN, it must be added in [!DNL Amazon Seller Central] so that Amazon can assign the product an ASIN. After a product is added in Amazon and a listing is created, the listing can be matched to your catalog in [!DNL Amazon Sales Channel] and synced.

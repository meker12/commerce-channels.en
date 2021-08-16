---
title: Onboard Amazon Sales Channel
redirect_from:
  - /sales-channels/amazon/amazon-onboarding-home.html
---

# Onboard Amazon Sales Channel

This section describes the pre-setup tasks, steps for onboarding, and some key concepts of how Amazon works with the [!DNL Amazon Sales Channel] in Adobe Commerce and Magento Open Source.

[!DNL Amazon Sales Channel] supports multiple [!DNL Amazon Sales Channel] stores. For a single [!DNL Amazon Seller Central] account that operates in the Amazon region that includes U.S./Canada/Mexico, you will create three [!DNL Amazon Sales Channel] stores (one for U.S. sales, one for Mexico sales, and one for Canada sales). Each of the three stores will define the marketplace country during its creation. If you have more than one [!DNL Amazon Seller Central] account, you could potentially have up to three [!DNL Amazon Sales Channel] stores for each of your [!DNL Amazon Seller Central] accounts. If you also sell in the U.K., you would have a fourth Amazon store.

>[!TIP]
>
>**Helpful onboarding tips**<br><br>
>Be aware that [!DNL Amazon Sales Channel] requires a [Professional Seller account][1] on [!DNL Amazon Seller Central] in the North America or European (UK) region. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan][2].<br><br>
>Onboarding is simple. Just create your store and then integrate (connect) it to to your [!DNL Amazon Seller Central] account.
>When your store is connected, [!DNL Amazon Sales Channel] attempts to import your Amazon listings and match them to your catalog, based on your [attribute mapping](./attributes-view.md).<br><br>
>Your [!DNL Amazon Sales Channel] settings affect your Amazon listings. Your initial listing, pricing, and product settings are defaulted for you. You can modify your [store settings](./ob-store-review.md) (listing, pricing, order, and reporting) after your store is connected to your [!DNL Amazon Seller Central] account.

|Steps|What Happens|
|--- |--- |
|[Pre-Setup Tasks](./amazon-pre-setup-tasks.md)|Before you onboard, you must ensure you have an active and approved [!DNL Amazon Seller Central] account. There are also some [!DNL Commerce] requirements and recommendations to complete prior to onboarding.|
|[Verify the Amazon API Key](./amazon-verify-api-key.md)|When accessing [!DNL Amazon Sales Channel], [!DNL Commerce] automatically checks and validates the Amazon API key you have added in your store configuration. If your API key has not been added or is invalid, you will be prompted to [add or update your Amazon API Key](./amazon-verify-api-key.md).|
|[Store Integration](./store-integration.md)|This step includes creating an [!DNL Amazon Sales Channel] store and then connecting it to your [!DNL Amazon Seller Central] account. You will need the primary log-in credentials for your [!DNL Amazon Seller Central] account (the email or phone used to create the seller account) for this step.|
|[Create Listing Rule](./ob-create-listing-rule.md)|After you connect your [!DNL Amazon Sales Channel] store, you are prompted to create a listing rule. We encourage you to create a rule, but you can also skip this step to start the listing import process. You can also access your [store and listing settings](./ob-store-review.md) on the store [dashboard](./amazon-store-dashboard.md).|

[1]: https://sell.amazon.com/{target="_blank"}
[2]: https://sell.amazon.com/pricing.html{target="_blank"}

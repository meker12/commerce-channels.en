---
title: Price Scope
description: Use the Commerce pricing scope to manage pricing according to multiple websites or globally.
---

# Price scope

[!DNL Commerce] provides configuration for your [pricing scope](https://docs.magento.com/user-guide/configuration/catalog/catalog.md#price){:target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there will be a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target="_blank"}.

If you change your catalog price scope from `Global` to `Website`, all price type attributes will also change to `Website`. See [Adding Websites](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target="_blank"}.

When a website price is chosen, there are two price sources:

- The website price
- The default (fall back) price

For the [!DNL Amazon Sales Channel] integration, based on your [Listing Rules](./listing-rules.md), you can map products from multiple websites into a single [!DNL Amazon Marketplace] Country ( defined during [store integration](./store-integration.md)). However, this introduces the issue of which price should be published if the product exists on multiple websites with differing prices.

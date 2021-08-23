---
title: Price Priority Logic
description: Amazon Sales Channel applies prioritization in determining the published price for an Amazon listing.
---

# Price priority logic

In the following example, how does the system determine if you should publish $31.99, $24.99, or $27.99?

![Commerce price scope](assets/amazon-price-scope.png)

To determine which price is used if a product is on two websites and has a varying price per website, use price priority logic (determined by the [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target="_blank"} value).

To view your stores' sort order, go to **Stores** > **All Stores** in the _Admin_ sidebar. In the _Web Site_ column, click the website name. The _Web Site Information_ page shows the _Sort Order_ setting for the website, which determines the priority of the website. A value of `1` indicates the highest priority.

If the product price is set to `Use Default`, it falls back to the default price value instead of the website price value.

## Example 1

||[Website Priority](https://docs.magento.com/user-guide/configuration/scope.html){:target="_blank"}|Price (Website)|Use Default|
|---|---|---|---|
|Default|0|$31.99|--|
|Store 1|1|$24.99|No|
|Store 2|2|$27.99|Yes|

- The **Magento Price Source** (defined in your [Listing Price](./listing-price.md) is set to the `Price` attribute.
- Look at the website with the highest website priority, which is Store 1 (defined by the [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target="_blank"} value).
- Since Store 1 is set to use the website price (Use Default = No), the published price is $24.99.

## Example 2

||[Website Priority](https://docs.magento.com/user-guide/configuration/scope.html){:target="_blank"}|Price [Website]|Use Default|
|---|---|---|---|
|Default|0|$31.99|--|
|Store 1|1|$24.99|Yes|
|Store 2|2|$27.99|No|

- The **Magento Price Source** (defined in your [Listing Price](./listing-price.md) is set to the `Price` attribute.
- Look at the website with the highest website priority, which is Store 1 (defined by the [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target="_blank"} value).
- Since Store 1 **is not** set to use the website price (Use Default = Yes), look at the next website in the sort order.
- Since Store 2 **is** set to use the website price (Use Default = No), the published price is $27.99.

## Example 3

||[Website Priority](https://docs.magento.com/user-guide/configuration/scope.html){:target="_blank"}|Price [Website]|Use Default|
|---|---|---|---|
|Default|0|$31.99|$30.00|
|Store 1|1|$24.99|--|
|Store 2|2|$27.99|$20.00|

This example adds the non-price value, which is used if you select another value for the **Magento Price Source** (defined in your [Listing Price](./listing-price.md) settings). The non-price value always uses price as the fallback price.

- The **Magento Price Source** (defined in your [Listing Price](./listing-price.md) settings) is set to `Non-Price`.
- Look at the website with the highest website priority, which is `Store 1`(defined by the [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target="_blank"} value).
- Since Store 1 **is not** set to use the `Non-Price` attribute, look at the next website in the sort order.
- Since Store 2 **is** set to use the `Non-Price` attribute (Non-Price [Website] = $20.00), the published price is $20.00.

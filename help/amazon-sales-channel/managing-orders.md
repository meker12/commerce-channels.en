---
title: Manage Orders
description: You can enable order import in your Order Settings to more easily manage your Amazon orders from your Commerce Admin.
---

# Manage orders

You can view your Amazon order information, as received from Amazon, in the _Recent Orders_ section of the [store dashboard](./amazon-store-dashboard.md) or on the _Amazon orders_ page (also called the _All Orders_ view).

How you manage your Amazon orders depends on whether or not you have order import enabled or disabled in your [Order Settings](./order-settings.md#configure-order-settings).

## With order import enabled

After [store integration](./store-integration.md), [**Import Amazon Orders**](./order-settings.md#configure-order-settings) is `Enabled` by default. This means that corresponding [!DNL Commerce] orders are created for your Amazon orders and can be managed in the [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html) workflow.

>[!NOTE]
>
>Regardless of your order import settings, Amazon orders that existed in your [!DNL Amazon Seller Central] account prior to your [store integration](./store-integration.md) do not import.

Imported Amazon orders are managed in the [[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html) workflow, just like your other [!DNL Commerce] stores. Click the Amazon order number in the _Order Number_ column to open the order in the [[!DNL Commerce] order process](https://docs.magento.com/user-guide/sales/order-processing.md#order-view-descriptions). See [View Amazon Orders](./amazon-orders-all.md).

### Order import process

When an order is placed on Amazon and [order import](./order-settings.md) is enabled, the following process begins.

|Change |Actions|
|---|---|
|An order is placed on Amazon. |- Amazon sets the order status to `Pending`.<br />- Order information is sent to [!DNL Commerce].<br />- Order is added to [_Amazon orders_ table](./amazon-orders-all.md) with a `Pending` status. |
|Amazon changes the order status to `Unshipped`. |- The status change is sent to [!DNL Commerce].<br />- In the [_Amazon orders_ table](./amazon-orders-all.md), the order status changes to `Unshipped`.<br />- In the [[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html), a corresponding [!DNL Commerce] order is created with a `Processing` status. |
|In [[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html), the [!DNL Commerce] order is processed and the status changes to `Shipped`. |- In the [_Amazon orders_ table](./amazon-orders-all.md), the order status changes to `Shipped`.<br />- On the next cron job, the order status changes to `Complete` in the [[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html). |

### Order creation blockers

There are a few scenarios that prevent the creation of the corresponding [!DNL Commerce] order. [!DNL Commerce] orders are not created for orders that are received when any of the following issues occur.

|Scenario|Solution|
|---|---|
|The item does not exist in the [!DNL Commerce] catalog. |[Create the new product](./creating-assigning-catalog-products.md) in your [!DNL Commerce] catalog and [manually match](./creating-assigning-catalog-products.md) it to the product. |
|The item in the catalog is disabled. |Make sure the [product status](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html) is enabled. |
|The ordered item is out of stock. |Update or configure the [product options](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html) for quantity and source. |

When orders cannot be imported, a system message similar to the following will appear at the top of the screen:

    `Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

When the issue is resolved, the [!DNL Commerce] order is created on the next sync.

## With order import disabled

If you do not want to import and manage your Amazon orders in [!DNL Commerce], you can change the [**Import Amazon Orders**](./order-settings.md#configure-order-settings) setting to `Disabled`. This means that when new orders are received from Amazon, corresponding [!DNL Commerce] orders are not created.

When disabled, order information received from Amazon appears in the _Recent Orders_ section of the store dashboard and in the _All Orders_ view. This order information is view only, and you must manage these orders in [!DNL Amazon Seller Central]. Click the Amazon order number in the _Order Number_ column to open the order details in [!DNL Amazon Seller Central]. See [View Amazon Orders](./amazon-orders-all.md).

See also [View Amazon Orders](./amazon-orders-all.md), [View Amazon Order Details](./amazon-order-details.md), and [Common Order Processing Tasks](./common-order-processing.md).

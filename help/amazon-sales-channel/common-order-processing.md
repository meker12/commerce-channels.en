---
title: Common Order Processing Tasks
---

# Common order processing tasks

[[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.md) can manage your Amazon orders, including emailing the buyer, fulfilling the order (shipping), issuing credits/refunds, adding comments, and more. To manage your Amazon orders, your [**Import Amazon Orders**](./order-settings.md) setting must be set `Enabled` so that corresponding [!DNL Commerce] orders are created when Amazon orders are received. Amazon order information shows in the _Recent Orders_ section of the store dashboard.

When enabled, corresponding [!DNL Commerce] orders are created for Amazon orders, and the Amazon order number shows in the _Order Number_ column. If a corresponding [!DNL Commerce] order is created, click the order number to open the order in the [!DNL Commerce] [order processing](https://docs.magento.com/user-guide/sales/order-processing.md) page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.md).

The [!DNL Commerce] order number does not show with the _Recent Orders_ information. The [!DNL Commerce] order number only shows when you click the Order Number on the store dashboard and open the order in [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.md). When viewing the [!DNL Commerce] order, the Amazon Order number appears in the _Payment & Shipping Method_ section, along with options to _View or Cancel Amazon Order_ and _View all Amazon Orders_, depending on the order's shipping status.

See [cancel an unshipped order](./cancel-unshipped-order.md).

![](assets/amazon-order-number-payment-info.png)
_Amazon Order info in the [!DNL Commerce] Order_

When processing an Amazon order, [!DNL Amazon Sales Channel] updates and syncs the order information with your [!DNL Amazon Seller Central] account. Your cron settings determine how often order information is synced between Amazon and [!DNL Amazon Sales Channel].

Common [!DNL Commerce] [order processing](https://docs.magento.com/user-guide/sales/order-processing.md) tasks include:

- [Order Actions](https://docs.magento.com/user-guide/sales/order-actions.md)
- [Order Search](https://docs.magento.com/user-guide/sales/orders-search.md)
- [Process an Order](https://docs.magento.com/user-guide/sales/order-processing.md)
  - [View an Order](https://docs.magento.com/user-guide/sales/order-processing.md#view-an-order)
  - [Process an Order](https://docs.magento.com/user-guide/sales/order-processing.md#process-an-order)
  - [Order and Account Information](https://docs.magento.com/user-guide/sales/order-processing.md#order-and-account-information)
  - [Address Information](https://docs.magento.com/user-guide/sales/order-processing.md#address-information)
  - [Payment & Shipping Method](https://docs.magento.com/user-guide/sales/order-processing.md#payment--shipping-method)
  - [Review items ordered](https://docs.magento.com/user-guide/sales/order-processing.md#review-items-ordered)
- [Issuing a credit/refund](https://docs.magento.com/user-guide/sales/credit-memo-create.md)
- [Fulfilling/shipping an order](https://docs.magento.com/user-guide/sales/shipments-create.md)
- [Create an invoice](https://docs.magento.com/user-guide/sales/invoice-create.md)
- [Cancel an unshipped order](./cancel-unshipped-order.md)

>[!NOTE]
>
>If an order is in `Unshipped` status, you can [cancel an Amazon order](./cancel-unshipped-order.md) on the [Amazon Order Details](./amazon-order-details.md) page. If an order has been shipped, it cannot be canceled.

See [Commerce Order Management](https://docs.magento.com/user-guide/sales/order-management.md).

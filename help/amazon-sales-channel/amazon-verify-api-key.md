---
title: Add or Verify the Amazon API Key
description: In your Commerce configuration, the validated Amazon API key allows you to integrate your stores with your Amazon Seller account.
---

# Add or verify the Amazon API key

When accessing [!DNL Amazon Sales Channel], [!DNL Commerce] automatically checks and validates the Amazon API key you have added in your store configuration. If validated, then you can move on to the next step, [Store Integration](./store-integration.md).

If the Amazon API key is missing, invalid, or expired, you must update your key. A message appears prompting you to get an API key and to add they key to your [!DNL Amazon Sales Channel] configuration.

## Get and add the Amazon API key as prompted

The API key is validated each time you access your [!DNL Amazon Sales Channel].

1. Log into the [!DNL Commerce Admin].

1. On the _Admin_ sidebar, go to **Marketing** > _Channels_ > **Amazon Sales Channel**.

    If this is your first time accessing [!DNL Amazon Sales Channel] or if you need to update your API key, the system prompts you through the process.

    ![Get and Add the Amazon API Key Prompt](assets/amazon-api-verification-prompt.png)

1. Click **Sign in** to access your [!DNL Commerce] web account.

    The [Commerce Accounts][1] page opens in a new browser tab.

   - If you are logged into your [!DNL Commerce] account, the _API Portal_ section of the _My Account_ page appears automatically.

   - If you are not logged in, you are prompted to enter your [!DNL Commerce] account username and password before the _API Portal_ tab appears.

   - If you need to create an account, visit [the [!DNL Commerce] account page][2] and register. This account should be part of your company or business.

1. If needed, you can view and generate API keys on the _API Portal_ tab in your [!DNL Commerce] account.

    If you need to create a new API key, enter a description like `Amazon Sales Channel` and click **Add New**. The new key is generated and shown with the name you entered. Click **Copy** to copy the new key.

    ![Generate or copy an API key](assets/amazon-add-api-key.png)

1. With the new key generated and copied, return to the _Amazon Sales Channel_ tab in the browser.

1. On the _Welcome to Amazon Sales Channel_ page, click **Add the key**.

    The browser exits [!DNL Amazon Sales Channel] and a store configuration page opens the _Api Keys_ page in the [!DNL Commerce Admin] at **Stores** > _Settings_ > **Configuration** > **Services** > **Magento Services**.

1. Paste the copied key for **Production Api key**.

1. Click **[!UICONTROL Save Config]**. You can now return to [!DNL Amazon Sales Channel].

    ![Adding your API Key in your store configuration](assets/config-magento-services-api-screen.png)

1. On the _Admin_ sidebar, go to **Marketing** > _Channels_ > **Amazon Sales Channel**.

   Re-accessing [!DNL Amazon Sales Channel] triggers [!DNL Commerce] verify and validate your API key and allows you to continue.

   If prompted to verify the key again, repeat this _Add and Verify_ process.

![Next icon](assets/btn-next.png) [**Continue to Store Integration**](./store-integration.md)

[1]: https://account.magento.com/apiportal/index/index/"target="_blank
[2]: https://account.magento.com/customer/account/login/"target="_blank

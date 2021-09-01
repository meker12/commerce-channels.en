---
title: Install the Amazon sales channel
description: To integrate your [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] and sell through the [!DNL Amazon Marketplace], download and install the Amazon sales channel extension.
---

>[!IMPORTANT]
>
>Only Amazon Sales Channel extension 4.0+ versions are supported when integrated with Adobe Commerce and Magento Open Source 2.4.x versions.

The [!UICONTROL Amazon Sales Channel] extension installs and adds features to integrate your Commerce catalog with [!DNL Amazon Seller Accounts] to sell through the [!DNL Amazon Marketplace]. To review additional information, see the [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) page in [!DNL Commerce Marketplace] and the [release notes](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) in the developer documentation.

## Requirements

-  **Commerce instance**: The Amazon sales channel extension can be installed on instances with Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure versions 2.3.x or later. It is no longer supported on 2.1, 2.2, or 1.x releases.
-  **Commerce web account**: You should have a Commerce web account, which is used to create and track an API key.
-  **API key**: Create an Amazon sales channel API key through your Commerce web account. The following instructions include these steps.

## Install

The Amazon sales channel extension installs from a `.zip` file, which is available from the [!DNL Commerce Marketplace]. It includes a composer.json which provides the name `magento/amazon-sales-channel` and the available version.

1. Log in to the [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target="_blank"}.

1. Click the **[!UICONTROL Marketplace]** tab, and then click **[!UICONTROL My Purchases]**.

1. Locate and select **[!UICONTROL Amazon Sales Channel]**.

1. On the extension page, select the version.

1. For the component name and version, click **[!UICONTROL Technical Details]**.

1. Click **[!UICONTROL Download]**.

1. Export the contents to your Magento root.

1. Follow all instructions for [extension installation](https://devdocs.magento.com/extensions/install/){target="_blank"} in the developer documentation.

1. Update the services connector entry in your `composer.json` file.

   -  Add the extension's name and version to your composer.json file.

   -  Navigate to your Commerce project directory and update your composer.json file.

     ```bash
     composer require magento/services-connector:~1.0.3
     ```

   -  Enter your [authentication keys](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"}. Your public key is your username; your private key is your password.

   -  Wait for Composer to finish updating your project dependencies and ensure that there are no errors.

## Add the Amazon sales channel API key

After installing, enter an [API Key](./amazon-verify-api-key.md)) to complete configuration.

## Set the Amazon channel configuration options

You have the following options for configuring the Amazon sales channel. You do not need to modify these settings to begin onboarding and selling on Amazon. It is recommended that advanced administrators consider these options.

1. Log into the Admin.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. Click **Sales Channels**, then **Global Settings**.

1. For **Clear Log History**, define the interval for clearing the collected logs.

   Options include `Once Daily`, `Once Weekly`, and `Once Monthly` (default).

1. For **Background Tasks (CRON) Source**, leave the `Magento CRON` setting.
   
   **_Advanced users recommendation_** - Advanced users can change this setting to Command Line (CLI) CRON.

1. Click **[!UICONTROL Save Config]**.

## Update the extension

1. Log in to the [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target="_blank"}.

1. Click the **[!UICONTROL Marketplace]** tab, and then click **[!UICONTROL My Purchases]**.

1. Locate and select **[!UICONTROL Amazon Sales Channel]**.

1. On the extension page, select the version.

1. For the component name and version, click **[!UICONTROL Technical Details]**.

1. Click **[!UICONTROL Download]**.

Complete the [extension upgrade instructions](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target="_blank"} in the developer documentation.

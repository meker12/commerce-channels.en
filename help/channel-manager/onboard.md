---
title: Onboard [!DNL Channel Manager]
description: Connect your instance to the [!DNL Channel Manager] service by completing a few onboarding steps.
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
---
# Onboard [!DNL Channel Manager]

Onboard Channel Manager by installing the Channel Manager extension on your [!DNL Commerce] instance and configuring API connections. These connections  enable communication and data synchronization between your Commerce instance and the Walmart Marketplace.

After you complete onboarding, configure and manage sales channel operations from the [!UICONTROL Channel Manager] option on the [!UICONTROL Commerce Admin Marketing] menu.

![[!DNL Channel Manager] option in Admin view](assets/channel-manager-admin-view.png)

## Onboarding overview

1. [Install the [!DNL Channel Manager] extension](install.md).

1. [Configure the [!DNL Commerce Services Connector]](connect.md) to integrate Channel Manager with the Commerce instance, and other supporting services.

1. [Connect your [!DNL Commerce] store to [!DNL Walmart Marketplace]](connect.md).

1. [Complete store setup](complete-store-setup.md).

## Prerequisites

- Verify that you have the required [Walmart Marketplace prerequisites](walmart-prerequisites.md) to integrate with Channel Manager.

- **Commerce account information**–Downloading and installing [!DNL Channel Manager] requires a [Commerce account](https://docs.magento.com/user-guide/magento/magento-account.html){target="_blank"}. You need an account ID and credentials with Owner or Admin access to the [!DNL Adobe Commerce] or [!DNL Magento Open Source] instance.

  - **MAGE ID**–[Log in](https://account.magento.com/customer/account/login/) to the Commerce account to get the ID from **[!UICONTROL My Account - Magento settings]**. You need this ID to register for the [!DNL Channel Manager] service Beta program.

     ![[!DNL MAGEID] on Commerce account settings](assets/mageid-my-commerce-account.png) 

  - **Access keys–** Get authentication keys to download Commerce extensions from the Commerce Composer repository `([!DNL repo.magento.com]`).

    ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

    On Adobe Commerce and Magento Open Source projects, the owner can set up [Shared Access](https://docs.magento.com/user-guide/magento/magento-account-share.html) to allow trusted employees and service providers to download extensions using credentials from the Owner or license holder account.

    On [!DNL Adobe Commerce] on cloud infrastructure projects, software installers must have the following access the [!DNL Commerce] instance:

    - Super User access to the Cloud project
    - Admin access to a specific environment
    - an [!DNL Adobe Commerce] or [!DNL Magento Open Source] account with permissions to access the Composer repository. 
    
    See [Manage user access](https://devdocs.magento.com/cloud/project/user-admin.html).

- **Authorization to download the Channel Manager Composer package**–Provide the MAGE ID from the Commerce account used to manage the service to the Adobe representative coordinating the Beta program for your organization.
- **Experience using Composer and the [!DNL Commerce CLI]** –See [General CLI Installation](https://devdocs.magento.com/extensions/install/){target="_blank"} for information about using these tools to install and manage extensions on [!DNL Adobe Commerce] or [!DNL Magento Open Source] platforms.
- **[Amazon Sales Channel version 4.4.2 or later](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)–If you have activated Amazon Sales Channel for your Commerce sites, verify that your Commerce platform has version 4.42 installed before you install Channel Manager.


### Requirements

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x or later](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Supported platforms

- Adobe Commerce on Cloud (ECE) : 2.4.x
- Adobe Commerce on premises (EE) : 2.4.x
- Magento Open Source 2.4.x
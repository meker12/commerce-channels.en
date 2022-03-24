---
title: Connect to Commerce Services
description: Connect Channel Manager instance to [!DNL Commerce services] to enable data synchronization and communication between the Commerce instance, Channel Manager, and other supporting services.
role: User
level: Intermediate
---
# Connect to Commerce Services

The Commerce Services Connector integrates the Channel Manager service with Adobe Commerce and Magento Open Source instances. The connector enables data synchronization and communication between the [!DNL Commerce] instance, [!DNL Channel Manager], and other supporting services.

 Commerce Services Connector setup is a one-time process required to use Adobe [Commerce SaaS services](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target="_blank"} like [!DNL Channel Manager], [!DNL Live Search], and [!DNL Product Recommendations]. If you have already configured the connector for another service, skip this step.

## Prerequisites

- **Commerce account**–To install software on Commerce instances, you must have an account with Owner or Admin access to the Commerce platform.

  Account owners and Admin users can create new Admin accounts from the Commerce instance or from the command line using the [!DNL Commerce] CLI command `admin:user:create`.

- **Adobe Commerce Production API Key**–This [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank" enables API access to services required by Channel Manager. You need the public and private credentials for this key.
    
  To provide the credentials, a Commerce license holder or account owner has options to 
  [share access](https://docs.magento.com/user-guide/magento/magento-account-share.html){target="_blank"}, or give the [API Key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank"} credentials to a trusted developer.

## Configure the Commerce Services Connector

1. Open the Store Services Configuration.

   - From the Admin, select **[!UICONTROL Stores]**.

   - Under *Settings*, select **[!UICONTROL Configuration]**.

   - Expand **[!UICONTROL Services]** and select **[!UICONTROL Commerce Services Connector]**.

1. Add Production API key credentials from your Adobe Commerce account.

   ![[!DNL Commerce Service Connector] service in the [!DNL Admin] view](assets/commerce-services-connector-admin-service-view.png)
     
  
   >[!NOTE]
   >
   > If your [!DNL Commerce] instance has other [!DNL Adobe Commerce] services like [!DNL Live Search] or [!DNL Product Recommendations] installed, the credential information displays in the interface, and no further configuration is required.

1. Configure the SaaS project and data space so that Commerce Services can send data to the Channel Manager service.

   ![[!DNL Commerce Service Connector] SaaS Identifier configuration in the [!DNL Admin] view](assets/commerce-services-connector-saas-config.png)
   

---
title: Connect Sales Channel to [!DNL Walmart Marketplace] 
description: Configure the sales channel and connect to Walmart Marketplace.
---
# Connect to [!DNL Walmart Marketplace]

After installing Channel Manager on your [!DNL Commerce] instance, connect a Commerce store to Walmart Marketplace.

1. Create the sales channel by [selecting the Commerce store for product listings](#select-the-commerce-store-for-the-sales-channel).

1. [Connect the channel to [!DNL Walmart Marketplace] by adding Walmart API credentials](#connect-the-channel-to-walmart-marketplace).

1. [Complete sales channel setup](#complete-store-setup) so you can manage listings, inventory, pricing, and sales from Channel Manger.

## Create the sales channel

1. Open Channel Manager.

   - In the Admin, select **[!UICONTROL Marketing** > _Channels_ > **Channel Manager]**. 

   - Select **[!UICONTROL Connect New Store]**.  
     
     ![Connect Commerce store to [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)   


1. Configure the store and connection:

   - Enter a unique **[!UICONTROL store name]**.

   - Select the **[!UICONTROL Adobe Commerce site]** for product listings.

   - Add an **[!UICONTROL email address]** to receive service notifications related to [!DNL Channel Manager].

     ![Configure connection between Commerce and [!DNL Walmart Marketplace] from [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## Connect the channel to Walmart Marketplace

1. Add the credentials for the [!DNL Walmart Marketplace Adobe Production API key] from your [!DNL Walmart Marketplace Seller] account.

   - If you don’t have the credentials, select **[!UICONTROL Get API credentials]** to get them from the [!DNL Walmart Marketplace Developer Portal].

     If prompted, select your region (US and Canada) and then log in.  

     ![[!DNL Walmart Marketplace] account login](assets/walmart-marketplace-login-page.png)
       
   - On the API key form, copy and save the **[!UICONTROL Client ID]** and **[!UICONTROL Client Secret]** values for the [!UICONTROL Adobe Inc Production API key] to a secure location. 

     ![[!DNL Walmart Marketplace API key] configuration page](assets/walmart-api-key-management-form.png) 
       
     >[!NOTE]
     >
     >If you don't see an [!DNL Adobe Inc] key in the Developer Portal, select **[!UICONTROL Add New Key for a Solution Provider]** to configure permissions and generate the key. For configuration details, see [Generate a [!DNL Walmart Marketplace API Key]](overview.md#generate-a-walmart-marketplace-api-key).

   - Return to [!DNL Channel Manager] to add the credentials to the **[!UICONTROL Walmart Connection]** information.  
       
     When you add credentials to [!DNL Channel Manager], Adobe hides the client secret and stores the value in a secure vault.  

1. [!UICONTROL Save] the configuration to establish the connection.

   After connecting successfully, manage the channel from **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] configuration page](assets/manage-connected-stores.png)


### Troubleshoot connection issues

If the connection to Walmart fails, see the [Walmart Marketplace FAQ](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} for troubleshooting tips.

- From the [!DNL Walmart Developer Portal], verify that you copied the correct credentials for the production API key for [!UICONTROL Adobe Inc.]

- Verify that the access configuration for the Walmart Adobe API key has the correct permissions. See [Walmart Prerequisites](overview.md#walmart-prerequisites).

- Confirm that the Walmart API service is available from the [Walmart API status page](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.


## Complete store setup

After you connect a Commerce store to [!DNL Walmart Marketplace], you can complete store setup from the [!DNL Channel Manager Stores] view. 

To complete store setup:

1. From the Admin, select **[!UICONTROL Marketing** > **Channel Manager**].

   ![[!DNL Walmart Marketplace API key] configuration page](assets/connect-commerce-store-config.png)

1. Open a connected sales channel by selecting the pencil icon in a store entry row.

1. Begin sales channel operations.

   - Add products from your Commerce Catalog to Channel Manager

   - Publish products to Walmart using product matching

   - View and manage inventory and pricing

   - View and manage Walmart orders from the Commerce Admin

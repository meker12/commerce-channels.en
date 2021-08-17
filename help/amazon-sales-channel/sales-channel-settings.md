---
title: Sales Channel Admin Settings
description: Update the Commerce configuration to manage logging, cron source, and synchronization for Amazon Sales Channel functions.
---

# Sales Channel Admin settings

When the [!DNL Amazon Sales Channel] extension is installed, default values are set in the Admin for [!DNL Amazon Sales Channel]. These settings can be modified in your configuration settings for your Amazon store. These settings include:

- Intervals for clearing Activity Log history
- Cron source selection
- Log synchronization options

## Modify the Admin settings

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. Scroll down and click **Sales Channels** and then **Global Settings**.

1. For **Clear Log History**, choose an option.

   - **Once Daily** - Choose to clear your store activity history once daily.

   - **Once Weekly** - Choose to clear your store activity history once weekly.

   - **Once Monthly** - (Default) Choose to clear your store activity history once monthly.

1. For **Background Tasks (CRON) Source**, choose `Magento CRON`.

   This tells [!DNL Amazon Sales Channel] to used your [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) settings to determine communication and data sync intervals with [!DNL Amazon Seller Central].

1. For **Enable Debug Logging**, choose `Enabled` to collect additional synchronization data when troubleshooting is needed.

   [!DNL Amazon Sales Channel] logging is written to the `{Commerce Root}/var/log/channel_amazon.log` file and can be viewed in [developer mode](https://docs.magento.com/user-guide/magento/installation-modes.html). Logging should only be `Enabled` during troubleshooting and should be `Disabled` when troubleshooting is complete.

1. Click **[!UICONTROL Save Config]**.

![](assets/config-sales-channel-global-settings.png)
[_Sales Channel Settings_](https://docs.magento.com/user-guide/configuration/sales-channels/global-settings.html)

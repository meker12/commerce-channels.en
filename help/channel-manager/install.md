---
title: Install [!DNL Channel Manager]
description: Install the Channel Manager extension.
---

# Install Channel Manager

Review the [prerequisites](onboard.md#prerequisites) and gather required information before you install Channel Manager.

## Update minimum-stability setting

Before installing the extension, you must update the `minimum-stability` requirement in your `composer.json` file so you can install early versions of Channel Manager using Composer.

To update the configuration, add the following lines to the `composer.json` file.

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## Install the extension

The installation instructions depend on whether you are installing Channel Manager on an on-premises or cloud Commerce instance:

- Install on an [On-premises instance](#install-on-an-on-premises-instance).

- Install on an [[!DNL Adobe Commerce] on cloud infrastructure instance](#install-adobe-commerce-on-cloud-infrastructure)

Both methods require you to use the Command Line Interface (CLI).

>[!NOTE]
>
>If you are unfamiliar with installing Commerce software using the CLI, see [General CLI Installation](https://devdocs.magento.com/extensions/install/){target="_blank"}. 

### Install on an on-premises instance

Use these instructions to install on Adobe Commerce and Magento Open Source platforms.

1. Log in to the [!DNL Commerce] server as a [user with permissions](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target="_blank"} to write to the [!DNL Commerce] file system.

1. Put your website into [maintenance mode](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target="_blank"}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. From the [!DNL Commerce] project root directory, add Channel Manager to `composer.json`.

   ```bash 
    $ composer require magento/channel-manager --no-update
   ```

1. If prompted, enter the access keys from your [!DNL Commerce] account.

   Your public key is your username; your private key is your password.

1. Update the dependencies and install the extension.

   ```bash
   $ composer update
   ```

   The `composer update` command updates all dependencies. If you only want to update dependencies related to Channel Manager, use this command instead: `composer update magento/channel-manager`.

1. Wait for Composer to finish updating your project dependencies and resolve any errors.

1. Verify the installation

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:
   
   ```terminal
   Module is disabled
   ```

1. Register the extension.
 
   ```bash
   $ bin/magento setup:upgrade
   ```

1. If prompted, recompile your [!DNL Commerce] project.

   ```bash
   $ bin/magento setup:di:compile
   ```

1. Verify that the extension is enabled:

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:

   ```bash
   Module is enabled
   ```

1. Clean the cache.

   ```bash
   $ bin/magento cache:clean
   ```

1. Disable maintenance mode.

   ```bash
    $ bin/magento maintenance:disable
   ```

### Install on an Adobe Commerce on cloud infrastructure instance

Work in a development branch when adding an extension to your cloud instance.

For help with using branches, see [Get started creating branches](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target="_blank"} in the Adobe Commerce developer documentation.

When installing an extension, the extension name (&lt;VendorName>\_&lt;ComponentName>) is automatically inserted in the [app/etc/config.php](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html){target="_blank"} file. You do not need to edit the file directly.

1. On your local workstation, change to the Cloud project root directory.
1. Create or check out a development branch. See [branching](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target="_blank"}.
1. Using the Composer name, add the extension to the `require` section of the composer.json file.  

   ```bash  
   $ composer require magento/channel-manager --no-update
   ```

1. Add, commit, and push code changes–include changes to both the `composer.lock` and `composer.json` file.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin &lt;branch-name>
   ``` 
  
1. After build and deploy completes, use SSH to log in to the remote environment and verify that the extension installed correctly.

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:

   ```terminal
   Module is enabled
   ```

1. After installation completes successfully, log in to the [!UICONTROL Admin] to [configure the Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >For instructions to update Channel Manager to a new release, see [Upgrade modules and extensions](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target="_blank"}.


## Troubleshooting

Use the following information to resolve errors that occur during the Channel Manager installation process.
 
### Incorrect composer keys

If the [access keys](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"} used to authenticate to the Composer repository are invalid, or not linked to the [!DNL MAGE ID] used to sign up for the [!DNL Channel Manager] service, the following error displays.  
  

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Check the key configuration:

1. Find the location of the `auth.json` file:

   ```bash
   $ composer config –global home
   ```

1. View the `auth.json` file.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Verify that the credentials in the auth.json match[ the keys associated with the MAGE ID](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"} used to register for the Channel Manager service.


### Insufficient memory for PHP

The following error displays if the system does not have enough memory allocated for PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Use either of the following methods to resolve the memory issue:

- [Increase the memory limit for PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target="_blank"} in the environment `php.ini` file. Also, verify that the Commerce instance has the [recommended values](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target="_blank"} for other PHP settings.

- Specify the memory limit from the command line.

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  For example:  
  
  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```


### Cloud deployment errors

For problems deploying the extension to the cloud, see[extension deployment failure](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target="_blank"}.

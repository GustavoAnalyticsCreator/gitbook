---
description: >-
  This guide will walk you through configuring AnalyticsCreator with your
  system.
noIndex: true
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Configuring AnalyticsCreator

### Provide the Login and Password that you received by e-mail from AnalyticsCreator

{% embed url="https://cdn2.hubspot.net/hub/7543628/hubfs/image-png-2.png?height=952&name=image-png-2.png&width=1903" %}

Click on the gear ![](https://cdn2.hubspot.net/hub/7543628/hubfs/image-png-3.png?width=35\&height=31\&name=image-png-3.png) button to access all the AnalyticsCreator user configuration settings.

**Configuration settings**

The configuration of AnalyticsCreator is very simple, the only mandatory configuration is the **SQL Server Settings (Number one)**

1. **SQL Server Settings:**&#x20;
   1. Use LocalDB to store repository: Enables you to store the AnalyticsCreator project (Metadata only) on your LocalDB
   2. .SQL Server to store repository: The IP address or the name of your Microsoft SQL Server
   3. Security
      1. Integrated : The method of authentication is integrated for the current user .
      2. Standard : User name & Password.
      3. Azure AD:  Uses Azure AD ( The new [Microsoft Entra)](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id?msockid=376ea588b059689f1c0eb0bcb1df69a1) for the Microsoft SQL Server authentication.
      4. Trust server certificate :  To rely on the server certificate.
   4. SQL user: The SQL Server user
   5. SQL password : The SQL Server user password.
2. **Paths**
   1. UNC (Universal Naming Convention) path to store backup: The local folder to store your project backup.
   2. Local SQL Server path to store backup: The local folder to store your project backup.
   3. Local SQL Server path to store database: The local folder to store your SQL Server project backup.
   4. Repository database template: The alias for your repositories. By default, we use repo\_{RepoName}.
   5. DWH database template: The alias for your DWH templates. By default we use dwh\_{RepoName}.
3. **Proxy settings**
   1. Proxy address: The IP address or the host of your proxy server.
   2. Proxy port: The port number of you proxy
   3. Proxy user: The username of your proxy
   4. Proxy password: The password of your proxy user.

Now you're ready to create your new Data Warehouse with AnalyticsCreator.

&#x20;

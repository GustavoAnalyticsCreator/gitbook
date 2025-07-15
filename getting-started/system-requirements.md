---
description: The Analytics Creator Installation
noIndex: true
---

# System Requirements

To ensure optimal performance, verify that the following requirements are met:

{% hint style="info" %}
If you already have SQL Server installed and accessible, you can proceed directly to the\
&#x20;[Launching AnalyticsCreator section.](../launching-analyticscreator/editor/)
{% endhint %}

* **Networking:**
  * **Communication over Port 443 is where analytics communicates to the sAnalyticsCreator server.**
* **Operating System:** Windows 10 or later.\
  &#x20;_AnalyticsCreator is compatible with Windows operating systems starting from version 10._

{% hint style="warning" %}
Port 443 is the **standard HTTPS port for secured transactions.** It is used for data transfers and ensures that data exchanged between a web browser and websites remains encrypted and protected from unauthorized access
{% endhint %}

* **Microsoft SQL Server:**&#x20;
  * **Azure SQL:** &#x20;
    * Managed Instance
  * **On Premises**&#x20;
    * Supported editions include Express, Standard, and Enterprise from Microsoft SQL Server 2012 onward.\
      &#xNAN;_&#x41;nalyticsCreator utilizes SQL Server to store project data, so it is essential to have a compatible version installed before continuing._

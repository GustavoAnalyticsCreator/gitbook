# Snapshots and snapshot groups

Snapshots and Snapshot Groups Snapshots are predefined dates calculated during the ETL process and used in Snapshot Transformations to combine historicized data.&#x20;

By default, there is always at least one snapshot, referred to as the "Actual Date", which represents the current timestamp. Additional snapshots can be defined as needed.&#x20;

Below is a typical snapshot definition:

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

**SQL Expression for Calculating the Previous Date**\
This SQL expression calculates the previous date relative to a given **@ActDate**. It uses the **DATEADD**, **CONVERT**, and **DATEPART** functions to adjust the date by subtracting days and converting between data types. The example demonstrates how to manipulate and calculate date values in SQL.

```sql
DATEADD(ms, -2, CONVERT(datetime, CONVERT(date, DATEADD(dd, 1-DATEPART(d, @ActDate), @ActDate))))

```



Each snapshot must have a unique name.\
An SQL statement is used to calculate the snapshot value, and the predefined variable **@ActDate**, which represents the current timestamp, can be utilized within this statement.\
Multiple snapshots can be organized into snapshot groups for better management and functionality, as demonstrated in the example below.

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

**Working with Multiple Snapshots**\
When working with multiple snapshots, a **Snapshot Dimension** can be defined and used as a common dimension in the data mart layer.\
To create a Snapshot Dimension, use the corresponding context menu, as demonstrated in the example below.

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

Snapshots are used in regular snapshot transformations to combine historicized data based on predefined dates. These transformations depend on snapshot values to accurately represent the historical context of the data, as shown in the image below.

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

<img src="../../.gitbook/assets/image (59).png" alt="" data-size="original">

**Using Snapshot Groups and Individual Snapshots**\
Both snapshot groups and individual snapshots can be utilized. All selected snapshots are applied during the transformation process.

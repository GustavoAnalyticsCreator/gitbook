# Snapshots and snapshot groups

Snapshots are predefined dates calculated during the ETL process and utilized in Snapshot Transformations to combine historicized data.

By default, there is always at least one snapshot, referred to as the **“Actual Date”**, which represents the current timestamp. Additional snapshots can be defined as needed. Below is a typical snapshot definition:

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

```sql
DATEADD(ms, -2, CONVERT(datetime, CONVERT(date, DATEADD(dd, 1-DATEPART(d, @ActDate), @ActDate))))

```



Each snapshot must have a unique name.

An SQL statement is used to calculate the snapshot value. The predefined variable `@ActDate`, representing the current timestamp, can be utilized within this statement.

Multiple snapshots can be organized into snapshot groups for better management and functionality, as demonstrated in the example below.

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

When working with multiple snapshots, a Snapshot Dimension can be defined and utilized as a common dimension in the data mart layer.

To create a Snapshot Dimension, use the corresponding context menu, as demonstrated in the example below.

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

Snapshots are used in the regular snapshot transformations:

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

<img src="../../.gitbook/assets/image (59).png" alt="" data-size="original">

Both snapshot groups and individual snapshots can be utilized. All selected snapshots are applied during the transformation process.

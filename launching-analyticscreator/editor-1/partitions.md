---
noIndex: true
icon: buildings
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Partitions

Partitions are an essential part of optimizing OLAP cubes, enabling you to split large datasets into smaller, more manageable segments. This improves query performance and makes it easier to work with large data volumes in both multidimensional and tabular models.

#### **Partitions in Data Mart**

Partitions are used to divide data into smaller, more manageable segments within **multidimensional** and **tabular OLAP cubes**. By defining partitions, you can optimize query performance and manage large datasets more effectively.

Partitions are applicable to facts and dimensions in the **datamart layer**. In **multidimensional OLAP cubes**, only fact partitions are used, while in **tabular OLAP cubes**, both facts and dimensions can be partitioned.

***

#### **Steps to Create or Edit a Partition**

**1. Add a New Partition**

To add a new partition, follow these steps:

* In the **navigation tree**, right-click **Partitions** and click **Add Partition**.

**2. Define Partition Details**

Once you click **Add Partition**, complete the following fields:

* **Partition Name**: Enter a name for the partition.
* **Table**: Select the table you want to partition from the list.
* **Slice**: Type the slice value that specifies how data will be partitioned.
* **SQL Command**: Type the SQL command that will be executed to define the partition.

**3. Save the Partition**

After defining the partition, click the **Save** button to create or update the partition.

***

#### **Note:**

Microsoft documentation on partitioning may offer additional insights. You can consult the official documentation for more detailed information on how to optimize partitions for performance and manageability.

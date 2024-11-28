---
noIndex: true
icon: sitemap
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

# Hierarchies

Hierarchies are vital for structuring data in both **multidimensional** and **tabular** models. By organizing dimension attributes in a parent-child relationship, you ensure a clearer and more intuitive way of accessing data. Follow the steps above to create and manage hierarchies within your Data Mart system.

#### **Hierarchies in Data Mart**

Hierarchies allow you to create logical parent-child structures within your data warehouse. They are essential in both **tabular** and **multidimensional OLAP** cubes, enabling you to define how dimensions should be organized and queried.

***

#### **Steps to Create or Edit a Hierarchy**

**1. Add a New Hierarchy**

To create a new hierarchy, follow these steps:

* In the **navigation tree**, right-click **Hierarchies** and click **Add Hierarchy**.

**2. Define Hierarchy Details**

Once you click **Add Hierarchy**, complete the following fields:

* **Schema**: Select the schema where you want to add the hierarchy.
* **Table**: Choose the table where the hierarchy will be applied.
* **Hierarchy Name**: Enter the name of the hierarchy.
* **Description**: Provide a description of the hierarchy.

**3. Define Hierarchy Sequences**

Next, configure the hierarchy sequence:

* **Column**: Choose the column from the table to define the hierarchy.
* **SeqNr**: Select the sequence number for the hierarchy (indicating its position in the hierarchy).
* **Name**: Type the name of the hierarchy sequence.
* **Description**: Type a description of the hierarchy sequence.

**4. Save the Hierarchy**

After configuring the hierarchy and its sequence, click the **Save** button to create or update the hierarchy.

***

#### **Additional Information**

Once the hierarchy is defined, it can be used in OLAP cubes for better data analysis. Hierarchies help organize dimension attributes logically, which makes it easier for users to navigate and query the data.

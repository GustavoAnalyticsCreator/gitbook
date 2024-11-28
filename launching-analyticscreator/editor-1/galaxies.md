---
noIndex: true
icon: stars
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

# Galaxies

Stars are a key component in building a structured and efficient data model for reporting and analysis. By creating a star schema with relevant galaxies and schemas, you can improve your data warehouse architecture and facilitate easier querying for users. Use the steps above to create and manage stars within your Data Mart system.

## **Stars in Data Mart**

Stars are used to define a central fact table surrounded by related dimension tables, following the star schema design pattern. This structure helps organize and optimize your data for better analysis and reporting.

#### **Steps to Create or Edit a Star**

**1. Add a New Star**

To add a new star, follow these steps:

* In the **navigation tree**, right-click **Galaxies** and click **Add Star**.

**2. Define Star Details**

Once you click **Add Star**, fill out the following fields:

* **Star Name**: Enter the name of the star you are creating.
* **Galaxy**: From the dropdown list, select the galaxy where you want to add the star.
* **Schema**: Select the schema where the star will be stored.
* **Order in Diagram**: Specify the position of the star in the data model diagram (if necessary).
* **Description**: Provide a brief description of the star, explaining its purpose and functionality.

**3. Define Model Type**

Next, choose the type of model for the star:

* **Multidimensional**: Select this tab if you are using the multidimensional model and wish to perform MDX (Multidimensional Expressions) queries.
* **Tabular**: Select this tab if you are using the tabular model.

**4. MDX Code**

In the **MDX** box, type or paste the MDX code for the star if you’re working with the multidimensional model.

**5. Save the Star**

After filling out all required fields and entering the MDX code (if applicable), click the **Save** button to create or update the star.

***

#### **Additional Information**

Once you have created the star, you can start adding scripts or further customizations to the star schema for your analytical needs.

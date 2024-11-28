---
icon: key-skeleton-left-right
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

# Indexes

An **Index** is crucial for optimizing the performance of the data warehouse by enabling faster search and retrieval of data. It helps to speed up data queries, reduce query execution time, and improve overall database performance, especially when dealing with large datasets. Creating the right indexes is an important part of database tuning.

_Breadcrumb:_\
Indexes → Index → Double-click\
Toolbar → DWH → Index → Double-click\
Navigation tree → Indexes → Add index\
Navigation tree → Indexes → Index → Edit index

### **Create a New Index**

To create a new index, follow these steps:

1. In the **Navigation Tree**, right-click **Indexes** and click **Add Index**.
2. In the **Schema** box, select the schema or layer where you want to add the Index.
3. In the **Table** box, select the table from the source. You must have added the source table beforehand.
4. In the **Index Name** box, type a name for the Index.
5. In the **Compression Type** list, select the MS SQL Server compression type.
6. Select the **check-boxes** for the index properties:
   * **Is Unique**
   * **Is Primary Key**
   * **Is Clustered**
   * **Is Column store**
7. Add the **Columns** in the list to define the desired processing for the index.

| Property          | Description                               |
| ----------------- | ----------------------------------------- |
| **Column**        | Name of the column to add to the index    |
| **Position**      | Position of the column (1, 2, 3, ...)     |
| **Is Descending** | Sort order. Active check-box = descending |
| **Include Only**  | Include only the field                    |

8. Click the **Save** button to create the index.

***

### **Manage Indexes**

* **List and Search Indexes**:\
  You can list and search for all created indexes by navigating to the **Indexes** section in the navigation tree. You can also search for specific indexes using the search field and delete or duplicate them as necessary.
* **Delete or Duplicate an Index**:\
  You can delete or duplicate an index by selecting it from the list and clicking the corresponding option.

### **Related Links**

* To better understand index functionality, refer to the Microsoft T-SQL documentation:\
  [CREATE INDEX](https://docs.microsoft.com/en-us/sql/t-sql/statements/create-index-transact-sql?view=sql-server-ver15)
* For more details on listing and searching objects, visit List and Search Objects.

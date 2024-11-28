---
icon: filter
noIndex: true
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

# Filters

Filters in AnalyticsCreator are mechanisms for refining and selecting data during transformations, queries, or ETL processes. They allow users to define conditions that limit the data being processed, improving performance and ensuring that only relevant data is included in the results.

***

#### **Key Features of Filters**

1. **Data Refinement**:
   * Filters help in narrowing down data sets by including or excluding records based on specified conditions.
   * Examples: Selecting rows where a column value matches a specific pattern or excluding records with null values.
2. **Flexible Condition Definitions**:
   * Supports a variety of logical operators (`=`, `!=`, `>`, `<`, `LIKE`, etc.) and functions (`ISNULL`, `LEN`, etc.).
   * Allows for the combination of multiple conditions using `AND`/`OR`.
3. **Dynamic Parameters**:
   * Filters can use parameterized values for greater flexibility. For example, you can create a filter condition like `DATE >= :StartDate` to dynamically adapt to different date ranges.
4. **Multi-Layer Application**:
   * Filters can be applied at various stages of the data pipeline, including:
     * Data source extraction
     * Transformation processes
     * Data presentation layers (e.g., reports or dashboards)

***

#### **Creating a Filter**

**1. Add a Filter**

To create a filter, follow these steps:

1. Navigate to **Filters** in the **navigation tree**.
2. Right-click and select **Add Filter**.

**2. Define Filter Details**

* **Name**: Provide a unique name for the filter.
* **Description**: Add a short description explaining the purpose of the filter.
* **Condition**: Define the filter condition using SQL-like syntax. Example: `Country = 'USA' AND Sales > 1000`.
* **Parameters**: Optionally add dynamic parameters for reusable filter conditions. Example: `Region = :RegionName`.

**3. Save the Filter**

* Once the filter is defined, click **Save** to add it to your repository.

***

#### **Using Filters**

Filters can be applied in various contexts throughout AnalyticsCreator:

1. **Source Data**: Apply filters at the connector level to limit data extraction from the source.
2. **Transformations**: Use filters in data transformation processes to refine intermediate results.
3. **Reports/Dashboards**: Apply filters to ensure reports focus only on relevant data.

***

#### **Example Filter Configurations**

1.  **Static Condition**:\


    ```sql
    SELECT * FROM Sales WHERE Country = 'USA'
    ```

This filter always limits data to sales in the USA.

1.  **Dynamic Condition with Parameters**:\


    ```sql
    SELECT * FROM Orders WHERE OrderDate BETWEEN :StartDate AND :EndDate
    ```

This filter dynamically adjusts the date range based on provided parameters.

***

#### **Best Practices for Using Filters**

* **Optimize Performance**: Apply filters as early as possible in the data pipeline to reduce unnecessary data processing.
* **Use Parameterization**: Leverage parameters for reusability and flexibility across multiple queries or transformations.
* **Combine Conditions Thoughtfully**: Use logical operators (`AND`, `OR`) to precisely define the filter logic.

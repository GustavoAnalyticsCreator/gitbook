---
noIndex: true
icon: toolbox
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

# Predefined transformations



**Breadcrumb:**\
Toolbar → Predefined Transformation → Double-click\
Navigation Tree → Predefined Transformations → Add Predefined Transformation\
Navigation Tree → Predefined Transformations → Predefined Transformation → Edit Predefined Transformation

***

#### **Overview**

Predefined transformations in AnalyticsCreator provide a flexible and reusable way to apply standard logic or operations across multiple workflows and projects. These transformations help automate repetitive tasks, improve consistency in data processing, and reduce the time needed to set up similar workflows manually.

AnalyticsCreator includes several built-in predefined transformations. These pre-defined transformations cover common data operations and can be customized or extended to suit specific use cases. Each transformation is defined using SQL-like logic and can be evaluated and tested before use.

***

#### **Why Use Predefined Transformations?**

* **Efficiency**: Streamline workflows by reusing transformations across projects.
* **Consistency**: Standardize logic across teams and projects for uniform data handling.
* **Scalability**: Simplify complex operations by encapsulating them into modular, reusable components.
* **Flexibility**: Customize transformations to fit specific data processing needs, such as cleansing, enrichment, or restructuring data.

***

#### **Steps to Add a Predefined Transformation**

**1. Add a New Transformation**

* In the **navigation tree**, right-click **Predefined Transformations** and select **Add Predefined Transformation**.

**2. Define Transformation Details**

* **Name**: Enter a unique name for the predefined transformation that reflects its purpose or functionality.
* **Description**: Provide a clear and detailed description to explain the transformation’s role and logic. This helps other users understand its purpose.

**3. Enter Transformation Logic**

In the statement section, define the logic or SQL-like statements that drive the transformation.

| **Statement**                | **Description**                                                                                                            |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Check Statement**          | Use to validate the structure or logic of the transformation. Helps ensure that the logic is error-free before deployment. |
| **Transformation Statement** | The core SQL-like statement that defines how the transformation manipulates or processes the data.                         |
| **Evaluated Statement**      | Previews the expected result of applying the transformation logic on test data.                                            |
| **Allowed Keywords**         | Specifies reserved keywords or rules for the transformation logic, ensuring compatibility and preventing conflicts.        |

Example of a **Transformation Statement**:

```sql
CASE
    WHEN :1 < '19800101' THEN 0
    WHEN :1 > '20401231' THEN CONVERT(bigint, DATEDIFF(DD, '19800101', '20401231') + 1)
    ELSE CONVERT(bigint, ISNULL(DATEDIFF(DD, '19800101', CONVERT(date, :1)) + 1, 0))
END
```

**4. Evaluate the Transformation**

* Click the **Evaluate** button to test the transformation logic and verify its correctness.
* This step ensures that any syntax errors or logical issues are identified and fixed before saving the transformation.

**5. Save the Transformation**

* Once the transformation has been evaluated successfully, click the **Save** button to store it in the repository.

***

#### **Applying Predefined Transformations**

Predefined transformations can be applied to various components, including:

* **Data Sources**: Automate data cleansing or enrichment directly at the source level.
* **Transformations**: Reuse transformations across projects for consistent data processing.
* **Data Outputs**: Ensure standardization in data formatting or business rule applications before exporting data.

***

#### **Managing Predefined Transformations**

* **Edit Transformations**: Navigate to an existing transformation in the **navigation tree** and double-click to edit its logic, parameters, or description.
* **Organize Transformations**: Use the navigation tree to group or categorize transformations for easier management.
* **Audit and Test**: Regularly evaluate transformations to ensure they meet current business requirements.

***

#### **Best Practices for Predefined Transformations**

1. **Descriptive Naming**: Use meaningful names for transformations to make them easily identifiable.
2. **Detailed Descriptions**: Provide clear descriptions to help other users understand the transformation’s purpose.
3. **Parameterization**: Use placeholders (`:1`, `:2`, etc.) for dynamic inputs, allowing greater flexibility and reusability.
4. **Testing**: Always use the **Evaluate** feature to test transformations with sample data before applying them in production.
5. **Version Control**: Maintain a record of changes to transformations to track improvements or modifications over time.

***

Predefined transformations are a cornerstone of efficient data handling in AnalyticsCreator, enabling users to define, reuse, and customize logic for various data operations. By leveraging predefined transformations effectively, you can optimize workflows, reduce errors, and maintain consistency across your data projects.

\
\

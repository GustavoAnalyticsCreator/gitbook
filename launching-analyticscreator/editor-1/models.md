---
noIndex: true
icon: kaaba
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

# Models

Models in AnalyticsCreator are representations of your data warehouse’s structure and relationships. They define how data is organized, stored, and accessed, serving as blueprints for building and maintaining the data warehouse. Models provide a clear visualization of the relationships between tables, dimensions, facts, and other elements.

***

#### **Key Features of Models**

1. **Data Structure Definition**: Models define the organization of facts, dimensions, hierarchies, and relationships in the data warehouse.
2. **Schema Representation**: Models represent the underlying database schema in a user-friendly and visual format.
3. **Customizability**: Users can create and customize models to align with business requirements and data needs.
4. **Multiple Modeling Approaches**:
   * **Star Schema**: Simplifies reporting by centering around fact tables connected to dimension tables.
   * **Data Vault 2.0**: Emphasizes scalability, agility, and historical tracking.
   * **Medallion Architecture**: Focuses on organizing data into bronze, silver, and gold layers for incremental value addition.

***

#### **Steps to Create a Model**

**1. Add a New Model**

1. In the **navigation tree**, right-click **Models** and select **Add Model**.
2. Provide the following details:
   * **Model Name**: A meaningful name that reflects the purpose of the model.
   * **Description**: A short description explaining the model’s role in the data warehouse.

**2. Define Model Components**

* Add tables, dimensions, and facts to the model.
* Configure relationships between tables, such as primary key and foreign key relationships.

**3. Select a Modeling Approach**

Choose the modeling approach that best suits your requirements:

* **Star Schema**: Ideal for reporting and analytics.
* **Data Vault**: Best for scalability and capturing historical changes.
* **Medallion Architecture**: Suitable for progressive refinement and transformation of data.

**4. Save the Model**

* After configuring the model, click **Save** to store it in the repository.

***

#### **Managing Models**

1. **List and Search Models**: View all existing models in the navigation tree under **Models**.
2. **Edit Models**: Update the structure, components, or descriptions of a model by selecting it and clicking **Edit Model**.
3. **Delete Models**: Remove outdated or unused models to maintain repository cleanliness.

***

#### **Best Practices for Models**

1. **Choose the Right Approach**: Select the modeling method (Star Schema, Data Vault, or Medallion Architecture) based on the business and technical requirements.
2. **Use Descriptive Naming**: Name models and their components clearly to make them easy to understand and navigate.
3. **Optimize Relationships**: Define relationships accurately to ensure consistency and integrity in the data.
4. **Document Models**: Include detailed descriptions for each model to communicate their purpose and structure effectively.

***

#### **Advanced Features**

* **Multiple Models**: Create and manage multiple models within the same repository for different business domains or use cases.
* **Model Validation**: Validate the structure and relationships in the model to ensure correctness and consistency.
* **Integration with Layers**: Models can be tied to specific layers in the data warehouse for better organization and processing.

***

#### **Examples of Use Cases**

1. **Sales Analysis**: Use a star schema model to define sales data with a central fact table and dimension tables for products, customers, and regions.
2. **Data Vault for Historical Tracking**: Build a Data Vault model to track historical changes in customer data over time.
3. **Medallion Architecture for ETL**: Define models for each layer (bronze, silver, gold) to progressively transform raw data into actionable insights


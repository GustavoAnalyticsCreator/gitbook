---
icon: layer-group
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

# Layers detailed

AnalyticsCreator empowers users to define and customize layers within their Data Warehouse projects, offering flexibility to align with popular methodologies and architectures. Layers serve as the foundation for organizing and transforming data throughout its lifecycle, from raw ingestion to final reporting and analytics.

### Supported Methodologies and Architectures

#### [**1. Kimball Methodology**](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/)

* Focused on **dimensional modeling**, this methodology organizes data into fact and dimension tables.
* Layers can represent stages such as **staging**, **transformation**, and **presentation**, ensuring a streamlined ETL process.
* Enables fast query performance, designed for business intelligence and reporting.

#### [**2. Medallion Architecture**](https://learn.microsoft.com/en-us/training/modules/describe-medallion-architecture/2-describe-medallion-architecture)

* Based on a **tiered structure** to process and refine data progressively:
  * **Bronze Layer**: Raw, unprocessed data ingestion.
  * **Silver Layer**: Cleaned and transformed data ready for analysis.
  * **Gold Layer**: Aggregated and optimized data for business reporting.
* Facilitates incremental data processing and ensures clear data lineage.

#### [**3. Data Vault 2.0**](https://datavaultalliance.com/data-vault-2-0-model/)

* Aimed at **flexible and scalable modeling** for large-scale data integration.
* Layers typically include:
  * **Raw Vault**: Ingested data in its raw, immutable form.
  * **Business Vault**: Applied business rules for enriched and transformed data.
  * **Information Mart**: Data structured for specific reporting needs.
* Supports agile development with a focus on historical tracking and auditability.

#### &#x34;**. Mixed modeling**



<mark style="background-color:orange;">Include mixed model --> check</mark>&#x20;

#### Key Features for Layer Management in AnalyticsCreator

* **Customization**: Define layers to fit your project’s specific requirements, whether it's raw data processing, transformation, or reporting.
* **Metadata-Driven Approach**: Automatically generate schemas and structures for each layer based on your selected methodology.
* **Data Flow Automation**: Leverage predefined transformations and scripts to ensure seamless data movement between layers.
* **Flexibility**: Combine methodologies, such as using a Medallion structure for staging and a Kimball model for reporting layers.

AnalyticsCreator robust archtechure allows you the freedom to choose any modeling approach you feell confortable with based on your project requirements, organizational goals, and preferences.

[This flexibility ensures that your Data Warehouse can be tailored to meet your specific needs while leveraging best practices.](https://www.analyticscreator.com/blog/best-practices-for-choosing-a-data-modeling-technique-for-your-data-warehouse)

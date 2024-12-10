# Layers

### Layers in a Data Warehouse

In a data warehouse, layers are a crucial aspect of its logical structure. Users have the ability to define a variety of layers which serve different purposes. Here, we will delve into the five primary types of layers typically used in a data warehouse architecture, explaining their functions and how they interconnect with each other.

#### 1. Source Layer (SRC)

This layer acts as the foundational logical data layer which includes external data sources. Even though the Source Layer itself is not a part of the data warehouse, it plays a critical role as the starting point where data enters the system. It serves as a collection pool for external data which is intended for use in the warehouse. Notably, within this layer, you cannot generate tables or execute transformations.

#### 2. Staging Layer (IMP)

Often referred to as the Import Layer, this is where data from the Source Layer is brought into tables and structured for entry into the warehouse environment. The Staging Layer is dynamic, regularly overwritten with new data imports to maintain current datasets.

#### 3. Persisted Staging Layer (STG)

The Persisted Staging Layer is where the ongoing commitment to data begins. Data arriving from the Import Layer is stored and historicized in this stage. As the primary data layer of the warehouse, the Staging Layer ensures that data becomes reliable and verifiable for further processes.

#### 4. Transformation Layer (TRN)

Operations performed here are to further manipulate and refine the content made available by the Staging Layer. Although considered optional, the Transformation Layer enables additional processing to facilitate data quality and consistency before data progresses to subsequent phases.

#### 5. Data Warehouse Layer (DWH)

Within the Data Warehouse Layer, data undergoes organization into complex structures, transformed into facts and dimensions required for analytical purposes. This layer forms the core repository where processed data is organized for efficient retrieval and analysis.

#### 6. Data Mart Layer (DM)

The Data Mart Layer is positioned as an interface layer, representing a focal point for end-user access. Data is structured logically, often adopting a star schema with fact tables and dimensions, effectively supporting user queries and reports.



The strategic arrangement of these layers within a data warehouse is organized conventionally in the sequence: SRC – IMP – STG – TRN – DWH – DM.  As presented on the image bellow, from left to right.

{% embed url="https://www.canva.com/design/DAGY03aazHw/sA6ZbaTvhw6IJXE9-E9fWg/view?utlId=hbb2a67e030&utm_campaign=designshare&utm_content=DAGY03aazHw&utm_medium=link2&utm_source=uniquelinks" %}

This configuration facilitates an efficient workflow, transforming raw data sources into insightful, user-accessible information.&#x20;

Each layer plays a distinct role in meeting the comprehensive objectives of warehousing, encapsulating data journey from acquisition to end-user presentation.

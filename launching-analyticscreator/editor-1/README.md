---
noIndex: true
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# AnalyticsCreator Repository

### What is AnalyticsCreator Repository

<mark style="background-color:orange;">AnalyticsCreator Repository is where you store your database metadata information.</mark>&#x20;

<mark style="background-color:orange;">Ask Dimitry for a better definition</mark>

Repository is organized into folders, and each folder represents a Data Warehouse artifact or a database object.

Not all items into the repository need to be used

#### **Data warehouse**

* <mark style="background-color:orange;">**Connectors:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">These are likely tools or configurations for connecting to different data sources.</mark>
* <mark style="background-color:orange;">**Layers:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">This could refer to a hierarchical structure for organizing data.</mark>
* <mark style="background-color:orange;">**Packages:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">These might be collections of related objects or configurations.</mark>
* <mark style="background-color:orange;">**Indexes:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Data structures used to improve query performance.</mark>
* <mark style="background-color:orange;">**Roles:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Permissions and access controls for different users.</mark>
* <mark style="background-color:orange;">**Galaxies, Hierarchies, Partitions, and Parameters:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">These terms are often used in data modeling and management contexts.</mark>
* <mark style="background-color:orange;">**Macros and Scripts:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Reusable code snippets for common data transformations and operations.</mark>
* <mark style="background-color:orange;">**Object Scripts:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Scripts specifically related to data objects.</mark>
* <mark style="background-color:orange;">**Filters:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Mechanisms for filtering and selecting data.</mark>
* <mark style="background-color:orange;">**Predefined Transformations:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Built-in transformations for data processing.</mark>
* <mark style="background-color:orange;">**Snapshots:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Copies or versions of data at specific points in time.</mark>
* <mark style="background-color:orange;">**Deployments:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Processes for deploying data warehouse changes.</mark>
* <mark style="background-color:orange;">**Groups:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Groupings of related objects or users.</mark>
* <mark style="background-color:orange;">**Models:**</mark> <mark style="background-color:orange;"></mark><mark style="background-color:orange;">Data models that define the structure and relationships of data</mark>.

**Types of repositories**

Repository could be in stored and take it in tree forms:

1. SQL Server repository
2. Local file
3. AnalyticsCreator Cloud

Both are actually MS SQL Server databases (no other software is installed) with a predefined schema to keep all AnalyticsCreator data. \







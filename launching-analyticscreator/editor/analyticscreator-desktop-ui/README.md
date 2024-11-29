---
description: >-
  The AnalyticsCreator interface provides a straightforward layout to help you
  navigate and configure your Data Ware projects efficiently. Below is an
  overview of its main components for quick reference
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

# AnalyticsCreator Desktop UI

AnalyticsCreator Desktop user interface consists of three main elements:

1. **Ribbon** that provides options for current view and selected element
2. **Data Warehouse(DWH) explorer** that enables navigation of repository
3. [**Work Area** ](working-area-elements.md)that's display details of the selected feature in repository explorer
4. **Menu & Ribbon** that provides options as _Home, Sources, DWH, Data Mart, ETL, Deployment_, and _Help_. These provide access to various tools and features.
5. **Navigation Pane** This area remains consistent and allows for navigation through the data warehouse's components, such as connectors, layers, packages, and transformations. Selecting an item here often updates the working area to reflect the selected object or process.
6. **Work Area** This changes depending on the task being carried out. To start it displays the data lineage diagram, showing the end-to-end pipeline from source systems to the star schema for analytics. When performing other tasks (e.g., configuring connectors, editing ETL scripts, or deploying models), this area transforms into a context-specific workspace to focus on the active task. The visual elements in the data lineage diagram (boxes, connectors, and icons) are clickable and editable, enabling users to interact directly with the components. For example, clicking a table might open its properties or transformation details in the working area.

{% embed url="https://www.canva.com/design/DAGXgnaC6Xg/Gf6kiFMUypUbQz7NxtR6AQ/view?utm_campaign=designshare&utm_content=DAGXgnaC6Xg&utm_medium=link&utm_source=editor" %}

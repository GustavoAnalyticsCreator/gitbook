---
noIndex: true
icon: camera-retro
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

# Snapshots

**Breadcrumb:**\
Toolbar → DWH → Snapshot\
Navigation Tree → Snapshots → Add Snapshot\
Navigation Tree → Snapshots → Snapshot → Edit Snapshot

***

#### **What is a Snapshot?**

A **Snapshot** in AnalyticsCreator represents a static copy of data at a specific point in time. Snapshots are primarily used for tracking historical changes, creating point-in-time comparisons, or maintaining data states for auditing and reporting purposes.

***

#### **How to Add a Snapshot**

**1. Create a New Snapshot**

1. In the **navigation tree**, click on **Snapshots** and select **Add Snapshot**.
2. In the **Snapshot name** box, enter a descriptive name for the snapshot.
3. In the **Description** box, provide a detailed explanation of the snapshot’s purpose or context.
4. In the **SQL** box, type or paste the SQL query defining the data to be included in the snapshot.
5. Click the **Save** button to create the snapshot.

***

#### **Snapshot Groups**

Snapshot groups allow you to organize and manage multiple snapshots under a single grouping. This is particularly useful for maintaining logical organization and simplifying access to related snapshots.

**1. Create a Snapshot Group**

**Breadcrumb:**\
Navigation Tree → Snapshots → Snapshot Groups → Add Snapshot Group

1. In the **navigation tree**, right-click on **Snapshot Groups** and select **Add Snapshot Group**.
2. In the **Group name** box, type the name of the group.
3. In the **Description** box, provide a description for the snapshot group.
4. In the column **Snapshot**, select the snapshots to include in this group.
5. Click the **Save** button to finalize the group.

***

#### **Managing Snapshots**

* **List and Search Snapshots**: View all snapshots in the repository using the **Snapshots** navigation tree.
* **Edit Snapshots**: Modify an existing snapshot’s name, description, or SQL logic by selecting it and clicking **Edit Snapshot**.
* **Delete Snapshots**: Remove obsolete snapshots to maintain repository cleanliness.

Refer to the List and Search Objects guide for detailed steps on managing snapshots.

***

#### **Best Practices for Using Snapshots**

1. **Purpose-Driven Design**: Clearly define the purpose of each snapshot, such as tracking historical changes or creating audit records.
2. **Optimize SQL Queries**: Use efficient SQL queries to minimize performance impact when creating snapshots.
3. **Organize with Groups**: Use snapshot groups to manage and logically categorize snapshots for better accessibility.
4. **Regular Maintenance**: Periodically review and clean up old snapshots to reduce clutter and maintain performance.

Snapshots are a powerful feature in AnalyticsCreator, enabling you to capture and preserve critical data points for historical analysis and compliance reporting. By leveraging snapshots effectively, you can ensure a robust and reliable data tracking system.


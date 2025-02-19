# Object membership

AnalyticsCreator objects, such as sources, tables, and transformations, can be organized into groups. These groups allow users to:

* Display only the objects belonging to a specific group.
* Enable or disable objects in the workflow based on their group membership.

To add an object to a group, select **"Object Groups"** from the object's context menu, as shown in the image below.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



The **Group Window** will open, allowing you to manage group memberships.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

**Creating and Managing Groups**

\
To create a new group, enter a group name and check the **"Member"** checkbox.\
To add all objects dependent on the selected object to the group, select the **"Inherit Successors"** checkbox.\
To add all objects that the selected object depends on to the group, select the **"Inherit Predecessors"** checkbox.\
To create SQL scripts for turning group objects on and off in the workflow package, select the **"Create Workflow"** checkbox. Three SQL scripts can be created:

1. **SSIS\_Configuration Complete Script**: Contains the workflow configuration, disabling all objects except those that belong to the group.
2. **SSIS\_Configuration Enable Script**: Contains the workflow configuration, enabling objects that belong to the group.
3. **SSIS\_Configuration Disable Script**: Contains the workflow configuration, disabling objects that belong to the group.

There is the group membership of one object, as shown in the image below:

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

This object belongs to several groups. The **"Inherited"** flag indicates that the group membership was inherited from a dependent or depending object. This object is displayed in the **"Inherited from Object"** column.\
To disable the "inherited" membership, select the **"Exclude"** checkbox.

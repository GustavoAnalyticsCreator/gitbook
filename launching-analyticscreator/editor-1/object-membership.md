# Object membership

AnalyticsCreator objects, such as sources, tables, and transformations, can be organized into groups. These groups allow for displaying only the objects belonging to a specific group or enabling and disabling objects in the workflow based on group membership. To add an object to a group, select **“Object Groups”** from the object’s context menu

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



The group window will be opened

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

To create a new group please enter a group name and check the “Member” check box.

To add to the group all objects depending from the selected object please select  the “Inherit successors” checkbox.

To add to the group all objects which the selected object depends on please select  the “Inherit predecessors” checkbox.

To create the SQL scripts turning on and of the group objects in the workflow package please select the “Create workflow” checkbox. Three are 3 SQL scripts which can be created:

1. The “SSIS\_Configuration complete script” contains the workflow configuration disabling all objects except the objects which belong to the group.
2. The “SSIS\_Configuration enable script” contains the workflow configuration enabling objects which belong to the group.
3. The “SSIS\_Configuration enable script” contains the workflow configuration disabling objects which belong to the group.

There is the group membership of one object:

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

This object belongs to some groups. The flag “inherited” shows that the group membership was inherit from the depending or dependent object. This object you can see in the column “Inherited from object”.

To turn of the “inherited” membership please select the checkbox “exclude”.

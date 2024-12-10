# Object membership

You can group AC objects (sources, tables and transformations) into groups. You can use groups to display only objects belong to specific group or to turn on and off in the workflow only objects belong to specific group. To add an object to the group select “Object groups” in object context menu: The group window will be opened

To create a new group please enter a group name and check the “Member” check box. To add to the group all objects depending from the selected object please select the “Inherit successors” checkbox. To add to the group all objects which the selected object depends on please select the “Inherit predecessors” checkbox. To create the SQL scripts turning on and of the group objects in the workflow package please select the “Create workflow” checkbox. Three are 3 SQL scripts which can be created: The “SSIS\_Configuration complete script” contains the workflow configuration disabling all objects except the objects which belong to the group. The “SSIS\_Configuration enable script” contains the workflow configuration enabling objects which belong to the group. The “SSIS\_Configuration enable script” contains the workflow configuration disabling objects which belong to the group.

There is the group membership of one object:

This object belongs to some groups. The flag “inherited” shows that the group membership was inherit from the depending or dependent object. This object the user can see in the column “Inherited from object”. To turn of the “inherited” membership please select the checkbox “exclude”.

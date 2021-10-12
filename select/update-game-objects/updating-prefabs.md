# Updating Prefabs

Prefabs can be [updated like any other game object](editor-selecting-objects.md), except they are edited separately from the scene and changes are applied to each instance of the prefab.

Trying to update the children of a prefab in a scene will give you this error:

![](<../../.gitbook/assets/image (102).png>)

## Accessing the Prefab Editor

There are a few ways to access the editor for a prefab object:

### **Through the Hierarchy Window**

Click on the arrow to the right of the parent object's name to edit the prefab.

![](<../../.gitbook/assets/image (100).png>)

### **Through the Project Window**

Double-click on the prefab to edit.

![](<../../.gitbook/assets/image (98).png>)

### **Through the Inspector Window**

Click on the Open Prefab button to edit the selected prefab.

![](<../../.gitbook/assets/image (103).png>)

## **The Prefab Editor**

When you are editing a prefab, the Hierarchy window shows the children objects and the Scene window shows a close up of the prefab with a solid background color.

![](<../../.gitbook/assets/image (105).png>)

Edit the game objects like you would any other game object.

Changes here will update all instances of the prefab when you click the back arrow in the Hierarchy window.

## Unpack a Prefab

Maybe you only want to change one of the instances and not all. 

You can "unpack" instances by right-clicking on the parent object in the prefab and clicking on an unpack option.

![](<../../.gitbook/assets/image (106).png>)

This will turn the prefab and its children gray, meaning they can be edited within the tab and without affecting other instances. 

{% hint style="warning" %}
Updating prefab assets will not update the unpacked version of the prefab.
{% endhint %}

{% content-ref url="../../create/create-prefabs.md" %}
[create-prefabs.md](../../create/create-prefabs.md)
{% endcontent-ref %}


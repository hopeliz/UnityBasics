# Parenting

## Overview

Parenting is where game objects can exist within other objects. The object containing other objects is the "parent" object and the objects within are "child" objects, referred to as "children."

![](<../../.gitbook/assets/image (80).png>)

In the example above:

* The game object "Fruit" is the parent of both "Banana" and "Peel"
* "Banana" is the parent of "Peel" and the child of "Fruit"
* "Peel" is the child of both "Fruit" and "Banana"

## **Behaviors**

Certain aspects applied to a parent object affect its children. The most common are transform controls (Translate, Rotate, and Scale), its active state, and visibility.

In the example above, if Fruit is moved or resized or hidden, it affects all the child objects the same way.

However, aspects affecting the object individually (scripts, mesh, colliders, etc.) do not change its child objects.

If Fruit had a script to trigger a noise, only that object creates the noise.

Changes to children remain with the individual object without affecting the parent object above it.

Moving the Banana object will affect the Peel, but not Fruit or any object outside of Banana.

## Local vs. Global Values

When a game object is created on its own, the Transform values are global values - its position, rotation, and scale in relation to the entire scene. Once you move the object to become a child of another object, the values shown change to local values - its position, rotation, and scale in relation to its parent. 

This is why sometimes, rotating child objects within the game scene looks funny. Be careful about changing values - especially scale - of parenting objects.

{% hint style="info" %}
To help avoid issues, be sure to "reset" or "zero out" new empty game objects by right-clicking on the Transform component in the Inspector window and clicking "reset."
{% endhint %}

{% hint style="danger" %}
When dragging objects, drag the parent object to take the children with it. Selecting the parent and children and dragging will remove the parent/child hierarchy.
{% endhint %}

## Handy Scripts

Here are some common scripts to access parenting features while the game is running:

### **Set the parent of an object**

```csharp
transform.parent = parentObject.transform;
```

and

```csharp
transform.SetParent(parentObject.transform);
```

### **Access a component of a parent object**

Below is an example of accessing the Collider of the parent object and putting it in the variable, "parentCollider."

```csharp
Collider parentCollider = transform.GetComponentInParent<Collider>();
```

### **Access a component of a child object**

Below is an example of accessing the Collider of a child object and putting it in the variable, "childCollider."

```csharp
Collider childCollider = transform.GetComponentInChildren<Collider>();
```

Usually, there will be multiple children, so the code to return or create a list or an array of components in child objects to access them individually, use transform.GetComponent**s**InChildren\<Component> then access them using an index value.

```csharp
Collider[] childColliders = transform.GetComponentsInChildren<Collider>();
```

## **Why Use This?**

**Organization**\
****Grouping similar objects can help you hide, move, etc. a certain type by manipulating one object.

**Tying Together Behavior**\
****A great example of this are games that use a camera that follows a character. One way to do this is to make the camera a child object of the character so when the character moves, the camera moves, maintaining its offset without extra coding.

**Easy Access**\
Similar to organizing, you can use a script to access only items inside a specific object instead of looking through all the game objects.

There are many other reasons to discover, but those are the top ones! 

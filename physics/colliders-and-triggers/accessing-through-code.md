# Accessing Colliders Through Scripts

## Overview

Colliders can be [accessed like any other component](../../select/components/accessing-attributes.md).

Example of storing a Collider component in a variable:

```csharp
public Collider thingCollider;
```

In the Inspector, the object with the script attached will have the component for the script and this property:

![](../../.gitbook/assets/image%20%28171%29.png)

You can click and drag an object with a collider into the field or click the circle target icon on the right to select from a list.

If you want to have collider of the object the script is attached to be stored, use this script in the Start\(\) function:

```csharp
thingCollider = gameObject.GetComponent<Collider>();
```

{% hint style="info" %}
Although the collider components are named "Box Collider" or "Capsule Collider" etc. in the editor, the component can be referenced as "Collider" in the script.
{% endhint %}

## Trigger Events When Touching / Stop Touching

Here is a script that runs code when objects touch or stop touching \(put this after the ending bracket of Update\(\) but before the ending bracket of the class\):

```csharp
public void OnCollisionEnter(Collision collision)
{
    if (collision.gameObject.tag == "Colliding Object")
    {
        // When something with the tag "Colliding Object" 
        // hits this object
        // Run this code on the first frame this is true
    }
}

public void OnCollisionStay(Collision collision)
{
    if (collision.gameObject.tag == "Colliding Object")
    {
        // When something with the tag "Colliding Object" 
        // continues to touch this object
        // Run this code each frame
    }
}

public void OnCollisionExit(Collision collision)
{
    if (collision.gameObject.tag == "Colliding Object")
    {
        // When something with the tag "Colliding Object" 
        // no longer touches this object
        // Run this code the first frame this is true
    }
}
```

In this example, the colliding object's tag is checked so the code only runs when that specific object\(s\) collide with the object this script is attached to. The if statements can be updated to look at the name, layer, etc. This if statement keeps the code from running when other objects collide or are inside the object.

## Trigger Events When Entering, Staying, and Exiting a "Trigger"

Here is a script that runs code when objects enter, stay, or exit a collider that has the Is Trigger checkbox checked  \(put this after the ending bracket of Update\(\) but before the ending bracket of the class\):

```csharp
public void OnTriggerEnter(Collider other)
{
    if (other.tag == "Entering Object")
    {
        // When something with the tag "Entering Object" 
        // enters this object's collider
        // Run this code on the first frame this is true
    }
}

public void OnTriggerEnter(Collider other)
{
    if (other.tag == "Entering Object")
    {
        // When something with the tag "Entering Object" 
        // continues to stay inside this object's collider
        // Run this code each frame
    }
}

public void OnTriggerEnter(Collider other)
{
    if (other.tag == "Entering Object")
    {
        // When something with the tag "Entering Object" 
        // exits this object's collider
        // Run this code the first frame this is true
    }
}
```

In this example, the entering object's tag is checked so the code only runs when that specific object\(s\) enter, stay, and exit the collider of the object this script is attached to. The if statements can be updated to look at the name, layer, etc. This if statement keeps the code from running when other objects are inside the object.

## Updating the Collider Component within the Script

You can update whether or not the collider is a trigger with this code:

```csharp
gameObject.GetComponent<Collider>().isTrigger = true;
```

## Related Links

{% page-ref page="../../select/components/accessing-attributes.md" %}




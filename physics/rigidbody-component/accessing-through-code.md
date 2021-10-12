# Accessing the Rigidbody Component Through Scripts

## Overview

Rigidbody components can be [accessed like any other component](../../select/components/accessing-attributes.md).

Example of storing the Rigidbody component in a variable:

```csharp
public Rigidbody thingRb;
```

In the Inspector, the object with the script attached will have the component for the script and this property:

![](<../../.gitbook/assets/image (173).png>)

You can click and drag an object with a Rigidbody component into the field or click the circle target icon on the right to select from a list.

If you want to have Rigidbody component of the object the script is attached to be stored, use this script in the Start() function:

```csharp
thingRb = gameObject.GetComponent<Rigidbody>();
```

## Commonly Accessed Properties

Here are some example scripts to access the properties:

```csharp
// Adds a force upward - great for making things jump (add a modifier)
thingRb.AddForce(new Vector3(0, 1.0F, 0));

// Turns off gravity for the item
thingRb.useGravity = false;

// Makes the item kinematic
thingRb.isKinematic = true;

// Update's the object's mass
thingRb.mass = 10;

// Resets the velocity and angular velocity - good for stopping moving objects
thingRb.velocity = new Vector3(0, 0, 0);
thingRb.angularVelocity = new Vector3(0, 0, 0);
```

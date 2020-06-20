# Updating Rotation Through Script Code

## Overview

When the game is running, you will not be able to rotate objects as you can within the editor, so one way to update the angle an object is facing is by updating the object's Euler angles.

The Euler angles are stored in a vector3 variable with read-only parts, so you cannot update just one axis at a time through transform.eulerAngles.y = 90.0F or something similar. You need to use the keyword new followed by a complete Vector3. Here's an example:

```csharp
// Rotates the object directly to 90 degrees right
transform.eulerAngles = new Vector3(0, 90.0F, 0);
```

Here, the object rotates right by 90 degrees, making it face right. If it starts at \(0,0,0\), it appears to jump to facing right in one frame and stays in that direction until it's rotated again.

## Rotating Objects by Updating the Euler Angles Smoothly Through Code

{% hint style="warning" %}
Avoid using Transform.rotation. It is a Quaternion and it takes four coordinates that are different than the Euler angles shown in the Transform component.
{% endhint %}

**Example codes:**

* _Each example should be placed within the Update\(\) or FixedUpdate\(\) function so that it runs once per frame_
* _Each example rotates the object it is attached to in the positive direction of the y-axis \(clockwise\)_

```csharp
transform.eulerAngles += new Vector3(0, 1.0F, 0) * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its rotation in Euler angles
2. Uses the += shortcut to add values to itself
3. _new Vector3\(float x, float y, float z\)_ is a way to tell it to add the matching variables
4. _Time.deltaTime_ adjusts for varying computer [speeds](../controlling-speed.md)

```csharp
transform.eulerAngles += Vector3.up * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its rotation in Euler angles
2. Uses the += shortcut to add values to itself
3. _Vector3.up_ is a [shortcut](../handy-transform-shortcuts.md) for Vector3\(0.0F, 1.0F, 0.0F\); Up is used here because we are spinning it on its y-axis "rod"
4. _Time.deltaTime_ adjusts for varying computer speeds


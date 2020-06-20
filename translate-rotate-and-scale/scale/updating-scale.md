# Updating Scale Through Script Code

## Overview

When the game is running, you will not be able to resize objects as you can within the editor, so one way to update the size or scale an object is by updating the object's scale in game units.

The scale values are stored in a vector3 variable with read-only parts, so you cannot update just one axis at a time through transform.localScale.y = 10.0F or something similar. You need to use the keyword new followed by a complete Vector3. Here's an example:

```csharp
// Makes the object 10 game units tall
transform.localScale = new Vector3(0, 10.0F, 0);
```

Here, the game object becomes 10 game units tall. If it starts at 1 x 1 x 1, it appears to jump to that size in one frame and stays at that size until it's resized again.

## Resize Objects by Updating the Local Scale Smoothly Through Code

{% hint style="warning" %}
Avoid using Transform.lossyScale. It controls the global scale of an object, so child objects can be skewed.
{% endhint %}

**Example codes:**

* _Each example should be placed within the Update\(\) or FixedUpdate\(\) function so that it runs once per frame_
* _Each example grows the object it is attached to along the y-axis \(gets taller from the center\)_

```csharp
transform.localScale += new Vector3(0, 1.0F, 0) * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its local scale in game units
2. Uses the += shortcut to add values to itself
3. _new Vector3\(float x, float y, float z\)_ is a way to tell it to add the matching variables
4. _Time.deltaTime_ adjusts for varying computer [speeds](../controlling-speed.md)

```csharp
transform.localScale += Vector3.up * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its local scale in game units
2. Uses the += shortcut to add values to itself
3. _Vector3.up_ is a [shortcut](../handy-transform-shortcuts.md) for Vector3\(0.0F, 1.0F, 0.0F\);
4. _Time.deltaTime_ adjusts for varying computer speeds


# Updating Position Through Script Code

When the game is running, you will not be able to move around objects as you can within the editor, so one way to move objects smoothly is by updating the object's position coordinates.

The position is a vector3 variable with read-only parts, so you cannot update just one axis at a time through transform.position.y = 1.0F or something similar. You need to use the keyword new followed by a complete Vector3. Here's an example:

```csharp
// Moves the object directly to (1,0,0)
transform.postion = new Vector3(1.0F, 0.0F, 0.0F);
```

Here, if the object moves to \(1,0,0\). If it starts at \(0,0,0\), it appears to jump to the right in one frame and stays there until moved again

### Moving Objects by Updating the Position Smoothly Through Code

{% hint style="info" %}
Moving objects this way is generally OK, but you might run into issues if you use it for player movement. For those situations, use Transform.Translate\(\) instead.
{% endhint %}

**Example codes:**

* _Each example should be placed within the Update\(\) or FixedUpdate\(\) function so that it runs once per frame_
* _Each example moves the object it is attached to in the positive direction of the x-axis \(right\)_

```csharp
transform.postion += new Vector3(1.0F, 0.0F, 0.0F) * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its position
2. Uses the += shortcut to add values to itself
3. _new Vector3\(float x, float y, float z\)_ is a way to tell it to add the matching variables
4. _Time.deltaTime_ adjusts for varying computer [speeds](../controlling-speed.md)

```csharp
transform.postion += Vector3.right * Time.deltaTime;
```

The code above:

1. Accesses the object's transform and then its position
2. Uses the += shortcut to add values to itself
3. _Vector3.right_ is a [shortcut](../handy-transform-shortcuts.md) for Vector3\(1.0F, 0.0F, 0.0F\);
4. _Time.deltaTime_ adjusts for varying computer speeds


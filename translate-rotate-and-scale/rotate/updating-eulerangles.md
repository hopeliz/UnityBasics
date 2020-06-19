# Updating EulerAngles Through Script Code

### Rotating Objects by Updating the Euler Angles Through Code

**Example codes:**

* _These examples use a public global GameObject variable called "cube"._
* _Each example should be placed within the Update\(\) or FixedUpdate\(\) function so that it runs once per frame_
* _Each example rotates "cube" in the positive end of the y-axis \(clockwise\)_

```csharp
cube.transform.eulerAngles += new Vector3(0, 1.0F, 0.0F) * Time.deltaTime;
```

The code above:

1. Accesses the cube's transform and then its rotation as Euler angles
   * The Euler angles are stored in a Vector3 type
2. Uses the += shortcut to add values to itself
3. _new Vector3\(float x, float y, float z\)_ is a way to tell it to add the matching variables
4. _Time.deltaTime_ adjusts for varying computer speeds

```csharp
cube.transform.eulerAngles += nVector3.up * Time.deltaTime;
```

The code above:

1. Accesses the cube's transform and then it's position
   * The position is a Vector3 type
2. Uses the += shortcut to add values to itself
3. _Vector3.right_ is a shortcut for Vector3\(1.0F, 0.0F, 0.0F\);
4. _Time.deltaTime_ adjusts for varying computer speeds


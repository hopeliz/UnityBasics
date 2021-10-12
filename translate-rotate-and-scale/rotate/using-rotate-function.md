# Using the Transform.Rotate() Function

## Overview

When the game is running, you will not be able to rotate objects as you can within the editor, so one way to rotate objects smoothly is with the Transform.Rotate() function.

It updates the Euler angles of the object and can be used incrementally to make the movement appear smooth.

Here is an example of a player rotate script using Transform.Rotate() to rotate a character when a key is pressed:

```csharp
using UnityEngine;

public class PlayerRotate : MonoBehaviour
{
    void Update()
    {
        // Press Left Arrow to rotate the object left/counter-clockwise
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Rotate(0, -1.0F, 0);
        }

        // Press Right Arrow to move the object right/clockwise
        if (Input.GetKey(KeyCode.RightArrow))
        {
            transform.Rotate(0, 1.0F, 0);
        }
    }
}
```

## Controlling Speed

Commands in the Update() function run once per frame, meaning speed changes based on the computer's frame rate.

Multiplying by Time.deltaTime adjusts the speed to be about the same, even with different frame rates. Adding a speed variable helps you adjust the speed it moves.

Here's the same example with these adjustments:

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    public float moveSpeed = 10;

    void Update()
    {
        // Press Left Arrow to rotate the object left/counter-clockwise
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Rotate(new Vector3(0, -1.0F, 0) * moveSpeed * Time.deltaTime);
        }

        // Press Right Arrow to move the object right/clockwise
        if (Input.GetKey(KeyCode.RightArrow))
        {
            transform.Rotate(new Vector3(0, 1.0F, 0) * moveSpeed * Time.deltaTime);
        }
    }
}
```

## Vector3 Shortcuts

Instead of remembering and typing a long piece of code like the one below:

```csharp
new Vector3(0, 1.0, 0)
```

Unity has short cuts like this one that you only have to remember a direction:

```csharp
Vector3.up
```

Here's the same example with these shortcuts:

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    public float moveSpeed = 10;
    
    void Update()
    {
        // Press Left Arrow to rotate the object left/counter-clockwise
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Rotate(Vector3.down * moveSpeed * Time.deltaTime);
        }

        // Press Right Arrow to move the object right/clockwise
        if (Input.GetKey(KeyCode.RightArrow))
        {
            transform.Rotate(Vector3.up  * moveSpeed * Time.deltaTime);
        }
    }
}
```

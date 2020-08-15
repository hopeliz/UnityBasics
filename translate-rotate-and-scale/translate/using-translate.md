# Using the Transform.Translate\(\) Function

## Overview

When the game is running, you will not be able to move around objects as you can within the editor, so one way to move objects smoothly is with the Transform.Translate\(\) function.

It updates the position of the object and can be used incrementally to make the movement appear smooth.

Here is an example of a player move script using Transform.Translate\(\) to move a character when a key is pressed:

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    void Update()
    {
        // Press W to move the object forward
        if (Input.GetKey(KeyCode.W))
        {
            transform.Translate(0, 0, 1.0F);
        }

        // Press A to move the object to the left
        if (Input.GetKey(KeyCode.A))
        {
            transform.Translate(-1.0F, 0, 0);
        }

        // Press S to move the object backward
        if (Input.GetKey(KeyCode.S))
        {
            transform.Translate(0, 0, -1.0F);
        }

        // Press D to move the object to the right
        if (Input.GetKey(KeyCode.D))
        {
            transform.Translate(1.0F, 0, 0);
        }
    }
}
```

## Controlling Speed

Commands in the Update\(\) function run once per frame, meaning speed changes based on the computer's frame rate.

Multiplying by Time.deltaTime adjusts the speed to be about the same, even with different frame rates. Adding a speed variable helps you adjust the speed it moves.

Here's the same example with these adjustments:

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    public float moveSpeed = 10;
    
    void Update()
    {
        // Press W to move the object forward
        if (Input.GetKey(KeyCode.W))
        {
            transform.Translate(new Vector3(0, 0, 1.0F) * moveSpeed * Time.deltaTime);
        }
        
        // Press A to move the object to the left
        if (Input.GetKey(KeyCode.A))
        {
            transform.Translate(new Vector3(-1.0F, 0, 1.0F) * moveSpeed * Time.deltaTime);
        }

        // Press S to move the object backward
        if (Input.GetKey(KeyCode.S))
        {
            transform.Translate(new Vector3(0, 0, -1.0F) * moveSpeed * Time.deltaTime);
        }

        // Press D to move the object to the right
        if (Input.GetKey(KeyCode.D))
        {
            transform.Translate(new Vector3(-1.0F, 0, 0) * moveSpeed * Time.deltaTime);
        }
    }
}
```

After adding the script to an object, this is how it will appear in the Inspector window when the object is selected. The Move Speed will default to what is in the script and you can update it through the Inspector through typing in a value or clicking and dragging left and right over the "Move Speed" label.

![](../../.gitbook/assets/image%20%28174%29.png)

## Vector3 Shortcuts

Instead of remembering and typing a long piece of code like the one below:

```csharp
new Vector3(0, 1.0, 0)
```

Unity has [shortcuts](../handy-transform-shortcuts.md) like this one that you only have to remember a direction:

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
        // Press W to move the object forward
        if (Input.GetKey(KeyCode.W))
        {
            transform.Translate(Vector3.forward * moveSpeed * Time.deltaTime);
        }

        // Press A to move the object to the left
        if (Input.GetKey(KeyCode.A))
        {
            transform.Translate(Vector3.left * moveSpeed * Time.deltaTime);
        }

        // Press S to move the object backward
        if (Input.GetKey(KeyCode.S))
        {
            transform.Translate(Vector3.back * moveSpeed * Time.deltaTime);
        }

        // Press D to move the object to the right
        if (Input.GetKey(KeyCode.D))
        {
            transform.Translate(Vector3.right * moveSpeed * Time.deltaTime);
        }
    }
}
```




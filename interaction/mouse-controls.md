# Mouse Controls

Use a script and the **Input** class to determine what mouse button is pressed:

### Types of Mouse Button Input

**Input.GetMouseButton() **- Returns true each frame the button within the parentheses is pressed. This is great for clicking and dragging items and drawing.

**Input.GetMouseButtonDown()** - Returns true only on the first frame the button within the parentheses is pressed. This is best for switches and buttons.

**Input.GetMouseButtonUp()** - Returns true on the frame the button within the parentheses is released.

Inside the parentheses, you want to use an integer that represents the mouse button:

**0** - Left Mouse Button

**1** - Right Mouse Button

**2** - Center / Pressing the Scroll Button

Since the code is to see if a key is pressed or not, the code is generally used in if statements.

Examples:

```csharp
if (Input.GetMouseButton(0))
{
     // Something to do when the left mouse button is held down
}

if (Input.GetMouseButtonDown(1))
{
     // Something to do when the player right-clicks
}
```

{% hint style="info" %}
**Common Issue:** The object that should continuously move only moves a tiny bit and only when the player continues to tap the mouse button.\
\
**Solution: **You might be using GetMouseButtonDown() which only runs for one frame. Try using GetMouseButton() instead.
{% endhint %}

### Using the Input Manager

If you set up the Input Manager, track mouse movement with Input.GetAxis("Mouse X") and Input.GetAxis("Mouse Y").

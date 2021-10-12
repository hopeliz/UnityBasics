# Keyboard Controls

Use a script and the **Input** class to determine what key is pressed on the keyboard:

### Types of Direct Keyboard Input

**Input.GetKey() **- Returns true each frame the key within the parentheses is pressed. This is great for moving objects.

**Input.GetKeyDown()** - Returns true only on the first frame the key within the parentheses is pressed. This is best for switches and buttons.

**Input.GetKeyUp()** - Returns true on the frame the key within the parentheses is released.

Inside the parentheses, you want to use the **KeyCode** class to access the key you want.

Since the code is to see if a key is pressed or not, the code is generally used in if statements.

Here is an example of basic player movement code added into a "PlayerMotor.cs" script attached to a player game object:

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    public float moveSpeed = 10;
    public float jumpHeight = 200;
    
    void Update()
    {
        if (Input.GetKey(KeyCode.W))
        {
            transform.Translate(Vector3.forward * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.A))
        {
            transform.Translate(Vector3.left * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.S))
        {
            transform.Translate(Vector3.back * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.D))
        {
            transform.Translate(Vector3.right * moveSpeed * Time.deltaTime);
        }
        
        if (Input.GetKeyDown(KeyCode.Space)) {
            transform.GetComponent<Rigidbody>().AddForce(Vector3.up * jumpHeight);
        }
    }
}
```

{% hint style="info" %}
**Common Issue:** The object that should continuously move only moves a tiny bit and only when the player continues to tap the key.\
\
**Solution: **You might be using GetKeyDown() which only runs for one frame. Try using GetKey() instead.
{% endhint %}

### Using the Input Manager

If you set up the Input Manager, the following is an example that can be used in place of the code above. It is better to use the Input Manager axes if you plan to have the player be able to change the controls.

```csharp
using UnityEngine;

public class PlayerMotor : MonoBehaviour
{
    public float moveSpeed = 10;
    public float jumpHeight = 200;
    
    void Update()
    {
        if (Input.GetAxis("Vertical") > 0)
        {
            transform.Translate(Vector3.forward * moveSpeed * Time.deltaTime);
        }

        if (Input.GetAxis("Horizontal") < 0)
        {
            transform.Translate(Vector3.left * moveSpeed * Time.deltaTime);
        }

        if (Input.GetAxis("Vertical") < 0)
        {
            transform.Translate(Vector3.back * moveSpeed * Time.deltaTime);
        }

        if (Input.GetAxis("Horizontal") > 0)
        {
            transform.Translate(Vector3.right * moveSpeed * Time.deltaTime);
        }

        if (Input.GetButtonDown("Jump")) {
            transform.GetComponent<Rigidbody>().AddForce(Vector3.up * jumpHeight);
        }
    }
}
```


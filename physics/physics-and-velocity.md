# Common Issues: Physics and Velocity

**Issue:**

When using a script to move or reposition an already moving object with a Rigidbody component, the object continues to move.

**Solution:**

The object maintains velocity even when the position is updated. In the script, update the velocity and angular velocity to stop unwanted movement:

```csharp
GetComponent<Rigidbody>().velocity = new Vector3(0, 0, 0);
GetComponent<Rigidbody>().angularVelocity = new Vector3(0, 0, 0);
```

Since this is a lot to type repeatedly, consider condensing it into its own function.

After the end bracket for the Update() function, add this function:

```csharp
public void ResetVelocity()
{
    Rigidbody rb = GetComponent<Rigidbody>();

    Vector3 zeroV = new Vector3(0, 0, 0);

    rb.velocity = zeroV;
    rb.angularVelocity = zeroV;
}
```

Now, when you want to reset the velocity on the object the script is attached to, use ResetVelocity().

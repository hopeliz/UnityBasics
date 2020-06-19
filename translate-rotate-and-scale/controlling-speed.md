# Controlling Speed

Different computers run at different speeds. The best way to account for this is to always multiply your transform code by Time.deltaTime.

Speed can be stored in its own variable to update with ease and is generally multiplied or divided when updating the transform.

Examples:

```csharp
// Define public global variables
// These will appear in the Inspector tab
public float speed = 3.5F;
public Vector3 destination;

// Only runs once
void Start() {

    // Initialize the destination location
    destination = new Vector3(20.0, 0, 0);
}

// Runs each frame
void Update() {

    // Example of updating position
    cube.transform.position += new Vector3(1.0F, 0, 0) * speed * Time.deltaTime;

    // Example of using Translate()
    cube.Translate(new Vector3(1.0F, 0, 0)) * speed * Time.deltaTime;

    // Example of using Vector3.Lerp()
    cube.transform.position = Vector3.Lerp(cube.transform.position, destination, speed * Time.deltaTime);

}
```


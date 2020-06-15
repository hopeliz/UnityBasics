# Disabling and Removing Components During Game Play

You won't have access to the checkbox and menus in the editor while the game is playing, but you might want to turn on and off or remove components.

### **Enabling and Disabling Components**

In the examples below, the following variables are used:

```csharp
public GameObject thing;
public Transform thingTransform;
```

Use the boolean value **.enable** or turn on components.

Example of turning on the collider on a game object:

```csharp
thing.GetComponent<Collider>().enabled = true;
```

Example of turning off the collider on a game object:

```csharp
thing.GetComponent<Collider>().enabled = false;
```

### Removing Components

Use the Destroy\(\) function to remove components. Go to the link below for more information.

{% page-ref page="../delete-game-objects/destroy-function.md" %}

### Avoiding Errors

You will get an error if you try to enable, disable, or remove component that is not there.

You can check to see if an component is there by using this script.

Example of checking for a rigidbody component:

```csharp
if (thing.GetComponent<Rigidbody>() != null)
{
    // There is a Rigidbody component
}
```

### Related links

{% page-ref page="../../select/components/accessing-attributes.md" %}




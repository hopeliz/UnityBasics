# Disabling and Removing Components During Gameplay

You won't have access to the checkbox and menus in the editor while the game is playing, but you might want to turn on and off or remove components.

## **Enabling and Disabling Components**

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

## Removing Components

Use the Destroy() function to remove components. Go to the link below for more information.

{% content-ref url="../delete-game-objects/destroy-function.md" %}
[destroy-function.md](../delete-game-objects/destroy-function.md)
{% endcontent-ref %}

## Avoiding Errors

You will get an error if you try to enable, disable, or remove a component that is not there.

You can check to see if a component is there by using this script.

Example of checking for a Rigidbody component:

```csharp
if (thing.GetComponent<Rigidbody>() != null)
{
    // There is a Rigidbody component
}
```

{% content-ref url="../../select/components/accessing-attributes.md" %}
[accessing-attributes.md](../../select/components/accessing-attributes.md)
{% endcontent-ref %}

{% content-ref url="../../create/create-scripts/custom-components-and-scripts.md" %}
[custom-components-and-scripts.md](../../create/create-scripts/custom-components-and-scripts.md)
{% endcontent-ref %}


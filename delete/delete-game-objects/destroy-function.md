# Using the Destroy() Function

Having too many items in a game could slow down the computer and its frame rate. This is especially apparent in games where objects are created during gameplay.

## The Destroy() Function

To remove a game object or components of a game object, use the Destroy() function.

In the examples below, the following variables are used:

```csharp
public GameObject thing;
public Transform thingTransform;
```

Example of deleting a game object:

```csharp
Destroy(thing);
```

Example of deleting a game object of a transform:

```csharp
Destroy(thingTransform.gameObject);
```

The Destroy() function can also delete components (colliders, Rigidbody, scripts, etc.).

Example of deleting a Rigidbody component on a game object:

```csharp
Destroy(thing.GetComponent<Rigidbody>());
```

## Self-Destruction

You can destroy the object the script is attached to. This is a great way of controlling prefabs that need to delete themselves.

Use this code:

```csharp
Destroy(gameObject);
```

{% hint style="danger" %}
Deleting parent objects will delete their child objects. Child objects can be moved to another parent if needed. Read more about [Parenting](../../create/create-game-objects/parenting.md).
{% endhint %}

## Avoiding Errors

You will get an error if you try to remove an object or component that is not there.

You can check to see if an object or component is there by using this script.

Example of checking if a variable has been assigned and if the associated game object exists:

```csharp
if (thing != null)
{
     // There is an object assigned to the variable thing
}
```

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

{% content-ref url="../../coding-basics/intro-to-scripts.md" %}
[intro-to-scripts.md](../../coding-basics/intro-to-scripts.md)
{% endcontent-ref %}


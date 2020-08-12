# Spawning Objects

## Using the Instantiate\(\) function to Spawn Objects

There are 5 different ways \(currently\) to use the Instantiate\(\) function to create or "spawn" pre-made objects.

The most basic use of it is as follows:

Define the gameObject within the script within the class, but before the Start\(\) function:

_In this example, the object is named "thing"._

```csharp
public GameObject thing;
```

Then, in your script where you want to create or "spawn" the object add this:

```csharp
Instantiate(thing);
```

Spawned objects with the simplest version of Instantiate\(\) will spawn with the transform, components, and settings as the original object.

You can put this into a variable:

```csharp
GameObject copiedThing = Instantiate(thing);
```

This is helpful when you want to create several in a loop, changing copies individually.

Many game artists use the Instantiate\(\) function with [prefabs](../create-prefabs.md) so they don't need to spawn each part individually.

{% hint style="info" %}
Prefabs for the Instantiate\(\) function are selected from or dragged from the Project window instead of the Hierarchy window.
{% endhint %}

## Example Code

Example of copies of a game object called "thing" spawning each time the player hits the letter S:

```csharp
using UnityEngine;

public class SpawnThing : MonoBehaviour
{
    public GameObject thing;
    
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.S))
        {
            GameObject copiedThing = Instantiate(thing);
        }
    }
}
```

In your Hierarchy window, the spawned copies will appear as clones:

![](../../.gitbook/assets/image%20%28101%29.png)

## Other Types of Instantiate\(\)

Other forms of the Instantiate\(\) function make it easy to control the position and rotation as well as determining the spawned objects' parent object.

Check out the [Unity Documentation to learn more about the Instantiate\(\) function](https://docs.unity3d.com/ScriptReference/Object.Instantiate.html) and the different ways to use it.

{% hint style="warning" %}
REMEMBER: Add the script to a game object in the scene. It will not work if it does not exist in the game.
{% endhint %}

{% page-ref page="../../select/update-game-objects/" %}

{% page-ref page="../../delete/delete-game-objects/" %}




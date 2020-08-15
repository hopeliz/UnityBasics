# Unhiding/Hiding Objects During Gameplay

## Using SetActive\(\)

Use the script below to make a game object visible and its components available: 

```csharp
this.gameObject.SetActive(true);
```

And unavailable:

```csharp
this.gameObject.SetActive(false);
```

Swap "this" with the variable name for a gameObject type.

**Note:** "gameObject" is only needed if the variable used is of a different type. 

{% hint style="warning" %}
Scripts cannot access components of objects that are not active.
{% endhint %}

## Example Code

Examples of a game object called "thing" that appears when "F" is pressed and disappears when "X" is pressed:

### **Example 1** \(using a gameObject type\):

```csharp
using UnityEngine;

public class AppearDisappear : MonoBehaviour
{
    public GameObject thing;
    
    void Update
    {
        if (Input.GetKeyDown(KeyCode.F) {
            thing.SetActive(true);
        }
        
        if (Input.GetKeyDown(KeyCode.X) {
            thing.SetActive(false);
        }
    }
}
```

### **Example 2** \(using a variable of another type\):

```csharp
using UnityEngine;

public class AppearDisappear : MonoBehaviour
{
    public Transform thing;
    
    void Update
    {
        if (Input.GetKeyDown(KeyCode.F) {
            thing.gameObject.SetActive(true);
        }
        
        if (Input.GetKeyDown(KeyCode.X) {
            thing.gameObject.SetActive(false);
        }
    }
}
```

{% hint style="danger" %}
**REMEMBER:** Hiding a parent object will hide its children.
{% endhint %}

## **Checking If the Game Object is Active**

This code can help if you want things to behave differently if an object is visible or not.

```csharp
this.gameObject.activeSelf
```

It is read-only \(you cannot directly change this value\) and will return true if active and false if not.

In the Hierarchy window, hidden / inactive objects will appear grayed out:

![](../../.gitbook/assets/image%20%28130%29.png)

In the Inspector window, the checkbox next to the object's name controls the active state of the object. Example of an inactive object:

![](../../.gitbook/assets/image%20%28105%29.png)

{% hint style="warning" %}
REMEMBER: Add the script to a game object in the scene. It will not work if it does not exist in the game.
{% endhint %}

{% page-ref page="../../select/update-game-objects/" %}

{% page-ref page="../../delete/delete-game-objects/" %}




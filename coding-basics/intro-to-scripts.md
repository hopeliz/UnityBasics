# Intro to Scripts

Scripts are a way to create custom components that control the properties and interaction with game objects. Unity uses C\# plus it's own library of code so developers don't have to type everything from scratch.

### Default Script

Lets take a look at what is in a default script:

```csharp
using UnityEngine;

public class Example2 : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}
```

**using UnityEngine** - this is one of the libraries that hold code making accessing game objects and components easier. Do not remove this!

**public class** - tells the program this script is accessible by other scrips and the code within this .cs file is a "class" ... think of it as saying this script is a full component that can be added and removed from game objects.

**Example2** - name of the script. This shows as "Example2.cs" in the Assets folder and "Example 2" in the Inspector Tab.

**: MonoBehaviour** - built in parent class that tells the program how to handle the component. All the code for the component should exist inside the brackets that follow.

### Start\(\) **Function**

Unity provides a helpful comment here. The code within the curly brackets after Start\(\) run only once and on the first frame.

This is similar to the setup\(\) function s found in some other programming languages.

### Update\(\) Function

Just as the comment says, the code within the curly brackets after Update\(\) will run once per frame - for many computers, that could mean 60 times a second!

This is similar to loop\(\) or draw\(\) in some other programming languages.

### Adding Custom Code

You can store values, messages, and objects into variables, then control and update them through code. Public variables will appear in the Inspector Tab when the script is added to a game object.

Please see the following sections for more information about the elements used in coding:

{% page-ref page="variables.md" %}

{% page-ref page="conditionals-and-operators.md" %}

{% page-ref page="arrays.md" %}

{% page-ref page="iterators-and-loops.md" %}

{% page-ref page="functions.md" %}






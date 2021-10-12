# Accessing Components Through Scripts

During gameplay, you won't be able to click and drag on objects to update them, so here are some ways to access common properties through scripts.

## Declaring Variables

In your script, public variables can be declared at the top of the class before the Start() function.

Example:

```csharp
public GameObject objectToAppear;
public Transform objectToMove;
public Rigidbody rb;
```

Once saved and added to a game object, the example will appear like this:

![](<../../.gitbook/assets/image (179).png>)

This means the script is looking for specific types of components (GameObject, Transform, and Rigidbody) and took the scripts and turned the variable name into something more readable (if the name is written in "camel" case).

## Assigning Variables

### **Using the Inspector**

Click and drag the game objects you want to manipulate with the script into the proper fields OR clock on the circle/target icon to the right of the field to search for and select the game object. Clicking the target icon will only list objects that have the type of component required.

![](../../.gitbook/assets/AddingObjectToScripts\_01.gif)

Once filled in, it will look similar to this:

![](<../../.gitbook/assets/image (178).png>)

### **Using a Script**

There are times when you need to get a component during gameplay that has changed or has been added that you can't click and drag into an editor field.

There is a GetComponent<> function that can be used to get one component and a GetComponent**s**<> function that gives you an array of the type of components in multiple objects.

Put the type you are looking for within the brackets <>.

This example shows an example of declaring and assigning a private/local Rigidbody variable using GetComponent<>:

```csharp
Rigidbody rb = objectToMove.GetComponent<Rigidbody>();
```

This tells the script to take the "objectToMove", find the Rigidbody component, and store it as "rb".

{% hint style="warning" %}
If there is a reference an object in the script and the Inspector field is empty and the script doesn't assign the variable, you will get a common error:

_UnassignedReferenceException: The variable \__\__\_ of \__\__\_ has not been assigned. You probably need to assign the \__\__\_ variable of the \__\__\_ script in the inspector._
{% endhint %}

## Updating Values

So now, the variable "rb" can be used with any Rigidbody functions.

Note: Storing information into variables is optional. The GetComponent<> function can also access the functions for the type within the brackets <>.

Both lines of code do the same thing:

```csharp
rb.useGravity = false;
objectToMove.GetComponent<Rigidbody>().useGravity = false;
```

This guide will not go in-depth in most components, so please search the Unity Documentation for details.

Generally, you can start typing the name of the value you would like to update and something close will appear in the smart text feature in your IDE/code editor. It will often give you details such as what the command does, what type uses it, what kind of value it uses, and what information is needed to work. There will be arrows that you can scroll through if there are multiple uses of the same function.

![](<../../.gitbook/assets/image (109).png>)

{% content-ref url="../../delete/delete-game-objects/destroy-function.md" %}
[destroy-function.md](../../delete/delete-game-objects/destroy-function.md)
{% endcontent-ref %}

{% content-ref url="../../create/create-scripts/custom-components-and-scripts.md" %}
[custom-components-and-scripts.md](../../create/create-scripts/custom-components-and-scripts.md)
{% endcontent-ref %}

## More Info

Some components are covered in these other sections:

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

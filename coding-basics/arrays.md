# Arrays

### Arrays and Lists

Many games and experiences created in Unity have repeated items that need to be grouped for organization, easy access, and control.

Arrays are lists of elements that can be sorted, searched, counted, etc.

The **index** of an array is the location of the element in the list, **starting with zero**. The index of an element in an array is always an **integer**.

### Why Use Arrays?

Imagine you had a game where you had a large pile of cubes that the player can pick up and manipulate, but you want to control each individually. Putting them all in an empty game object and controlling that parent game object will affect all of them.

You might consider making each cube its own variable:

```csharp
public Transform cube01;
public Transform cube02;
public Transform cube03;
public Transform cube04;
public Transform cube05;
```

....but this gets tedious and the code long.

Instead, use an array!

```csharp
public Transform[] cubes;
```

Adding the square brackets \[\] at the end of the variable type tells the program this is a list of this type of variable.

In the Inspector, this looks like this:

![](../.gitbook/assets/image%20%28150%29.png)

Twirl down the triangle to reveal more values:

![](../.gitbook/assets/image%20%2846%29.png)

Here, you can update how many items to store in the variable "cubes." Once you put in the number, fields will appear for objects and values:

![](../.gitbook/assets/image%20%2874%29.png)

Add your objects and values like you would for other parts of the component:

![](../.gitbook/assets/image%20%28113%29.png)

You'll notice the are a numbered list of "elements." The number for the element is the _index_ of the array.

To access an object or value in an element, use the name of the array and the index inside square brackets \[\]:

```csharp
// Moving only the third listed cube forward
cubes[2].Translate(Vector3.forward);
```

{% hint style="info" %}
Remember: Arrays and lists start with zero, so Element or Index 2 is the third item in the list.
{% endhint %}

This means you can control things through iterative loops:

```csharp
// Moving all cubes forward
for (int i = 0; i < cubes.Length; i++)
{
    cubes[i].Translate(Vector3.forward);
}

// Moving every other cube forward
for (int i = 0; i < cubes.Length; i++)
{
    if (i % 2 == 0)
    {
        cubes[i].Translate(Vector3.forward);
    }
}
```

{% page-ref page="iterators-and-loops.md" %}

### Common Array Functions and Properties

**arrayName.Length** - Provides the size of an array determined by the code, not the number of assigned indexes. Used mostly as a test value in for loops.

{% hint style="info" %}
Since arrays start with zero, make sure for loop control values \(usually _i_ for index\) are tested to be LESS THAN the array length.
{% endhint %}

### **Lists**

Lists are similar to arrays, but have a little more flexibility with it comes to updating the objects and values within them.

Here's how you declare a list of Transforms:

```csharp
public List<Transform> cubes;
```

This appears the same in the Inspector as arrays and the same script can access the elements of the list as arrays.

One big difference is that it doesn't use .Length. Instead, it uses .Capacity:

```csharp
// Moving all cubes forward
for (int i = 0; i < cubes.Capacity; i++)
{
    cubes[i].Translate(Vector3.forward);
}
```

### Common List Functions and Properties

**listName.Capacity** - Provides the size of a list. Used mostly as a test value in for loops.

{% hint style="info" %}
Since arrays start with zero, make sure for loop control values \(usually _i_ for index\) are tested to be LESS THAN the list capacity.
{% endhint %}

**listName.Add\(\)** - Adds the object or value in the parentheses to the end of the list.

**listName.Remove\(\)** - Removes the object or value in the parentheses. You can use listName\[index\] here to remove the proper item.

**listName.Sort\(\)** - Sorts the list alphabetically.

### Using Unity's Built-in Functions

Many built-in functions in Unity return arrays.

Below is an example of accessing a child object using the index.

```csharp
public Transform parentObject;

// Move the third child object upward
parentObject.GetComponentsInChildren<Transform>()[3].Translate(Vector3.up);
```

{% hint style="warning" %}
GetComponentsInChildren&lt;&gt;\(\) will return the parent object as well if the component exists in the parent object.
{% endhint %}

### Helpful Tutorials

[Click here for a helpful tutorial by the creators of Unity about how to use lists and dictionaries within Unity](https://learn.unity.com/tutorial/lists-and-dictionaries#)




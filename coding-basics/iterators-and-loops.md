# Loops

Loops are great for repeating the same command or comparison for multiple items, so they are often used with arrays.

A loop tells the program to run a piece of code multiple times. The number of times is set based on conditions you set.

The most common loops in Unity are For Loops.

### For Loops

For loops basically say, “run this code for this many times.”

The three elements found in for loops are:

1. Starting point or initialization value
2. Conditions to be met
3. How to increase/decrease the value \(steps\)

The value change in steps allows you to skip elements in your array \(prints every fifth element, etc.\).

Format:

```csharp
for (int i = 0; i < 10; i++)
{
    // Do something
}
```

In the code above:

**int i = 0** is the starting point or initialization value. in this example, we start with zero - a common starting value since arrays start with zero. i is generally used, standing for "index."

**i &lt; 10** is the condition to be met to run the code in the brackets. Here, the code will run 10 times, since on the 11th time, i will be 10 and be false.

**i++** is how much to increase the i or index value. ++ is a shorthand for "add 1" and could have also been written as i += 1 \(another shorthand\) or i = i + 1. This number can also be decreased. The shorthand for that would be i-- or i -= 1; The number it increases or decreases can be any integer.

For Loops are great for updating arrays and lists. Just use i \(or your index value\) for your index:

```csharp
public Transform[] cubes;

// Moving all cubes in the cubes array forward
for (int i = 0; i < cubes.Length; i++)
{
     cubes[i].Translate(Vector3.forward);
}
```




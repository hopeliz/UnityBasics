# Conditionals \(If / Then / Else\)

## **If, Then, Otherwise**

Most code can be boiled down to "If this is true, do this."

First, let's look at how to compare values to see if something is true.

## **Comparison Operators**

| Operator | Name | Example |
| :--- | :--- | :--- |
| == | Equals | x == y |
| === | Equals \(exact\) | x === y |
| != | Does Not Equal | x != y |
| &gt; | Greater Than | x &gt; y |
| &lt; | Lesser Than | x &lt; y |
| &gt;= | Greater Than or Equal To | x &gt;= y |
| &lt;= | Lesser Than or Equal To | x &lt;= y |

{% hint style="danger" %}
When comparing using an equals sign, remember to use two equal signs. Using only one tells the program to store/overwrite a variable instead of comparing it.
{% endhint %}

## Using Comparison Operators

An **if statement** asks if a comparison is TRUE.

```csharp
if (true) 
{
    // Do something
}
```

The commands in the brackets will only run if the comparison in the parentheses is true.

Example of true statements:

```csharp
int x = 23;

// Example of true statements

if (x == 23) { }
if (x != 2) { }
if (x < 24) { }
if (x >= 23) { }
```

You might want the program to so something by default or when the comparison is false. Use an **if/else statement** by using the keyword "else" followed by commands in curly brackets:

```csharp
if (true)
{
    // Do something
}
else
{
    // Do something else
}
```

The commands in the else brackets will only run for the times the comparison is false. Writing this code outside of an else statement will apply it in all cases.

There are also ways to do this while checking for a few different comparisons, using an **if/else if/else statement**:

Format:

```csharp
if (true)
{
    // Do something
}
else if (true)
{
    // Do this other thing
}
else
{
    // Do something else
}
```

Example:

```csharp
string fruit = "apples";

if (fruit == "apples")
{
    print("An apple a day keeps the doctor away!");
}
else if (fruit == "bananas")
{
    print("This is bananas!");
}
else
{
    print("That sounds tasty.");
}
```

There can be multiple else if statements. 

**Note:** Each comparison goes in order, so if a comparison is true in the first if statement, it does not get checked in the else if and else statements that follow. Code outside of the if/else if/else statement will be applied to all cases.

## Switch / Case Statements

Using else if statements can get tedious, especially when you are comparing something to a specific number or string.

A switch/case statement takes in the variable to compare and compares it to defined "cases," running the commands within those cases. Instead of an else statement, a default case can be defined.

Format:

```csharp
switch (value)
{
    case comparedValue1:
        // Do something
        break;
    case compareValue2:
        // Do another thing
        break;
    default:
        // Do something if it all else is false
        break;
}
```

Example:

```csharp
string fruit = "apples";

switch (fruit)
{
    case "apples":
        print("An apple a day keeps the doctor away!");
        break;
    case "bananas":
        print("This is bananas!");
        break;
    default:
        print("That sounds tasty.");
        break;
}
```


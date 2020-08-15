# Variables

Variables are ways to tell the computer to get certain information through using a word instead of having to type out a lengthy command each time.

## Parts of a Variable

Let's look at the code for _declaring_ and _assigning_ a simple variable:

```csharp
public int count = 0;
```

**public** - the [**scope**](variables.md#scope) of the variable. It determines how it can be accessed \(can other parts of the code use it? can the user see and update it in the Inspector?\).

**int** - the variable [**type**](variables.md#variable-types). In C\#, this has to be stated and it limits the type of information stored and how it can be used.

**count** - the variable **name**. This is the representative word and can be anything that is not already used, but there are some [naming conventions and rules](variables.md#variable-naming-conventions-and-rules) to follow to ensure it works.

**= \(single equals sign\)** - tells the computer what the variable name should represent or be [_assigned_](variables.md#assigning-variables).

**0** **\(zero\)** - the information stored or [_assigned_](variables.md#assigning-variables) to the variable named count.

**; \(semi-colon\)** - the end of the command.

## Declaring vs. Assigning

**Declaring** a variable is stating the scope, type, and name.

```csharp
public int count;
```

**Assigning** or setting a variable is telling the computer what to represent with the variable name:

```csharp
count = 0;
```

Variables only can be declared once, but they can be assigned and updated when needed.

{% hint style="info" %}
**Best Practice:** When possible, always assign a value or object to your declared variables, even if that is zero or null.
{% endhint %}

## Variable Scope

Scope determines how a variable can be used. They are **private** by default, but adding the scope when declaring a variable helps developers read code quickly.

### Public vs. Private Variables

**Public** variables allow users to see and sometimes update what information the variable represents. You can make a variable public by typing "public" before the variable type when declaring a variable for a script \(at the top and outside of the functions\). Public variables are also accessible by other scripts.

**Private** variables allow the script to reuse a variable, but it will not be visible within the Unity editor's Inspector window nor will it be able to be accessed by other scripts.

### **Global vs. Local Variables**

In most scripts, you will declare variables just above the Start\(\) function. This makes the variable a **global** variable accessible by the functions within the script as well as other scripts accessing it \(as long as it's public\).

Variables declared inside of any function or loop are **local** variables, used only within the function or loop they are declared. So if a variable is declared in the Start\(\) function, the script within the Update\(\) function would not be able to access it.

Unless it is a temporary variable \(such as to keep track of something within a loop only until the loop is finished\) or if it is a name used differently in multiple functions, it's best to make variables as global as possible.

## Variable Types

Here is a list of common types, how to use them in declarations, and their descriptions:

| Type | Declaration | Description |
| :--- | :--- | :--- |
| Integer | int | Whole numbers; can be negative |
| Floating Point | float | Numbers with a decimal; add the letter "F" to the end of these values; can be negative; more precise; used in Vectors and for time; |
| Boolean | bool | true or false; 1 or 0; yes or no; works best with true or false |
| String | string | Plain text; always put this in quotes " " or ' ' ; be careful of apostrophes! \(use \' to avoid breaking code\) |

C\# is an object-oriented programming language. So another type is an object, but it is declared using specific types of objects already built into Unity's code.

Examples include GameObject, Transform, Vector2, Vector3, Collider, Rigidbody, etc.

{% hint style="info" %}
The difference between the type in a variable declaration and using the same word when accessing a part of a game object lies in the capitalization.   
  
Declaring the variable's object type will start with an uppercase letter. Accessing a component of a game object will use the word that starts with a lowercase letter.
{% endhint %}

## Variable Naming Conventions and Rules

Generally, variable names can be almost anything. However, there are some strict rules and some good practices.

### **Strict Rules**

1. User-defined names cannot match keywords used within the script \(i.e. bool, public, for, return, etc.\).
2. Variable names cannot match those within the same scope.
3. Cannot start with a number.
4. No spaces.
5. No special characters.

### **Conventions and Best Practices** 

1. Use descriptive names. Some programming languages use single letters, but Unity is built to take longer descriptive names to help scripts be read by multiple developers.
2. Use "camel casing" for variable names. This is where the first letter is lowercase and other words within the variable name have the first letter capitalized. Examples: moveSpeed, objectToAppear, bluePlayerCollider, etc. The Unity editor will convert this into friendly labels within the Inspector Tab.
3. Avoid reusing variable names in function arguments, even if they are local variables. It makes code easier to troubleshoot.
4. Constant variable names should be in all caps and use underscores between words to signify that they are constants. Examples: BOILING, MAX\_TEMP, TOO\_HIGH, etc.

## Assigning Variables

The information to be stored into a variable should always appear **to the right** of the equal sign.

Objects sometimes require the keyword "new" followed by the object and aspects of that object.

Examples:

```csharp
// Assigning a Vector3
Vector3 destinationPosition = new Vector3(1.3F, 2.4F, 10.12F);

// Assigning a color
Color redShade = new Color(0.9F, 0, 0, 1.0F);
```




# Accessing Materials Through Code

## Getting the Renderer Component

Similar to accessing components through code, the same GetComponent&lt;&gt;\(\) function can be used.

However, you aren't getting a component called "Material." Instead, you are getting the game object's Mesh Renderer to access and update its material.

In the examples below, the following variables are used:

```csharp
public GameObject thing;
public Transform thingTransform;
```

Materials and some of their properties can be stored in variables:

```csharp
public Material woodMaterial;
public Color selectedColor;
public Texture2D woodTexture;
```

In the Inspector, it appears like this, ready for game objects and assets with or of certain types:

![](../../.gitbook/assets/image%20%2880%29.png)

**Remember:** In this example, Thing and Thing Transform fields will only accept game objects. Wood Material and Wood Texture fields will only accept assets of those types. The Selected Color field uses a color picker.

Here is the example filled in:

![](../../.gitbook/assets/image%20%28129%29.png)

Now, the Mesh Renderer of a game object can be accessed and replaced with those stored in variables.

Example of code that would update the material of thing with woodMaterial:

```csharp
thing.GetComponent<Renderer>().material = woodMaterial;
```

## **Accessing the Material**

thing.GetComponent&lt;Renderer&gt;\(\).material is a lot to type each time you need to access the material of an object. So if you find yourself needing to access a game object's material properties often, you can replace that line by storing it in a public variable:

```csharp
public Material thingMaterial;
```

You can also assign the variable using the code:

```csharp
thingMaterial = thing.GetComponent<Renderer>().material;
```

So now, the material can be accessed with the variable.

```csharp
thingMaterial = woodMaterial;
thingMaterial.color = selectedColor;
thingMaterial.SetTexture("_MainTex", woodTexture);
```

## Updating Color

You can store color in a public variable of Color type as seen above or update the values within the script.

The Color object takes red, green, and blue values and an optional fourth value, alpha \(opacity\). Numbers range from 0-1.0 by default.

To set a color, you must tell the program it's a new Color, a new set of values to create a Color object:

Examples:

```csharp
thingMaterial.color = new Color(0, 1, 0);   // Green at full opacity
thingMaterial.color = new Color(1, 1, 0, 0.5F);   // Yellow at half opacity
```

## Updating Textures

You can store a texture in a public variable of Texture 2D type as seen above, but to update it in the script you use the SetTexture\(\) function.

There are different versions of SetTexture\(\), but the most simple takes two arguments - the name of the variable that controls the texture as a string \(in quotes\) and the texture in the form of a variable.

Example:

```csharp
thingMaterial.SetTexture("_MainTex", woodTexture);
```

"\_MainTex" is the default variable used for the texture of Unity shaders.


# Creating and Applying Materials

### Creating a Material Asset

Since materials can be used on multiple game objects, it is an [asset created](../../create/create-assets.md) and stored in the Assets folder and [Project Tab](../../the-unity-interface/the-tabs/project-tab.md).

Right-click in the Project Tab or click on Assets in the task bar.

Select **Create &gt; Material**.

![](../../.gitbook/assets/image%20%2862%29.png)

This will create a new asset in the tab in the current folder:

![](../../.gitbook/assets/image%20%2879%29.png)

Name your material and press Enter to confirm.

**Note:** Unlike scripts, renaming a material is safe and will update editor references to it.

When the asset is selected, the [Inspector Tab](../../the-unity-interface/the-tabs/inspector-tab.md) will show its properties.

![Properties for a standard material called &quot;Wood Material&quot;](../../.gitbook/assets/image%20%28145%29.png)

### **Applying the Material**

This can be done before or after updating the properties. Many developers add the material first to see how the game object will look as they mess with the material options.

To apply the material, simply click and drag the material onto the game object in the Scene Tab, Hierarchy Tab, or \(if selected\) into the Inspector Tab.

### **Common Properties to Play With**

These properties are listed in the order I find myself using the most often.

**Color**

![](../../.gitbook/assets/image%20%28119%29.png)

Click on the color picker to choose the color or input color values. Click on the link below for more details:

{% page-ref page="../../select/components/using-the-inspector-tab.md" %}

**Textures**

Click on the circle / target icon to the left of "Albedo." A window will appear listing your available textures - those in your Asset folder and a few built-in options.

![Wood is a texture I added to the Asset folder. The other textures are built-in to most projects.](../../.gitbook/assets/image%20%2835%29.png)

Double-click or select the asset and close the window. The texture will appear in the square next to Albedo.

![](../../.gitbook/assets/image%20%2825%29.png)

Using a texture with a color other than white could effect the look of your material.

With the current texture and color, the preview of the texture at the bottom of the Inspector Tab looks like this:

![](../../.gitbook/assets/image%20%2876%29.png)

What it looks like on a cube in the scene:

![](../../.gitbook/assets/image%20%28139%29.png)

**Emission**

Materials appearing to glow use the Emission property.

![](../../.gitbook/assets/image%20%2899%29.png)

Click the checkbox to see more options.

![](../../.gitbook/assets/image%20%2819%29.png)

This property can glow based on a color or a texture. The Tiling and Offset is for tweaking textures. HDR colors have an intensity setting to contribute to it's "light source" appearance.

Example of a material named "Glow" with a black albedo color and bright green HDR emission color:

![](../../.gitbook/assets/image%20%2818%29.png)

What it looks like on a cube in the scene:

![](../../.gitbook/assets/image%20%28136%29.png)

**Metallic**

This property can make reflective materials.

![Default settings](../../.gitbook/assets/image%20%2864%29.png)

Example of a material using a white albedo and max  Metallic setting of 1:

![](../../.gitbook/assets/image%20%2829%29.png)

What it looks like on a cube in the scene:

![](../../.gitbook/assets/image%20%2855%29.png)

Example of a material using a white albedo and max Metallic and Smoothness settings of 1:

![](../../.gitbook/assets/image%20%2871%29.png)

What it looks like on a cube in the scene:

![This is so metallic and smooth, it reflects the skybox to the point of looking transparent.](../../.gitbook/assets/image%20%28137%29.png)

**Normal and Height Maps**

Normal and height maps are a type of texture that looks similar to the main albedo texture that is colored in a way to convert the texture into having the appearance of detailed depth. These are used in more advanced texturing and material techniques that allow developers to create super detailed scenes with very basic shapes.

**Occlusion**

Occlusion tells the program what NOT to show. This property can be a texture to help add another layer of detail, similar to Normal and Height maps.

**Tiling and Offset**

![](../../.gitbook/assets/image%20%2834%29.png)

Many textures are not "seamless" and will appear with a very noticeable seam down the middle of your game object. This Tiling and Offset property lets you stretch/zoom in or compress/zoom out the texture on the X and Y axes using the Tiling setting. To move the texture on either axis, use the Offset setting.

Example of using a tiling of 5 on both axes:

![](../../.gitbook/assets/image%20%28123%29.png)

What it looks like on the cube object in the scene:

![](../../.gitbook/assets/image%20%28118%29.png)

{% hint style="warning" %}
Similar to enlarging lower quality images, lower-quality textures will look kinda crappy when zooming in \(tiling less than 1\). If you plan to use parts of a texture, try to find images that are larger.
{% endhint %}

**Rendering Mode**

![](../../.gitbook/assets/image%20%28103%29.png)

This mode is where you can make a material render in different ways, including transparent.

**Shaders**

![](../../.gitbook/assets/image%20%2824%29.png)

As mentioned above, Shaders are powerful code that can tell the computer exactly how a surface or material should appear. In fact, "Standard," is the shader all these properties are part of. Standar is a good place to start, but some tutorials might tell you to choose another. 


# Material Basics

## Overview

This section will cover the basics of materials to get you started. Please check out [Unity's documentation](https://docs.unity3d.com/Manual/Shaders.html) for more information.

Materials are assets that are applied to visible game objects that determine the object's texture, color, and other attributes programmed within its _shader_. Shaders will not be covered in this guide, but they can be coded using HLSL and tools like Shader Graph, available in some Unity project types.

## Default Material

When you create a primitive object (sphere, cube, etc.), it will have a default material.

![How the Material component appears in the Inspector when the object is selected.](<../../.gitbook/assets/image (117).png>)

If you click the triangle on the left to twirl down the properties, you'll notice they're grayed out.

![](<../../.gitbook/assets/image (118).png>)

Depending on your lighting, this default material will appear similar to this:

![](<../../.gitbook/assets/image (119).png>)

In the next section, we'll look at using the Unity editor to create and add materials to game objects.

{% content-ref url="creating-materials.md" %}
[creating-materials.md](creating-materials.md)
{% endcontent-ref %}


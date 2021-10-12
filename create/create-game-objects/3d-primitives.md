# 3D Primitives

**3D Primitives** are the most basic 3D shapes available in Unity.

They include:

| Primitive Name | Collider         | Notes                                                                        |
| -------------- | ---------------- | ---------------------------------------------------------------------------- |
| Cube           | Box Collider     |                                                                              |
| Sphere         | Sphere Collider  |                                                                              |
| Capsule        | Capsule Collider | Y-scale is x 2                                                               |
| Cylinder       | Capsule Collider | Y-scale is x 2                                                               |
| Plane          | Mesh Collider    | <p>X-scale and Z-scale is x 10</p><p>Visible only on one side by default</p> |
| Quad           | Mesh Collider    | Visible only on one side by default                                          |

Each primitive has the following components (seen in the Inspector):

* Transform
* Mesh Filter
* Mesh Renderer
* Collider
* Material

{% content-ref url="editor-creating-game-objects.md" %}
[editor-creating-game-objects.md](editor-creating-game-objects.md)
{% endcontent-ref %}


# Creating Prefabs

## Prefab Overview

Prefabs are sets of game objects with elements and settings you would like to use multiple times or have the ability to change one set to affect all instances of that set. Think projectiles, enemy NPCs, types of structures, etc.

When you add a 3D model to your Assets folder, it becomes a prefab.

## Creating a Prefab

For an example, I made a weird character out of four different spheres with four different positions, sizes, and materials. It would take forever if I wanted to create this multiple times. Even if I duplicated the parent object, updating each could be a nightmare.

![Set of object in the Scene View](<../.gitbook/assets/image (96).png>)

![Hierarchy Tab view](<../.gitbook/assets/image (97).png>)

To make a prefab, click and drag the parent object in the Hierarchy into the Project window.

![](../.gitbook/assets/CreatePrefab\_01.gif)

This creates a prefab asset that can be used multiple times, updated easily, spawned during gameplay, etc.

![Project Tab view](<../.gitbook/assets/image (98).png>)

![Inspector Tab view](<../.gitbook/assets/image (99).png>)

![Hierarchy Tab view](<../.gitbook/assets/image (100).png>)

Prefabs are shown with a blue box icon and the game objects within the prefab are blue, meaning to update them, they need to be updated within the prefab.

{% content-ref url="../select/update-game-objects/updating-prefabs.md" %}
[updating-prefabs.md](../select/update-game-objects/updating-prefabs.md)
{% endcontent-ref %}


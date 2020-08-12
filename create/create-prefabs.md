# Creating Prefabs

## Prefab Overview

Prefabs are sets of game objects with elements and settings you would like to use multiple times or have the ability to change one set to affect all instances of that set. Think projectiles, enemy NPCs, types of structures, etc.

When you add a 3D model to your Assets folder, it becomes a prefab.

## Creating a Prefab

For an example, I made a weird character out of four different spheres with four different positions, sizes, and materials. It would take forever if I wanted to create this multiple times. Even if I duplicated the parent object, updating each could be a nightmare.

![Set of object in the Scene View](../.gitbook/assets/image%20%28132%29.png)

![Hierarchy Tab view](../.gitbook/assets/image%20%28125%29.png)

To make a prefab, click and drag the parent object in the Hierarchy window into the Project window.

This creates a prefab asset that can be used multiple times, updated easily, spawned during gameplay, etc.

![Project Tab view](../.gitbook/assets/image%20%28146%29.png)

![Inspector Tab view](../.gitbook/assets/image%20%28149%29.png)

![Hierarchy Tab view](../.gitbook/assets/image%20%2828%29.png)

Prefabs are shown with a blue box icon and the game objects within the prefab are blue, meaning to update them, they need to be updated within the prefab.

{% page-ref page="../select/update-game-objects/updating-prefabs.md" %}




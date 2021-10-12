# Rigidbody Component Overview

## Default Rigidbody Component

![](<../../.gitbook/assets/image (170).png>)

## Gravity

Here, you can use the mass and drag properties to say how heavy the object seems as it falls, slides, or floats. The more mass the object has, the more force it is required to move it and keep it moving and the more force it will appear to have when accelerated.

Gravity can be toggled for neat effects, but cannot be less than zero. If you want a "floating" effect for water, etc., consider using a script with Vector3.Lerp() where the destination position is a set height.

To see the gravity in action, click the Play button.

{% hint style="warning" %}
Any object or property added, updated, or removed will reset when you stop playing. Make sure to not make important changes in Play Mode.
{% endhint %}

## Is Kinematic

When this is checked, collisions and forces in the scene will not affect the object's Rigidbody component. Why have one, then? Even with Kinematic turned on, force and other factors can be changed through scripts to have it fall and float with mass.

## Constraints

![](<../../.gitbook/assets/image (171).png>)

Use these constraints where an object needs to be frozen on one or more axes from moving or rotating. This is helpful for objects you do not want to tip but needs a Rigidbody component. An example could be a player object that might run into something, but it should stay standing. Constraining the X and Z rotations will prevent the object from tipping, but it can be rotated to look and move around the room.

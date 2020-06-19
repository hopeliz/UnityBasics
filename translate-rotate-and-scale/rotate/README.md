# Rotate

### Rotation

Rotation is the direction an object is facing. This is not in relation to the camera, but an overall coordinate system of the game \(global rotation\) or of the object's parent object \(local rotation\). The rotation coordinates in the Transform component show the object's local rotation in Euler angles unless it is not in a parent object.

### Rotation vs. Euler Angles

The biggest difference you'll notice is that Transform.rotation is a Quaternion expecting four coordinates and Transform.eulerAngles is a Vector3.

When updating rotations directly, it's easiest to use Euler angles because it uses angles -360 to 360 \(and technically, beyond\).

If you ever need to use rotation and Quaternions, use Quaternion.Euler\(\) or Quaternion.LookRotation to get the correct rotation quaternion coordinates.

You can...

[Rotate an object within the Unity editor](rotating.md)

[Rotate an object during gameplay using Transform.Rotate\(\)](using-rotate-function.md)

[Rotate an object during gameplay by directly updating its rotation](updating-eulerangles.md)


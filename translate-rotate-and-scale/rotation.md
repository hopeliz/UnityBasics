# Common Issues with Transforms

**Issue:**

When using a script to rotate a player, the direction the character moves does not update to match the rotation.

**Solution**:

You might be updating the position of your player though updating the position directly. Try using Transform.Translate\(\) instead.


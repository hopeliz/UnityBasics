---
description: Common collider issues
---

# Colliders and Triggers

**Issue:**

OnTriggerEnter\(\), OnTriggerStay\(\), and/or OnTriggerExit\(\) are not working.

**Solutions:**

1. Make sure the objects have colliders and the proper one has the checkbox for **Trigger** checked in the Inspector Tab.  This can be checked and updated with the script by using .isTrigger with the object's collider component.
2. Try adding a rigidbody component to objects that need them.

**Issue:**

OnColliderEnter\(\), OnColliderStay\(\), and/or OnColliderExit\(\) are not working.

**Solutions:**

1. Make sure the objects have colliders and the **Trigger** property is unchecked in the Inspector Tab.  This can be checked and updated with the script by using .isTrigger with the object's collider component.
2. Try adding a rigidbody component to objects that need them.

{% hint style="info" %}
You can check for and update these components and their properties within the script. Go here for information about [accessing components](../select/components/accessing-attributes.md) through the script.
{% endhint %}




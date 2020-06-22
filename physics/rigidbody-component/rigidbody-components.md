---
description: Common Rigidbody issues
---

# Common Issues: Rigidbody Components

**Issue:** 

My objects appear to explode or blast out from each other.

**Solution:** 

Do not have objects with Rigidbody components overlapping each other in the scene. If you need them to overlap, consider making some kinematic, add a Rigidbody component later with AddComponent&lt;Rigidbody&gt;\(\) when needed, or removing a Rigidbody component with Destroy\(GetComponent&lt;Rigidbody&gt;\(\)\).




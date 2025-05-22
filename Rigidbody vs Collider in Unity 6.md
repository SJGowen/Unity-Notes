# Rigidbody vs Collider in Unity 6

## **Rigidbody**
- Enables an object to be **affected by physics forces** like gravity, collisions, and movement through forces or impulses.
- Without a rigidbody, an object **won’t move dynamically** in response to physics calculations.

## **Collider**
- Defines the **physical shape** of an object for collision detection.
- An object with a collider **won’t move due to physics** unless a rigidbody is attached.
- Can be used to detect overlaps and interactions without enabling physics-based movement.

## **Key Difference**
- A **rigidbody controls movement and physics interactions**.
- A **collider determines an object's shape for detecting collisions**.
- Most physics-driven objects need **both** a rigidbody and a collider for proper functionality!

In Unity 6, you can compare Vector3 values using different methods depending on how precise you need the comparison to be.

1. Using == (Equality Operator) // In my experience doesn't always work!
Unity provides an overloaded == operator for Vector3, which checks if two vectors are approximately equal:

csharp
Vector3 a = new Vector3(1.0f, 2.0f, 3.0f);
Vector3 b = new Vector3(1.0f, 2.0f, 3.0f);

if (a == b)
{
    Debug.Log("Vectors are equal!");
}
This method allows for floating-point inaccuracies, meaning it considers two vectors equal if their difference is very small.

2. Using Vector3.Distance()
If you want to check if two vectors are close enough rather than exactly equal:

csharp
if (Vector3.Distance(a, b) < 0.01f) // Threshold for "almost equal"
{
    Debug.Log("Vectors are nearly equal!");
}
3. Using sqrMagnitude for Performance
Instead of Vector3.Distance(), you can use sqrMagnitude, which avoids the costly square root calculation:

csharp
if ((a - b).sqrMagnitude < 0.0001f) // Small threshold
{
    Debug.Log("Vectors are nearly equal!");
}
4. Comparing Individual Components
If you need fine control, compare each component separately:

csharp
if (Mathf.Approximately(a.x, b.x) && Mathf.Approximately(a.y, b.y) && Mathf.Approximately(a.z, b.z))
{
    Debug.Log("Vectors are approximately equal!");
}

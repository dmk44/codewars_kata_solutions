# Counting sheep...

**DESCRIPTION:**

Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example,
```csharp
{true,  true,  true,  false,
  true,  true,  true,  true ,
  true,  false, true,  false,
  true,  false, false, true ,
  true,  true,  true,  true ,
  false, false, true,  true}
```
The correct answer would be 17.

Hint: Don't forget to check for bad values like null/undefined

## Solution
```csharp
using System;
using System.Linq;

public static class Kata {
  public static int CountSheeps(bool[] sheeps) {
            return sheeps.Select(b => b ? 1 : 0).Sum();
        }
}
```

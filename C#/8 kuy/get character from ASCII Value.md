# get character from ASCII Value

**DESCRIPTION:**
Write a function which takes a number and returns the corresponding ASCII char for that value.

**Example:**

65 --> 'A'
97 --> 'a'
48 --> '0
For ASCII table, you can refer to http://www.asciitable.com/

## Solution

```csharp
using System;
using System.Linq;

public class Kata
{
  public static char GetChar(int charcode) => Convert.ToChar(charcode);

}
```

# String ends with?
**DESCRIPTION**: Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

Examples:
```
Inputs: "abc", "bc"
Output: true

Inputs: "abc", "d"
Output: false
```
## Solution
```C#
public class Kata
{
  public static bool Solution(string str, string ending) => str.EndsWith(ending);

}
```
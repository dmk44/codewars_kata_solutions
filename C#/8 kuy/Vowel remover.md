# Vowel remover

**DESCRIPTION:**

Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples
```
"hello"     -->  "hll"
"codewars"  -->  "cdwrs"
"goodbye"   -->  "gdby"
"HELLO"     -->  "HELLO"
```
don't worry about uppercase vowels
`y` is not considered a vowel for this kata

## Solution

```csharp
using System.Linq;

public class Kata {
  public static string Shortcut(string input) {
            char[] vowels = {'a', 'e', 'i', 'o', 'u'};
            return string.Concat(input.Where(c => !vowels.Contains(c)));
        }
}
```
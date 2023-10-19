# Vowel Count
**DESCRIPTION:**

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.


## Solution
```C#
using System;
using System.Linq;

public static class Kata
{
     public static int GetVowelCount(string str) {
        int vowelCount = 0;
        char[] vow = new char[] {'a', 'e', 'i', 'o', 'u'};

        foreach (char el in str.ToCharArray()) {
          if (vow.Contains(el)) vowelCount++; 
        }
        return vowelCount;

}
  }
```
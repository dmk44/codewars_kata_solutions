# Shortest Word
**DESCRIPTION:**

Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.


## Solution
```C#
using System;
using System.Linq;

public class Kata
{
public static int FindShort(string s) {
            string[] ghh = s.Split(" ");
            int[] lens = new int[ghh.Length];

            for (int w = 0; w < ghh.Length; w++) {
                lens[w] = ghh[w].Length;
            }

            return lens.Min();
}}
```
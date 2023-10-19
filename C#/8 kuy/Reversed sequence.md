# Reversed sequence
**DESCRIPTION:**

Build a function that returns an array of integers from n to 1 where n>0.

Example : n=5 --> `[5,4,3,2,1]`


## Solution
```C#
using System;

class Kata {
  
     public static int[] ReverseSeq(int n) {
        int[] seq = new int[n];
        int nn = n;
        for (int i = 0; i < n; i++) {
            seq[i] = nn;
            nn--;
        }
        return seq;
       }
}
```
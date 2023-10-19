# Primes in numbers
**DESCRIPTION:**

Given a positive number n > 1 find the prime factor decomposition of n. The result will be a string with the following form :
```
 "(p1**n1)(p2**n2)...(pk**nk)"
```

with the p(i) in increasing order and n(i) empty if n(i) is 1.

Example: n = 86240 should return `"(2**5)(5)(7**2)(11)"`


## Solution
```C#
using System;
using System.Collections.Generic;

public class PrimeDecomp {

	public static string factors(int n)
    {
        List<(int, int)> factors = new List<(int, int)>();
        int divisor = 2;

        while (divisor <= n)
        {
            if (n % divisor == 0)
            {
                int count = 0;
                while (n % divisor == 0)
                {
                    n /= divisor;
                    count++;
                }
                factors.Add((divisor, count));
            }
            divisor++;
        }

        string decomposition = "";
        foreach (var factor in factors)
        {
            if (factor.Item2 > 1)
            {
                decomposition += $"({factor.Item1}**{factor.Item2})";
            }
            else
            {
                decomposition += $"({factor.Item1})";
            }
        }

        return decomposition;
    }
}
```
# Beginner Series #4 Cockroach

The cockroach is one of the fastest insects. Write a function which takes its speed in km per hour and returns it in cm per second, rounded down to the integer (= floored).

**For example:**

`1.08 --> 30`

Note! The input is a Real number (actual type is language dependent) and is >= 0. The result should be an Integer.

## Solution

```C++
#include <cmath>
float cockroach_speed(float s) {
  return trunc((s * 1000 * 100) / (1 * 60 * 60));
  }
```
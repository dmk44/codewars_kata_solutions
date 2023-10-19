# What is between
**DESCRIPTION:**
Complete the function that takes two integers (a, b, where a < b) and return an array of all integers between the input parameters, including them.

For example:
```
a = 1
b = 4
--> [1, 2, 3, 4]
```
## Solution
```C++
#include <vector>

std::vector <int> between(int start, int end) {
    std::vector <int> vas;

    for (int i = start; i <= end; i++) vas.push_back(i);

    return vas;
} 
```
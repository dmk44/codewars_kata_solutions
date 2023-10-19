# Count of positives / sum of negatives
**DESCRIPTION:**

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input is an empty array or is null, return an empty array.

Example
For input `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]`, you should return `[10, -65]`.

## Solution
```C++
#include <vector>

std::vector<int> countPositivesSumNegatives(std::vector<int> input)
{
int cunt = 0, sum = 0;
for (int i=0; i<input.size(); i++) {
    if (input[i] > 0) cunt++;
    if (input[i] < 0) sum +=input[i];

}

if (cunt == 0 && sum == 0) return {};

else return {cunt, sum};


}
```
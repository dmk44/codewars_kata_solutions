# You only need one - Beginner

You will be given an array `a` and a value `x`. All you need to do is check whether the provided array contains the value.

Array can contain numbers or strings. X can be either.

Return `true` if the array contains the value, `false` if not.

## Solution

```c++
#include <vector>
#include <string>

bool check(const std::vector<std::string>& seq, const std::string& elem) {
    return std::count(std::begin(seq), std::end(seq), elem) > 0;
}
```
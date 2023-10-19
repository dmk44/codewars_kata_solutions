# Split Strings
**DESCRIPTION:**

Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

Examples:
```
* 'abc' =>  ['ab', 'c_']
* 'abcdef' => ['ab', 'cd', 'ef']
```

## Solution
```Python
def solution(s):

    sl = []
    for i in range(0, len(s), 2):
        sl.append(s[i:i+2])

    for i in range(len(sl)):
        if len(sl[i]) < 2:
            sl[i] = sl[i] + "_"

    return sl
```
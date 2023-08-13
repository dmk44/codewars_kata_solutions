# MakeUpperCase

Write a function which converts the input string to uppercase.

## Solution

```c++
#include <string>
using namespace std;

string makeUpperCase (string a)
{

for (short int i=0; i < a.length(); i++) {
    a[i] = toupper(a[i]);
}
return a;

} 
```

# Area of a Square
Complete the function that calculates the area of the red square, when the length of the circular arc A is given as the input. Return the result rounded to two decimals.

![Graph](http://i.imgur.com/nJrae8n.png)

Note: use the π value provided in your language (Math::PI, M_PI, math.pi, etc)


## Solution
```C++
#include <cmath>
double square_area(double A) {
  
  A = A * 4;
  double r = A / (2 * M_PI);
  return round(r * r * 100)/100;
}
```
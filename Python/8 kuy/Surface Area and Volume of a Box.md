# Surface Area and Volume of a Box
**DESCRIPTION**: Write a function that returns the total surface area and volume of a box.

The given input will be three positive non-zero integers: width, height, and depth.

The output will be language dependant, so please check sample tests for the corresponding data type, (list, tuple, struct, query, etcetera).
## Solution
```py
get_size = lambda w, h, d: [2*(d*w + d*h + w*h), w*h*d]
```
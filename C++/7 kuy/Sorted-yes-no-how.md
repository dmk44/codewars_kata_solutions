# Sorted? yes? no? how?
**DESCRIPTION**: Complete the method which accepts an array of integers, and returns one of the following:

`"yes, ascending"` - if the numbers in the array are sorted in an ascending order

`"yes, descending"` - if the numbers in the array are sorted in a descending order

`"no"` - otherwise

The order does not have to be strict: a sorted array can contain consecutive duplicates, e.g. [1, 1, 2, 3] is sorted in ascending order.

It is guaranteed that there will always be a unique valid answer. More precisely:

there will be no arrays with less than 2 elements
there will be no arrays where all elements are equal
## Solution
```C++

std::string is_sorted_and_how(std::vector<int> arr) {
    bool asc = true;
    bool desc = true;

    for (int i = 1; i < arr.size(); i++) {
        if (arr[i] < arr[i - 1]) {
            asc = false;
        }
        if (arr[i] > arr[i - 1]) {
            desc = false;
        }
    }

    if (asc) {
        return "yes, ascending";
    } else if (desc) {
        return "yes, descending";
    } else {
        return "no";
    }
}
```
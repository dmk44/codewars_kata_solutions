# Factorial

Your task is to write function `factorial`.

## Solution

```C++
long long factorial(int n) {
    if (n == 0) return 1;
    else return n * factorial(n-1);
}
```
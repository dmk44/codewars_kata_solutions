# Calculate average
**DESCRIPTION:**

Write a function which calculates the average of the numbers in a given list.

Note: Empty arrays should return 0.


## Solution
```C#
class AverageSolution
{
  public static double FindAverage(double[] array)
  {
    double sum = 0;
    foreach (double el in array) {
    sum += el;
}

if (array.Length == 0) return 0;
    else return (sum / array.Length);
  }
} 
```
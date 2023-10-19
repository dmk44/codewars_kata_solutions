# Switch it Up!
**DESCRIPTION:**

When provided with a number between 0-9, return it in words.

Input :: 1

Output :: "One".

If your language supports it, try using a switch statement.


## Solution
```C#
public class Kata
{
  public static string SwitchItUp(int number) {
            string [] digits = new string[] {"Zero", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten"};
            return digits[number];
        }

}
```
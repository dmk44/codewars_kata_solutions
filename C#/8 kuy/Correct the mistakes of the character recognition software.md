# Correct the mistakes of the character recognition software
**DESCRIPTION:**

Character recognition software is widely used to digitise printed texts. Thus the texts can be edited, searched and stored on a computer.

When documents (especially pretty old ones written with a typewriter), are digitised character recognition softwares often make mistakes.

Your task is correct the errors in the digitised text. You only have to handle the following mistakes:

```
S is misinterpreted as 5
O is misinterpreted as 0
I is misinterpreted as 1
```
The test cases contain numbers only by mistake.


## Solution
```C#
public class Kata
{
  public static string Correct(string text) => text.Replace("1", "I").Replace("0", "O").Replace("5", "S");
  
}
```
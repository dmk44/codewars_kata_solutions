# Detect Pangram
**DESCRIPTION:**

A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.


## Solution
```C#
using System;
using System.Linq;

public static class Kata
{
      public static bool IsPangram(string sentence)
    {
        string alphabet = "abcdefghijklmnopqrstuvwxyz";
        sentence = sentence.ToLower();
        sentence = new string(sentence.Where(char.IsLetter).ToArray());
        var sentenceLetters = sentence.Distinct();

        return sentenceLetters.Count() == alphabet.Length;
    }
}
```
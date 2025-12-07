# Highest Scoring Word
**DESCRIPTION**: Given a string of words, you need to find the highest scoring word.

Each letter of a word scores points according to its position in the alphabet: `a = 1`, `b = 2`, `c = 3` etc.

For example, the score of abad is 8 `(1 + 2 + 1 + 4)`.

You need to return the highest scoring word as a string.

If two words score the same, return the word that appears earliest in the original string.

All letters will be lowercase and all inputs will be valid.
## Solution
```py
def high(words):
    words = words.split(" ")
    alpha = [chr(i) for i in range(97, 123)]

    max_score_word = ""
    max_score = 0

    for w in words:
        score = 0
        for letter in w:
            score += alpha.index(letter) + 1

        if score > max_score:
            max_score = score
            max_score_word = w

    return max_score_word
```
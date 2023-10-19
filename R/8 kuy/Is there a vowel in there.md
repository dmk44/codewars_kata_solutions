# Is there a vowel in there?

Given an array of numbers, check if any of the numbers are the character codes for lower case vowels (a, e, i, o, u).

If they are, change the array value to a string of that vowel.

Return the resulting array.

```R
is_vow <- function(x) {
    vows <- c("a", "e", "i", "o", "u")
    for (i in 1:(length(x))) {
        if (intToUtf8(x[i]) %in% vows) {
            x[i] <- intToUtf8(x[i])
        }
    }
    return(x)
}
```
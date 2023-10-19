# Convert boolean values to strings 'Yes' or 'No'.
**DESCRIPTION:**
Complete the method that takes a boolean value and return a "Yes" string for true, or a "No" string for false.


## Solution
```R
bool_to_word <- function(bool){
  if (bool) return("Yes")
  else return("No")
}
```
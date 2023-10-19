# The Hashtag Generator
**DESCRIPTION:**

The marketing team is spending way too much time typing in hashtags.
Let's help them with our own Hashtag Generator!

Here's the deal:

* It must start with a hashtag (#).
* All words must have their first letter capitalized.
* If the final result is longer than 140 chars it must return false.
* If the input or the result is an empty string it must return false.

Examples
```
" Hello there thanks for trying my Kata"  =>  "#HelloThereThanksForTryingMyKata"
"    Hello     World   "                  =>  "#HelloWorld"
""                                        =>  false
```

## Solution
```Python
def generate_hashtag(s):
    
    s1 = s.split()
    s1 = [x.lower().capitalize() for x in s1]
    hs = "#" + "".join(s1)
    if len(hs) > 140 or len(s) == 0:
        return False
    else: return hs
```
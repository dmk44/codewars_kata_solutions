# All Balanced Parentheses
**DESCRIPTION**: Write a function which makes a list of strings representing all of the ways you can balance n pairs of parentheses

Examples
```
balanced_parens(0) => [""]
balanced_parens(1) => ["()"]
balanced_parens(2) => ["()()","(())"]
balanced_parens(3) => ["()()()","(())()","()(())","(()())","((()))"]
```
## Solution
```py
def balanced_parens(n):
    def generate_parenthesis(left, right, current, result):
        if left == n and right == n:
            result.append(current)
            return
        if left < n:
            generate_parenthesis(left + 1, right, current + "(", result)
        if right < left:
            generate_parenthesis(left, right + 1, current + ")", result)

    result = []
    generate_parenthesis(0, 0, "", result)
    return result
```
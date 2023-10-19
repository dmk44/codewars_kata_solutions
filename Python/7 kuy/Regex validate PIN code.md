# Regex validate PIN code
**DESCRIPTION:**
ATM machines allow 4 or 6 digit PIN codes and PIN codes cannot contain anything but exactly 4 digits or exactly 6 digits.

If the function is passed a valid PIN string, return true, else return false.

Examples (Input --> Output)
```
"1234"   -->  true
"12345"  -->  false
"a234"   -->  false
```

## Solution
```Python
def validate_pin(pin):
    digs = all([l.isdigit() for l in pin])
    return len(pin) == 4 and digs or len(pin) == 6 and digs
```
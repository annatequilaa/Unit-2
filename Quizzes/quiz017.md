

## Code
```.py
def get_truth(n):
    digits = []
    for i in range(n):
        digits.append(0)
    out = ""
    out += f"|bit{n}"
    for i in range(n-1,0,-1):
        out += f"|bit{i}"
    out += "|\n"
    for a in range(2**n):
        for b in range(n):
            if (a // (2 ** (n - 1 - b))) % 2 == 1:
                digits[b] = 1
            else:
                digits[b] = 0
        out += f"| {digits[0]}"
        for c in range(1, n):
            out += f"  | {digits[c]}"
        out += "  |\n"
    return out
```

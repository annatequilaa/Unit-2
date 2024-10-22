# Quiz017 2024/10

## Paper solution

## Flowchart

## Code
```.py
def get_truth(n):
    digits = []
    for i in range(n):
        digits.append(0)
    out = ""
    out += f"|bit{n}"
#this prints numbers from big to small, change it to range(n) to make it from small to big. I prefer showing the biggest number first. 
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

## Proof of Work
![image](https://github.com/user-attachments/assets/850c81f8-08aa-4ee1-a4bb-3c1c6d22e48f)
![image](https://github.com/user-attachments/assets/2b16455a-8164-4337-8c1a-197b4057b4ba)


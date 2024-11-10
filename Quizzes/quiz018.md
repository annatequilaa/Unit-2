# Quiz018 2024/10

## Paper solution
![Uploading image.png…]()

## Code
```.py
def get_truth():
    A, B, C = 1, 1, 1
    output = "| A | B | C |AB+(not B)+not(CB)|\n"
    for i in range(8):
        if i%1 == 0:
            C = not C
        if i%2 == 0:
            B = not B
        if i%4 == 0:
            A = not A
        ans = (A and B) or (not (C and B)) or (not B)
        output += f"| {int(A)} | {int(B)} | {int(C)} |{str(int(ans)).center(18)}|\n"
    return output

print(get_truth())
```

## Proof of Work
![image](https://github.com/user-attachments/assets/48da4583-babb-426a-a47e-aa333652b3fa)


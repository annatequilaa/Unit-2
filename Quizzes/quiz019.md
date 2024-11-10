# Quiz019 2024/10

## Paper solution
![image](https://github.com/user-attachments/assets/740a37f9-875a-4961-8e2b-ceacc94d114b)

## Code
```.py
import random
random.seed(1234)
def produce(n=5,m=3,s=2):
    if s == 0:
        out = "invalid input: cannot be zero"
    else:
        out = f"|{"x".center(20," ")}|{"y".center(20," ")}|\n"
        for i in range(n):
            rx = random.randint(0,100)
            ry = f"{round(rx ** (0.5*((m/s)**2)),2):.2f}"
            out += f"|{str(rx).center(20," ")}|{str(ry).center(20," ")}|\n"
    return out

print(produce())
```

## Proof of Work
![image](https://github.com/user-attachments/assets/5dcb9db6-39bd-4bcb-a19e-02802c0fd169)


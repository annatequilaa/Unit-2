# Quiz020 2024/10

## Paper solution
![image](https://github.com/user-attachments/assets/0c739677-a831-4cc1-b1dc-9816d11a5ffd)

## Code
```.py
import random

from matplotlib import pyplot as plt
import matplotlib

random.seed(1234)

def produce(n=5,m=3,s=2): #default parameters
    x,y = [],[]
    for _ in range(n):
        r = random.randint(0,100)
        x.append(r)
        e = r ** (0.5 * (m/s) ** 2)
        y.append(e)
    return x,y

ax, ay = produce(n=10)
plt.plot(ax,ay,'or') #'or' marker is a circle, color red, no line
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/aaf36757-4ec1-4586-9791-26070353897f)


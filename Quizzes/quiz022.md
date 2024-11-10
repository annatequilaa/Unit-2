# Quiz022 2024/11

## Paper solution

## Code
```.py
from matplotlib import pyplot as plt
plt.style.use('ggplot')
start = -10
step = 0.01
x,y = [], []
for i in range(int(20/step)): #20 = -10 to 10
    n = start + step * i
    x.append(n)
    if n >= 0:
        y.append(n)
    else:
        y.append(n*-1)

plt.plot(x,y)
plt.xlabel("x")
plt.ylabel("$y=|x|$")
plt.title("Graph for the parabola $y=|x|$")
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/1a3af419-09bc-47eb-8703-383e615adbb3)



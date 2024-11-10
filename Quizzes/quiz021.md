# Quiz021 2024/10

## Paper solution
![Uploading image.png…]()

## Code
```.py
from matplotlib import pyplot as plt
import matplotlib

plt.style.use('ggplot')

start = -10
step = 0.01
x,y = [], []

for i in range(int(20/step)): #20 = -10 to 10
    x.append(start + step*i)
    y.append(2*(x[-1]+5)**2)

line_x = [-5, -5]
line_y = [0, 2*((15)**2)]

plt.plot(line_x, line_y, linestyle = "dashed", linewidth = 2, color = "#0a55a6")

plt.plot(x, y, linewidth = 2, color = "#abcdef")
plt.xlabel("x")
plt.ylabel("$y=2(x+5)^2$")
plt.title("Graph for the parabola $y=2(x+5)^2$")
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/0b0331bc-4d28-48f5-9f40-5b17a04e0bf8)


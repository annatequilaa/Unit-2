# Quiz031 2024/11

## Paper solution

## Code
```.py
import matplotlib.pyplot as plt
x1 = [x/100 for x in range(-200,200)]
y1 = [x*x for x in x1]
y2 = [x*x*-1 for x in x1]

ya = [y/100 for y in range(-200,200)]
xa = [y*y for y in ya]
xb = [y*y*-1 for y in ya]


plt.plot(x1,y1, color="red", label = "parabola 1 (x-axis)")
plt.plot(x1,y2, color="purple", label = "parabola 2 (x-axis)")
plt.plot(xa,ya, color="blue", label = "parabola 3 (y-axis)")
plt.plot(xb,ya, color="grey", label = "parabola 3 (y-axis)")
plt.legend(loc="best",frameon = False)
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Four Parabolas Aligned with Axes")
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/6bbec58c-4a28-4746-954a-694c6bb60468)


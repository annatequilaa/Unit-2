# Quiz028 2024/11

## Code
```.py
import requests
from matplotlib import pyplot as plt
import numpy as np

server_ip = "192.168.4.137"

def moving_average(windowSize:int, x:list) -> list:
    x_smoothed = []
    for i in range(0,len(x)-windowSize):
        x_section = x[i:i+windowSize]
        x_average = sum(x_section)/windowSize
        x_smoothed.append(x_average)
    return x_smoothed


sensor_id = 11
sensor_data = []
r = requests.get(f"http://{server_ip}/readings")
r = r.json()
readings = r["readings"][0]
for item in readings:
    if item["sensor_id"] == 11:
        sensor_data.append(item["value"])

y = sensor_data
y_smoothed = moving_average(windowSize = 50, x=y[600:1600])
x = [i for i in range(len(y_smoothed))]

a, b, c = np.polyfit(x,y_smoothed, deg=2)
qua = []
for i in x:
    qua += [a*i**2 + b*i + c]

m, meow = np.polyfit(x,y_smoothed, deg=1)
lin = []
for j in x:
    lin.append(float(m*j + meow))
print(lin)


# s, t, u, v = np.polyfit(x,y_smoothed, deg=3)
# cub = []
# for k in x:
#     cub += [s*k**3 + t*k**2 + u*k + v]

plt.plot(x,y_smoothed)
plt.plot(x,lin, color = "red")
plt.plot(x,qua, color = "green")


plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/248af526-d8c5-4c27-97dc-3ec78c9efab7)


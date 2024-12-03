# Quiz029 2024/11

## Code
```.py
import requests
from matplotlib import pyplot as plt
import numpy as np

server_ip = "192.168.4.137"

request = requests.get(f"http://{server_ip}/readings")
data = request.json()

readings = data['readings'][0]

ids = []
for r in readings:
    if r["sensor_id"] not in ids:
        ids.append(r["sensor_id"])

y = {}
for id in ids:
    y[id] = []

for r in readings:
    y[r["sensor_id"]].append(r["value"])

temperature = y[11]
pressure = y[12]
p_temp = []
avg = []
x_temp = [i for i in range(len(temperature))]
x_pretemp = [i for i in range(len(pressure))]

for pr in pressure:
    p_temp.append(((pr/1010)**5.25)*15)

for k in range(len(p_temp)):
    avg.append((p_temp[k]+temperature[k])/2)


plt.subplot(3,1,1)
plt.plot(x_temp,temperature)

plt.subplot(3,1,2)
plt.plot(x_pretemp,p_temp)

plt.subplot(3,1,3)
plt.plot(x_pretemp,avg)

plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/85709a93-f996-40e1-b94d-4152b4576d7f)


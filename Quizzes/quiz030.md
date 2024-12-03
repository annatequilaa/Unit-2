# Quiz030 2024/11

## Code
```.py
import requests
from matplotlib import pyplot as plt
import matplotlib
from matplotlib.gridspec import GridSpec
import numpy as np

server_ip = "192.168.4.137"

def moving_average(windowSize:int, x:list) -> list:
    x_smoothed = []
    for i in range(0,len(x)-windowSize):
        x_section = x[i:i+windowSize]
        x_average = sum(x_section)/windowSize
        x_smoothed.append(x_average)
    return x_smoothed

#part a
request = requests.get(f"http://{server_ip}/readings") #register is a set of commands that the public can't access
readings = request.json()["readings"][0]

temp = []
humidity = []
for r in readings:
    if r["sensor_id"] == 11:
        temp.append(r["value"])
    if r["sensor_id"] == 10:
        humidity.append(r["value"])

fig = plt.figure(figsize = (10,5)) #10cm x 5cm on the screen)
#from matplotlib.gridspec import GridSpec
grid = GridSpec(nrows=3, ncols=4, figure=fig)
plt.subplots_adjust(hspace=1) #more space between the plots

box1 = fig.add_subplot(grid[1,0]) #row 1 column 0
plt.plot(temp, color = "blue")


minus = []
for q in range(min(len(temp),len(humidity))):
    minus.append(temp[q] - humidity[q])

box2 = fig.add_subplot(grid[0:3,1:3]) #row: 0 to 2 column: 1 to 2
plt.plot(minus, color = "blue")
plt.title("Sensor #11 - sensor #10")

box3 = fig.add_subplot(grid[1,3]) #row 1 column 3
plt.plot(humidity, color = "blue")

plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/d3df553e-5492-4b8d-bb9d-f32e282d2561)


# Quiz023 2024/11

## Paper solution
![image](https://github.com/user-attachments/assets/56aceca6-847a-4dfe-8a65-537f1031adf4)

## Code
```.py
from matplotlib import pyplot as plt
import numpy as np
plt.style.use('ggplot')
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
t = []
for i in range(len(h)):
    t.append((i+1)*10)

m,b = np.polyfit(t,h,1)
print(f"The linear model for the data is y={m:.2f}x+({b:.2f})")
def H_model(m,t,b):
    return m*t+b

t_model = [min(t),max(t)]
h_model = [H_model(min(t),m,b),H_model(max(t),m,b)]
plt.plot(t_model, h_model, color="blue")

plt.scatter(t,h)
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/22dfc8b4-5f92-4b72-a443-0f36bea5639a)


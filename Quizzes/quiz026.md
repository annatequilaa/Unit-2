# Quiz025 2024/11

## Paper solution
![image](https://github.com/user-attachments/assets/d3d2c494-25a2-4925-bf6c-10fc1dd91e4a)

## Code
```.py
def flip(in_dict: dict):
    out_dict = {}
    keys = list(in_dict.keys())
    values = list(in_dict.values())
    for i in range(len(in_dict)):
        if values[i] not in out_dict:
            out_dict[values[i]] = []
        out_dict[values[i]].append(keys[i])
    return out_dict
```

## Proof of Work
![image](https://github.com/user-attachments/assets/c019c1e8-2bfb-42fe-bb79-10138373a183)


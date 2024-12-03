![image](https://github.com/user-attachments/assets/b5a88446-78af-4bc6-9ecd-ddc361c24eb7)# Quiz027 2024/11

## graph
![image](https://github.com/user-attachments/assets/cd64aa30-fdeb-4a2d-bf47-b805adc96797)

## Code
```.py
def sort_dict(in_dict: dict):
    out_dict = {}
    v = list(in_dict.values())
    k = list(in_dict.keys())
    for i in range(len(v)):
        for n in range(i + 1, len(v)):
            if type(v[i]) == str and type(v[n]) == int:
                v[i], v[n] = v[n], v[i]
                k[i], k[n] = k[n], k[i]
            elif type(v[i]) == int and type(v[n]) == int and v[i] > v[n]:
                v[i], v[n] = v[n], v[i]
                k[i], k[n] = k[n], k[i]
    for i in range(len(v)):
        out_dict[k[i]] = v[i]
    return out_dict
```

## Proof of Work
![image](https://github.com/user-attachments/assets/87813da6-6502-4f52-8558-8c6411333b02)


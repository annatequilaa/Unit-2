# Quiz025 2024/11

## Paper solution
![image](https://github.com/user-attachments/assets/818a76c4-9904-41bc-a5f8-9dcd3baec8fd)

## Code
```.py
def count_letters(lexicon: dict, msg: str) -> dict:
    for letter in msg:
        if letter in lexicon:
            lexicon[letter] += 1
    return lexicon
```

## Proof of Work
![image](https://github.com/user-attachments/assets/6bf60ea8-9d4e-4be7-9904-27df5483c86f)


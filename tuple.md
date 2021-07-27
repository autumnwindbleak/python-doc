```python
def get_info():
    name = "ian"
    age = 31
    return name, age


info = get_info()
print(info)
print(type(info))

```



```python
import numpy as np
a = [
    [1, 2, 3, 4, 5],
    [6, 7, 8, 9, 10],
    [11, 12, 13, 14, 15],
    [16, 17, 18, 19, 20],
    [21, 22, 23, 24, 25]
]

a = np.array(a)

print(a[2::2, 2::2])
print(a[1, 10:])
print(a[1, 2:-1])

```

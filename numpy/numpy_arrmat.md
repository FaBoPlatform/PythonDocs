# 配列からTensor(行列)を作る

## Sample(Python2.7)

![](/img/np_arrmat.png)

```python
import numpy as np
arr = np.array([1,5,10,4,11,22,21,11,10,1])
print arr

mat = arr.reshape([5,2])

print mat
```

結果
```shell
[[ 1  5]
 [10  4]
 [11 22]
 [21 11]
 [10  1]]
```

# Sample(Python3.0)

![](/img/np_arrmat.png)

```python
import numpy as np
arr = np.array([1,5,10,4,11,22,21,11,10,1])
print(arr)

mat = arr.reshape([5,2])

print(mat)
```

結果
```shell
[[ 1  5]
 [10  4]
 [11 22]
 [21 11]
 [10  1]]
```
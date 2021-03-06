# ユニバーサル関数

ユニバーサル関数は、numpyオブジェクトのそれぞれの要素に対して計算・操作を返す関数である。

ユニバーサル関数の例:

|関数名|説明|
|:-:|:-:|
|np.add(x1, x2)|加算|
|np.negative(x)|-1を掛けた値を返す|
|np.power(x1, x2)|n乗|
|np.exp(x)|指数関数|
|np.log(x)|対数関数|
|np.sqrt(x)|平方根|

詳しくは[ドキュメント](https://docs.scipy.org/doc/numpy/reference/ufuncs.html#math-operations)を参考。

Sample

```python
# coding:utf-8
import numpy as np

# 4x4行列
x = np.arange(1, 17).reshape(4, 4)
print x
# 加算
print np.add(x, 1)
# 以下も同様
print x + 1
# -1を掛ける
print np.negative(x)
# n乗
print np.power(x, 2)
# 指数関数
print np.exp(x)
# 対数関数
print np.log(x)
# 平方根
print np.sqrt(x)
```

出力結果

```shell
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]
[[ 2  3  4  5]
 [ 6  7  8  9]
 [10 11 12 13]
 [14 15 16 17]]
[[ 2  3  4  5]
 [ 6  7  8  9]
 [10 11 12 13]
 [14 15 16 17]]
[[ -1  -2  -3  -4]
 [ -5  -6  -7  -8]
 [ -9 -10 -11 -12]
 [-13 -14 -15 -16]]
[[  1   4   9  16]
 [ 25  36  49  64]
 [ 81 100 121 144]
 [169 196 225 256]]
[[  2.71828183e+00   7.38905610e+00   2.00855369e+01   5.45981500e+01]
 [  1.48413159e+02   4.03428793e+02   1.09663316e+03   2.98095799e+03]
 [  8.10308393e+03   2.20264658e+04   5.98741417e+04   1.62754791e+05]
 [  4.42413392e+05   1.20260428e+06   3.26901737e+06   8.88611052e+06]]
[[ 0.          0.69314718  1.09861229  1.38629436]
 [ 1.60943791  1.79175947  1.94591015  2.07944154]
 [ 2.19722458  2.30258509  2.39789527  2.48490665]
 [ 2.56494936  2.63905733  2.7080502   2.77258872]]
[[ 1.          1.41421356  1.73205081  2.        ]
 [ 2.23606798  2.44948974  2.64575131  2.82842712]
 [ 3.          3.16227766  3.31662479  3.46410162]
 [ 3.60555128  3.74165739  3.87298335  4.        ]]
```

## 参考

* Numpyのユニバーサル関数一覧
    * https://docs.scipy.org/doc/numpy/reference/ufuncs.html#math-operations

# JavaScript笔试题

```
(1) ["1", "2", "3"].map(parseInt)
```

* A. ["1", "2", "3"]
* B. [1, 2, 3]
* C. [0, 1, 2]
* D. other

> D 你实际上得到的应该是 [1, NaN, NaN] 因为 parseInt 需要两个参数 (val, radix) 但 map 传了 3 个 (element, index, array)

```

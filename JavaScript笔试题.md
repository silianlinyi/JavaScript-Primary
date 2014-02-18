# JavaScript笔试题

```
["1", "2", "3"].map(parseInt)
```

* A. ["1", "2", "3"]
* B. [1, 2, 3]
* C. [0, 1, 2]
* D. other

> D 你实际上得到的应该是 [1, NaN, NaN] 因为 parseInt 需要两个参数 (val, radix) 但 map 传了 3 个 (element, index, array)

```
[typeof null, null instanceof Object]
```

* A. ["object", false]
* B. [null, false]
* C. ["object", true]
* D. other

> A typeof 对原生非可调用对象会始终返回 "object"


```
[ [3,2,1].reduce(Math.pow), [].reduce(Math.pow)] ]
```

* A. an error
* B. [9, 0]
* C. [9, NaN]
* D. [9, undefined]

> A 根据规范： 在一个空数组上应用reduce会抛初始化错误的异常 TypeError

```
var val = 'smtg';
console.log('Value is ' + (val === 'smtg') ? 'Something' : 'Nothing');
```

* A. Value is Something
* B. Value is Nothing
* C. NaN
* D. other

> D 它实际上会打印 'Something' 这个 + 操作符的优先级实际上比三元操作符要高.

```
var name = 'World!';
(function () {
    if (typeof name === 'undefined') {
        var name = 'Jack';
        console.log('Goodbye ' + name);
    } else {
        console.log('Hello ' + name);
    }
})();
```

* A. Goodbye Jack
* B. Hello Jack
* C. Hello undefined
* D. Hello World

> A var 声明的作用域在整个 function 中, 但并没有初始化

```

```





















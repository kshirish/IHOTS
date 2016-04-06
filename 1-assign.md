## [Source](https://github.com/1-liners/1-liners/blob/master/module/assign.js)

```js
    // Returns a new object and assigns `assign` to `object`.
    var test = (assign, object) => ({ ...object, ...assign });
    var a = {name: 'K', id: 1};
    var b = {name: 'G', age: 2};

    console.log(test(a, b));    // {name: "K", age: 2, id: 1}
    console.log(a);             // {name: "K", id: 1}
    console.log(b);             // {name: "G", age: 2}
```


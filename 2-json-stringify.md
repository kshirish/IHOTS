## [Source](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify)

```js
var obj = {
    name: 'K',
    age: 31,
    address: {
        city: 'NY',
        country: 'China'
    },
    isMarried: true
};

var arr = ['Hello', 'World', '!'];

// values to return 
var replacer = function (key, value) {
  if (typeof value === 'number') {
    return 0;
  }
  return value;
};

// space formatting 
var space = 4;

JSON.stringify(obj, replacer, space);
JSON.stringify(arr, replacer, space);
```

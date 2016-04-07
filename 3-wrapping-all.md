## [Source](https://github.com/moll/js-must/blob/master/register.js)

```js
// Usage:
// [].say.evening
// 100.say.day
// true.say.night
// '100'.say.morning

function SayClass() {}
SayClass.prototype.day = function() {console.log('Have a Good Day!');}
SayClass.prototype.morning = function() {console.log('Good morning!');}
SayClass.prototype.evening = function() {console.log('Good evening!');}
SayClass.prototype.night = function() {console.log('Good night!');}

Object.defineProperty(Object.prototype, 'say', {

    get: function() { return new SayClass(this) },
    set: function(value) {

        Object.defineProperty(this, 'say', {
            value: value,
            configurable: true,
            writable: true
        });
    },

    // enumerable will be false default similar to built-in properties
    configurable: true
});
```
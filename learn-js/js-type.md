# JavaScript 数据类型

## 基本数据类型

ES5
- undefined
- null
- boolean
- number
- string
- object

ES6
- symbol

## typeof
```JavaScript
console.log('typeof undefined =', typeof undefined); // undefined
console.log('typeof null =', typeof null); // object
console.log('typeof true =', typeof true); // boolean
console.log('typeof false =', typeof false); // boolean
console.log('typeof 1 =', typeof 1); // number
console.log(`typeof 'abc' =`, typeof 'abc'); // string
console.log(`typeof {} =`, typeof {}); // object
console.log(`typeof [] =`, typeof []); // object
console.log(`typeof function() { } =`, typeof function () { }); // function
console.log(`typeof Symbol() =`, typeof Symbol()); // symbol
```

> 为什么 typeof null 是 object？
>
> 这其实是 js 的一个 bug，详见 [The history of “typeof null”](https://2ality.com/2013/10/typeof-null.html)（[中文](https://juejin.im/post/5a439e30f265da4335630bf4)）
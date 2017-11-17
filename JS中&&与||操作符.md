# JS中&&与||操作符

> a && b : 如果执行a后返回true，则执行b并返回b的值；如果执行a后返回false，则整个表达式返回a的值，b不执行；
> a || b : 如果执行a后返回true，则整个表达式返回a的值，b不执行；如果执行a后返回false，则执行b并返回b的值；

```javascript
console.log(0 && null)      //0
console.log(null && 'a')    //null
console.log('a' && null)    //null
console.log('a' && 'b')     //b
console.log(0 || null)      //null
console.log(null || 'a')    //a
console.log('a' || null)    //a
console.log('a' || 'b')     //a
```

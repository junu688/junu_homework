### 1-22

```js
var n = null;
console.log(typeof n); // object

console.log(n == undefined); // true 둘다 없음 취급
console.log(n == null); // true

console.log(n === undefined); // false 타입 다름
console.log(n === null); // true
```

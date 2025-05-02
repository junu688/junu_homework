### 1-20

```js
var arr1 = [];
arr1.length = 3;
console.log(arr1); // 공간만 있고 값 없음

var arr2 = new Array(3);
console.log(arr2); // 위와 동일

var arr3 = [undefined, undefined, undefined];
console.log(arr3); // 값이 undefined로 명시됨
```

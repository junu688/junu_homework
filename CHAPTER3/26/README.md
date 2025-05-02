### 3-26

```js
var func = function(a, b, c, d) {
  console.log(this, a, b, c, d);
};
var bindFunc = func.bind({ x: 1 }, 4, 5);
console.log(func.name); // func
console.log(bindFunc.name); // bound funcFunction.prototype.name은 함수 이름을 반환bind된 함수는 "bound " 접두사가 붙은 이름을 가짐
```
### 2-12

```js
console.log(sum(3, 4)); // Uncaught Type Error: sum is not a function

var sum = function(x, y) {
  return x + y;
}; // 변수 sum은 undefined로 호이스팅 되며 sum() 호출 시 함수가 아님

var a = sum(1, 2);
### 2-11

```js
console.log(sum(3, 4));

function sum(x, y) {
  return x + y;
}

var a = sum(1, 2);

function sum(x, y) {
  return x + ' + ' + y + ' = ' + (x + y);
} // 재정의된 두 번 째 sum 사용

var c = sum(1, 2);
console.log(c);
```
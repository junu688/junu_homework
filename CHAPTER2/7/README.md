### 2-7

```js
function a() {
  var b;
  var b = function b() {}; // b는 외부 스코프에서 변수. 내부의 b는 이름만 있는 지역 스코프

  console.log(b); // (1)
  b = 'bbb';
  console.log(b); // (2)
  console.log(b); // (3)
}
a();
```
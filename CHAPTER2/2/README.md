### 2-2

```js
function a(x) {
  // 수집 대상 1(매개변수)
  console.log(x); // (1)
  var x; // var는 중복 선언 됨
  console.log(x); // (2)
  var x = 2; // 실제 재할당
  console.log(x); // (3)
}
a(1);
```

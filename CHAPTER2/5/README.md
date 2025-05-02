### 2-5

```js
function a() {
  console.log(b); // (1)
  var b = 'bbb'; // 변수 선언 호이스팅, 값은 원래 자리
  console.log(b); // (2)
  function b() {} // 함수 선언문 전체가 호이스팅됨
  console.log(b); // (3)
}
a();
```
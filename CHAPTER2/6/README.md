### 2-6

```js
function a() {
  var b; // 호이스팅됨
  function b() {} // 전체 호이스팅-> 함수가 우선

  console.log(b); // (1)
  b = 'bbb'; // 변수의 할당부는 원래 자리에 남겨둡니다.
  console.log(b); // (2)
  console.log(b); // (3)
}
a();
```

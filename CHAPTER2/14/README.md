### 2-14

```js
var a = 1;
var outer = function() {
  var b = 2;
  var inner = function() {
    console.dir(inner);
  };
  inner();
};
outer();// 함수의 클로저 스코프 확인가능
```
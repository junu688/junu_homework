### 2-16

```js
var a = 1;
var outer = function() {
  var b = 2;
  var inner = function() {
    console.log(b);
    debugger;
  };
  inner();
};
outer();// debugger는 개발자 도구에서 클로저 및 실행 컨텍스트 확인하게 함
```

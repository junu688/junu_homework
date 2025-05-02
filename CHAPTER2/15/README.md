### 2-15

```js
var a = 1;
var outer = function() {
  var b = 2;
  var inner = function() {
    console.log(b);
    console.dir(inner);
  };
  inner();
};
outer();// inner는 outer의 b를 클로저로 참고함
```
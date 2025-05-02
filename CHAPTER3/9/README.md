### 3-9

```js
var obj1 = {
  outer: function() {
    console.log(this); // (1)
    var innerFunc = function() {
      console.log(this); // (2) (3)
    };
    innerFunc();

    var obj2 = {
      innerMethod: innerFunc,
    };
    obj2.innerMethod();
  },
};
obj1.outer(); // this는 호출 주체에 따라 결정됨. innerFunc()는 일반 호출 → this === window obj2.innerMethod()는 메서드 호출 → this === obj2
```

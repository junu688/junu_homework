### 3-28

```js
var obj = {
  logThis: function() {
    console.log(this);
  },
  logThisLater1: function() {
    setTimeout(this.logThis, 500);
  },
  logThisLater2: function() {
    setTimeout(this.logThis.bind(this), 1000);
  },
};
obj.logThisLater1(); // Window { ... }
obj.logThisLater2(); // obj { logThis: f, ... } setTimeout(this.logThis)는 함수만 전달 → this는 window bind(this)로 묶어주면 this가 obj로 고정됨
```

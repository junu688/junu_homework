### 3-15

```js
var obj = {
  a: 1,
  method: function(x, y) {
    console.log(this.a, x, y);
  },
};

obj.method(2, 3); // 1 2 3
obj.method.call({ a: 4 }, 5, 6); // 4 5 6 메서드를 call로 호출하면 this를 바꿔 실행 가능첫 번째 인자에 전달한 객체가 this로 작동함
```
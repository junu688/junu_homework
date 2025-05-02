### 3-11

```js
var obj = {
  outer: function() {
    console.log(this); // (1) { outer: f }
    var innerFunc = () => {
      console.log(this); // (2) { outer: f }
    };
    innerFunc();
  },
};
obj.outer();// 화살표 함수는 상위 스코프의 this를 그대로 사용함
```
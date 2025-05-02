### 3-27

```js
var obj = {
  outer: function() {
    console.log(this);
    var innerFunc = function() {
      console.log(this);
    };
    innerFunc.call(this);
  },
};
obj.outer();
```

```js
var obj = {
  outer: function() {
    console.log(this);
    var innerFunc = function() {
      console.log(this);
    }.bind(this);
    innerFunc();
  },
};
obj.outer();// 일반 함수는 기본적으로 this === windowcall(this)이나 bind(this)로 내부 함수의 this를 외부에 맞춤
```

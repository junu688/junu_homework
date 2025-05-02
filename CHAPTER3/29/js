### 3-29

```js
var obj = {
  outer: function() {
    console.log(this);
    var innerFunc = () => {
      console.log(this);
    };
    innerFunc();
  },
};
obj.outer();//화살표 함수는 **상위 스코프의 this(obj)**를 그대로 사용 this 유지하려고 bind나 self = this 안 써도 됨


```
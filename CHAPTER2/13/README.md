 
### 2-13

```js
var a = 1;
var outer = function() {
  var inner = function() {
    console.log(a);
    var a = 3;
  };
  inner();
  console.log(a);
};
outer(); // 내부의  var a = 3 이 호이스팅 되고 defined, 바깥 a는 그대로 1
console.log(a);
```


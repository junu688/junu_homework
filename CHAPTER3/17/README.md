### 3-17

```js
var obj = {
  0: 'a',
  1: 'b',
  2: 'c',
  length: 3,
};
Array.prototype.push.call(obj, 'd');
console.log(obj); // { 0: 'a', 1: 'b', 2: 'c', 3: 'd', length: 4 }

var arr = Array.prototype.slice.call(obj);
console.log(arr); // [ 'a', 'b', 'c', 'd' ] obj는 배열처럼 생긴 객체 → push와 slice 사용 가능call로 this를 obj에 지정해 배열 메서드 강제 적용
```

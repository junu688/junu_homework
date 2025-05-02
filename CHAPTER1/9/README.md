### 1-9

```js
var a = 10;
var b = a;
var obj1 = { c: 10, d: 'ddd' };
var obj2 = obj1;

b = 15;// 원시값 b만 변경
obj2 = { c: 20, d: 'ddd' };// obj2가 새 객체를 가리킴 (obj1은 영향 없음)
```
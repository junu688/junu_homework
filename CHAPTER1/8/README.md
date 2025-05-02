### 1-8

```js
var a = 10;
var b = a; // 값 복사
var obj1 = { c: 10, d: 'ddd' };
var obj2 = obj1; // 참조 복사

b = 15; // b만 바뀌고 a는 개별값이므로 변하지 않음
obj2.c = 20; // obj1과 obj2가 같은 객체이므로 obj1.c 도 바뀜
```
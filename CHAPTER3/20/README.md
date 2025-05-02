### 3-20

```js
var obj = {
  0: 'a',
  1: 'b',
  2: 'c',
  length: 3,
};
var arr = Array.from(obj);
console.log(arr); // ['a', 'b', 'c']Array.from은 배열 유사 객체를 진짜 배열로 변환 length 속성이 있어야 제대로 작동함


```
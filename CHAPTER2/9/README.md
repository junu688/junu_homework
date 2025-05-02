### 2-9

```js
console.log(sum(1, 2));
console.log(multiply(3, 4));

function sum(a, b) {
  // 함수 선언문 sum
  return a + b;
}

var multiply = function(a, b) {
  // 함수 표현식 multiply
  return a * b;
};
```// sum()은 정상 호출됨 (선언문이라 호이스팅됨)

multiply()는 undefined → 오류 (호이스팅되는 건 var multiply;뿐
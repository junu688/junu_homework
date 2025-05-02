### 2-1

```js
// -------------------------- (1)
var a = 1;
function outer() {
  function inner() {
    console.log(a); // undefined
    var a = 3;
  }
  inner(); // ------------ (2)
  console.log(a); // var a=3; 에서 var a;가 호이스팅되고 undefined 로 초기화됨. 
}
outer(); // 함수 바깥의 var a =1;을 참조
console.log(a); // outer 실행 후에도 전역 변수 a=1
```
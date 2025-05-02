### 3-5

```js
var a = 1;
delete window.a; // false
console.log(a, window.a, this.a); // 1 1 1

var b = 2;
delete b; // false
console.log(b, window.b, this.b); // 2 2 2

window.c = 3;
delete window.c; // true
console.log(c, window.c, this.c); // Uncaught ReferenceError: c is not defined

window.d = 4;
delete d; // true var로 선언된 변수는 삭제 불가 (false)window.c = 3처럼 직접 추가한 속성은 삭제 가능 (true)
console.log(d, window.d, this.d); // Uncaught ReferenceError: d is not defined
```
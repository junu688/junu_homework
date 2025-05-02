### 2-3

```js
function a() {
  var x = 1; // 수집 대상 1(매개변수 선언)
  console.log(x); // (1)
  var x; // 수집 대상 2(변수 선언)
  console.log(x); // (2)
  var x = 2; // 중복된 var x 선언은 무시됨. 실행 흐름은 x=1 -> x=2
  console.log(x); // (3)
}
a();
```
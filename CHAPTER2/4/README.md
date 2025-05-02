### 2-4

```js
function a() {
  var x; // 수집 대상 1의 변수 선언 부분
  var x; // 수집 대상 2의 변수 선언 부분
  var x; // 수집 대상 3의 변수 선언 부분

  x = 1; // 수집 대상 1의 할당 부분
  console.log(x); // (1)
  console.log(x); // (2)
  x = 2; // 모두 하나로 병합되어 위로 올라감. 중복 선언 무시함
  console.log(x); // (3)
}
a(1);
```
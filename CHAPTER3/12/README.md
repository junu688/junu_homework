### 3-12

```js
setTimeout(function() {
  console.log(this);
}, 300); // (1)

[1, 2, 3, 4, 5].forEach(function(x) {
  // (2)
  console.log(this, x);
});

document.body.innerHTML += '<button id="a">클릭</button>';
document.body.querySelector('#a').addEventListener('click', function(e) {
  // (3)
  console.log(this, e);// setTimeout과 forEach의 this는 기본적으로 window 이벤트 리스너의 this는 이벤트 발생한 DOM 요소
});
```
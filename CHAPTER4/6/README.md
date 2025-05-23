// 4-6: this 바인딩에 따른 동작 비교
// 일반 함수 호출 시 this는 window, 이벤트 리스너 내에서는 this가 버튼 요소
setTimeout(function() {
  console.log(this); // window
}, 300);

[1, 2, 3, 4, 5].forEach(function(x) {
  console.log(this); // window
});

document.body.innerHTML += '<button id="a">클릭</button>';
document.body.querySelector('#a').addEventListener(
  'click',
  function(e) {
    console.log(this, e); // 클릭된 버튼 요소와 이벤트 객체 출력
  }
);

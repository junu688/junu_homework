// 5-4(1): setInterval에서 클로저로 변수 a를 참조해 반복 출력
(function() {
  var a = 0;
  var intervalId = null;
  var inner = function() {
    if (++a >= 10) {
      clearInterval(intervalId); // 10 이상이면 반복 중지
    }
    console.log(a);
  };
  intervalId = setInterval(inner, 1000);
})();

// 5-4(2): eventListener 내 클로저를 사용해 count를 참조
(function() {
  var count = 0;
  var button = document.createElement('button');
  button.innerText = 'click';
  button.addEventListener('click', function() {
    console.log(++count, 'times clicked');
  });
  document.body.appendChild(button);
})();
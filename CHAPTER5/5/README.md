// 5-5(1): 클로저를 반환한 후 참조를 해제하여 메모리 해제 유도
var outer = (function() {
  var a = 1;
  var inner = function() {
    return ++a;
  };
  return inner;
})();
console.log(outer());
console.log(outer());
outer = null; // 참조 제거

// 5-5(2): setInterval 내부 클로저 참조 제거
(function() {
  var a = 0;
  var intervalId = null;
  var inner = function() {
    if (++a >= 10) {
      clearInterval(intervalId);
      inner = null; // 참조 제거
    }
    console.log(a);
  };
  intervalId = setInterval(inner, 1000);
})();

// 5-5(3): 이벤트 리스너의 참조 제거
(function() {
  var count = 0;
  var button = document.createElement('button');
  button.innerText = 'click';

  var clickHandler = function() {
    console.log(++count, 'times clicked');
    if (count >= 10) {
      button.removeEventListener('click', clickHandler);
      clickHandler = null; // 참조 제거
    }
  };
  button.addEventListener('click', clickHandler);
  document.body.appendChild(button);
})();

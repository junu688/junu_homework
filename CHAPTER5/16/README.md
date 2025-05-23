// 5-16: debounce 함수 – 빠른 이벤트를 일정 시간 후 하나만 실행
var debounce = function(eventName, func, wait) {
  var timeoutId = null;
  return function(event) {
    var self = this;
    console.log(eventName, 'event 발생');
    clearTimeout(timeoutId);
    timeoutId = setTimeout(func.bind(self, event), wait);
  };
};

document.body.addEventListener('mousemove', debounce('move', function() {
  console.log('move event 처리');
}, 500));

document.body.addEventListener('mousewheel', debounce('wheel', function() {
  console.log('wheel event 처리');
}, 700));

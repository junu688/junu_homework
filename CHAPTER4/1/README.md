// 4-1: setInterval을 이용해 0.3초 간격으로 count 출력
// count가 5가 되면 clearInterval로 타이머 종료

var count = 0;
var timer = setInterval(function() {
  console.log(count); // 현재 count 출력
  if (++count > 4) clearInterval(timer); // 증가된 count가 4 초과면 종료
}, 300);
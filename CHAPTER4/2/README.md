// 4-2: 동일한 타이머 로직이지만 콜백 함수를 변수로 분리하여 선언
// 같은 동작이지만 코드 구조를 개선함
var count = 0;
var cbFunc = function() {
  console.log(count);
  if (++count > 4) clearInterval(timer);
};
var timer = setInterval(cbFunc, 300);
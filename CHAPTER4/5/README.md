// 4-5: Array.prototype.map을 직접 구현한 사용자 정의 버전
// 콜백 함수에 thisArg를 전달할 수 있도록 call 메서드 사용
Array.prototype.map = function(callback, thisArg) {
  var mappedArr = [];
  for (var i = 0; i < this.length; i++) {
    var mappedValue = callback.call(thisArg || window, this[i], i, this);
    mappedArr[i] = mappedValue;
  }
  return mappedArr;
};

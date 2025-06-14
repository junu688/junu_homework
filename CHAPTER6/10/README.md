var Grade = function() {
  var args = Array.prototype.slice.call(arguments);  // arguments를 진짜 배열로 변환
  for (var i = 0; i < args.length; i++) {
    this[i] = args[i];  // 인덱스 기반으로 프로퍼티 할당 → 유사 배열처럼
  }
  this.length = args.length;  // length 프로퍼티 추가
};
var g = new Grade(100, 80);

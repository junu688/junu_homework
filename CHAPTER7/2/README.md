var Grade = function() {  // 유사배열 Grade 생성자
  var args = Array.prototype.slice.call(arguments);
  for (var i = 0; i < args.length; i++) {
    this[i] = args[i];
  }
  this.length = args.length;
};
Grade.prototype = [];  // 프로토타입을 빈 배열로 설정 (배열처럼 사용하기 위한 설정)
var g = new Grade(100, 80);

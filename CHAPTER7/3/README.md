var Grade = function() {  // 위와 동일
  var args = Array.prototype.slice.call(arguments);
  for (var i = 0; i < args.length; i++) {
    this[i] = args[i];
  }
  this.length = args.length;
};
Grade.prototype = [];  // 배열 프로토타입 상속

var g = new Grade(100, 80);

g.push(90);  // 프로토타입 배열의 push 메서드 사용 가능
console.log(g); // Grade { 0: 100, 1: 80, 2: 90, length: 3 }


delete g.length;  // length 프로퍼티 삭제 (주의: 유사배열이므로 length는 직접 소유)
g.push(70);  // 이제 length가 undefined이므로 push가 length 0으로 간주하고 0번부터 덮어씀
console.log(g); // Grade { 0: 70, 1: 80, 2: 90, length: 1 }

var Grade = function() {  // 동일
  var args = Array.prototype.slice.call(arguments);
  for (var i = 0; i < args.length; i++) {
    this[i] = args[i];
  }
  this.length = args.length;
};
Grade.prototype = ['a', 'b', 'c', 'd'];  // 프로토타입 배열에 초기값 설정
var g = new Grade(100, 80);

g.push(90);  // push는 length 사용 → 인스턴스 length가 우선됨
console.log(g); // Grade { 0: 100, 1: 80, 2: 90, length: 3 }

delete g.length;  // length 삭제 → 프로토타입의 length 사용됨 (4)
g.push(70);  // prototype length가 4라서 4번 인덱스부터 push 시작
console.log(g); // Grade { 0: 100, 1: 80, 2: 90, ___ 4: 70, length: 5 }

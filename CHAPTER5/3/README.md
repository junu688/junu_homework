// 5-3: 클로저를 반환값으로 저장하여 이후에도 상태를 유지함
var outer = function() {
  var a = 1;
  var inner = function() {
    return ++a;
  };
  return inner; // 함수 자체 반환
};
var outer2 = outer();
console.log(outer2()); // 2
console.log(outer2()); // 3 (상태 유지)
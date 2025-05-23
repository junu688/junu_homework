// 5-2: 클로저를 return 값으로 사용
var outer = function() {
  var a = 1;
  var inner = function() {
    return ++a; // 외부 변수 a를 증가시킨 후 반환
  };
  return inner(); // inner 함수 결과 반환
};
var outer2 = outer();
console.log(outer2); // 2
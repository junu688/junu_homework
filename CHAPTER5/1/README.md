// 5-1: 클로저 기본 개념 – inner 함수가 outer의 변수 a를 참조함
var outer = function() {
  var a = 1;
  var inner = function() {
    console.log(++a); // outer의 변수 a를 참조하고 증가시킴
  };
  inner(); // 즉시 호출
};
outer(); // 출력: 2
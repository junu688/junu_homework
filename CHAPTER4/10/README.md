// 4-10: this와 함수 참조의 불일치 사례
var obj1 = {
  name: 'obj1',
  func: function() {
    console.log(obj1.name); // this가 obj1이 아님에도 직접 참조
  },
};
var obj2 = {
  name: 'obj2',
  func: obj1.func,
};
var callback2 = obj2.func(); // 실행 시점에 obj1.name 참조됨
setTimeout(callback2, 1500); // undefined 가능

var obj3 = { name: 'obj3' };
var callback3 = obj1.func.call(obj3); // 여전히 obj1.name 참조
setTimeout(callback3, 2000);
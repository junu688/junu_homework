// 4-9: obj1.name을 직접 참조하는 방식이므로 this에 영향을 받지 않음
var obj1 = {
  name: 'obj1',
  func: function() {
    console.log(obj1.name); // 직접 참조로 항상 'obj1'
  },
};
setTimeout(obj1.func, 1000);
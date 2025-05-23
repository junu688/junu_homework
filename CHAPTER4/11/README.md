// 4-11: bind를 사용한 this 고정
var obj1 = {
  name: 'obj1',
  func: function() {
    console.log(this.name); // bind로 this를 고정시킴
  },
};
setTimeout(obj1.func.bind(obj1), 1000); // obj1

var obj2 = { name: 'obj2' };
setTimeout(obj1.func.bind(obj2), 1500); // obj2

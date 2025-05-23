// 4-8: self를 이용한 this 우회 보존
var obj1 = {
  name: 'obj1',
  func: function() {
    var self = this;
    return function() {
      console.log(self.name); // self를 참조하므로 obj1.name 출력됨
    };
  },
};
var callback = obj1.func();
setTimeout(callback, 1000);
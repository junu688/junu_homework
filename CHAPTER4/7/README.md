// 4-7: forEach의 콜백으로 객체의 메서드를 전달할 경우 this가 window로 바인딩됨
var obj = {
  vals: [1, 2, 3],
  logValues: function(v, i) {
    console.log(this, v, i); // 기대: obj, 실제: window
  },
};
obj.logValues(1, 2);
[4, 5, 6].forEach(obj.logValues); // this가 window
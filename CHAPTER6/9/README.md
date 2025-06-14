Object.prototype.getEntries = function() {
  var res = [];
  for (var prop in this) {  // for-in: 열거 가능한 프로퍼티 모두 순회
    if (this.hasOwnProperty(prop)) {  // 상속받은 프로퍼티 제외
      res.push([prop, this[prop]]);
    }
  }
  return res;
};
var data = [
  ['object', { a: 1, b: 2, c: 3 }],
  ['number', 345],
  ['string', 'abc'],
  ['boolean', false],
  ['func', function() {}],
  ['array', [1, 2, 3]],
];
data.forEach(function(datum) {
  console.log(datum[1].getEntries());
});

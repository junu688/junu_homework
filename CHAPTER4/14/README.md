// 4-14: Promise 체인을 활용하여 순차적으로 비동기 처리 구현
new Promise(function(resolve) {
  setTimeout(function() {
    var name = '에스프레소';
    console.log(name);
    resolve(name);
  }, 500);
})
  .then(function(prevName) {
    return new Promise(function(resolve) {
      setTimeout(function() {
        var name = prevName + ', 아메리카노';
        console.log(name);
        resolve(name);
      }, 500);
    });
  })
  .then(function(prevName) {
    return new Promise(function(resolve) {
      setTimeout(function() {
        var name = prevName + ', 카페모카';
        console.log(name);
        resolve(name);
      }, 500);
    });
  })
  .then(function(prevName) {
    return new Promise(function(resolve) {
      setTimeout(function() {
        var name = prevName + ', 카페라떼';
        console.log(name);
        resolve(name);
      }, 500);
    });
  });
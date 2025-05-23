// 4-16: generator를 이용한 비동기 흐름 제어
// next() 호출마다 함수 진행이 재개됨
var addCoffee = function(prevName, name) {
  setTimeout(function() {
    coffeeMaker.next(prevName ? prevName + ', ' + name : name);
  }, 500);
};
var coffeeGenerator = function*() {
  var espresso = yield addCoffee('', '에스프레소');
  console.log(espresso);
  var americano = yield addCoffee(espresso, '아메리카노');
  console.log(americano);
  var mocha = yield addCoffee(americano, '카페모카');
  console.log(mocha);
  var latte = yield addCoffee(mocha, '카페라떼');
  console.log(latte);
};
var coffeeMaker = coffeeGenerator();
coffeeMaker.next(); // 실행 시작
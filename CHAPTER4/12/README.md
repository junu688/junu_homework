// 4-12: 중첩된 setTimeout을 통한 콜백 지옥
// 커피 이름을 순서대로 추가하며 출력함
setTimeout(function(name) {
  var coffeeList = name;
  console.log(coffeeList);

  setTimeout(function(name) {
    coffeeList += ', ' + name;
    console.log(coffeeList);

    setTimeout(function(name) {
      coffeeList += ', ' + name;
      console.log(coffeeList);

      setTimeout(function(name) {
        coffeeList += ', ' + name;
        console.log(coffeeList);
      }, 500, '카페라떼');
    }, 500, '카페모카');
  }, 500, '아메리카노');
}, 500, '에스프레소');
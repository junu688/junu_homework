// 5-9: 클로저 팩토리 패턴 사용 (함수를 리턴)
var fruits = ['apple', 'banana', 'peach'];
var $ul = document.createElement('ul');

var alertFruitBuilder = function(fruit) {
  return function() {
    alert('your choice is ' + fruit); // 클로저에 fruit 저장
  };
};
fruits.forEach(function(fruit) {
  var $li = document.createElement('li');
  $li.innerText = fruit;
  $li.addEventListener('click', alertFruitBuilder(fruit));
  $ul.appendChild($li);
});
document.body.appendChild($ul);
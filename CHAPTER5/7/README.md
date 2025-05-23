// 5-7: 클로저 대신 외부 함수 참조를 사용한 경우 – 모든 항목이 동일 반응
var fruits = ['apple', 'banana', 'peach'];
var $ul = document.createElement('ul');

var alertFruit = function(fruit) {
  alert('your choice is ' + fruit);
};
fruits.forEach(function(fruit) {
  var $li = document.createElement('li');
  $li.innerText = fruit;
  $li.addEventListener('click', alertFruit); // fruit 전달 X
  $ul.appendChild($li);
});
document.body.appendChild($ul);
alertFruit(fruits[1]); // 호출 예시

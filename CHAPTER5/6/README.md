// 5-6: 클로저로 각 fruit 값을 기억한 함수 생성
var fruits = ['apple', 'banana', 'peach'];
var $ul = document.createElement('ul');

fruits.forEach(function(fruit) {
  var $li = document.createElement('li');
  $li.innerText = fruit;
  $li.addEventListener('click', function() {
    alert('your choice is ' + fruit); // 클로저로 fruit를 유지
  });
  $ul.appendChild($li);
});
document.body.appendChild($ul);
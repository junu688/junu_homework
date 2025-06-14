var NewConstructor = function() {  // 새로운 생성자 선언
  console.log('this is new constuctor!');
};
var dataTypes = [  // 다양한 데이터 타입 준비
  1, 'test', true, {}, [], function() {}, /test/,
  new Number(), new String(), new Boolean(), new Object(),
  new Array(), new Function(), new RegExp(), new Date(), new Error(),
];

dataTypes.forEach(function(d) {
  d.constructor = NewConstructor;  // 강제로 constructor 프로퍼티 변경
  console.log(d.constructor.name, '&', d instanceof NewConstructor);  
  // constructor 이름은 변경되었지만, instanceof는 false (실제 생성자 아님)
});

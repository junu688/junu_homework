var Person = function(name) {
  this.name = name;
};
var p1 = new Person('사람1');  // Person 생성자를 이용해 인스턴스 생성
var p1Proto = Object.getPrototypeOf(p1);  // p1의 프로토타입 가져오기
var p2 = new Person.prototype.constructor('사람2');  // 프로토타입의 constructor 활용
var p3 = new p1Proto.constructor('사람3');  // 프로토타입 객체에서 constructor 활용
var p4 = new p1.__proto__.constructor('사람4');  // __proto__로 프로토타입 접근하여 constructor 사용
var p5 = new p1.constructor('사람5');  // 인스턴스에서 constructor 바로 사용

[p1, p2, p3, p4, p5].forEach(function(p) {
  console.log(p, p instanceof Person);  // 모두 Person 인스턴스임
});

var Constructor = function(name) {  
  this.name = name;  // 생성자의 인자로 받은 name을 인스턴스 프로퍼티로 저장
};
Constructor.prototype.method1 = function() {};  // 프로토타입에 method1 메서드 추가
Constructor.prototype.property1 = 'Constructor Prototype Property';  // 프로토타입에 프로퍼티 추가

var instance = new Constructor('Instance');  // Constructor를 이용해 인스턴스 생성
console.dir(Constructor);  // 생성자 자체 구조 출력 (생성자 함수의 prototype 확인 가능)
console.dir(instance);  // 생성된 인스턴스 구조 출력 (프로토타입 체인 확인 가능)

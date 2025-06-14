var Person = function(name) {  // Person이라는 생성자 함수를 선언 (생성자 함수 패턴)
  this._name = name;  // 생성된 객체에 _name 프로퍼티를 저장
};
Person.prototype.getName = function() {  // 프로토타입에 메서드 추가 (공유 메서드)
  return this._name;  // _name을 반환하는 함수
};

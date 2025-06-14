var extendClass1 = function(SuperClass, SubClass, subMethods) {
  SubClass.prototype = new SuperClass();  // 프로토타입 상속
  for (var prop in SubClass.prototype) {  // 상속받은 인스턴스 프로퍼티 삭제
    if (SubClass.prototype.hasOwnProperty(prop)) {
      delete SubClass.prototype[prop];
    }
  }
  if (subMethods) {  // 서브클래스 메서드 추가
    for (var method in subMethods) {
      SubClass.prototype[method] = subMethods[method];
    }
  }
  Object.freeze(SubClass.prototype);  // 프로토타입 수정 방지
  return SubClass;
};

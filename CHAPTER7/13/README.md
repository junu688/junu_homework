var extendClass3 = function(SuperClass, SubClass, subMethods) {
  SubClass.prototype = Object.create(SuperClass.prototype);  // 정석적 프로토타입 상속
  SubClass.prototype.constructor = SubClass;  // constructor 정상 복구
  if (subMethods) {
    for (var method in subMethods) {
      SubClass.prototype[method] = subMethods[method];
    }
  }
  Object.freeze(SubClass.prototype);
  return SubClass;
};

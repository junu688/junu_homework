var extendClass = function(SuperClass, SubClass, subMethods) {
  SubClass.prototype = Object.create(SuperClass.prototype);
  SubClass.prototype.constructor = SubClass;
  SubClass.prototype.super = function(propName) {  // super 기능 추가
    var self = this;
    if (!propName)
      return function() { SuperClass.apply(self, arguments); };  // 생성자 호출
    var prop = SuperClass.prototype[propName];
    if (typeof prop !== 'function') return prop;
    return function() { return prop.apply(self, arguments); };  // 메서드 호출
  };
  if (subMethods) {
    for (var method in subMethods) {
      SubClass.prototype[method] = subMethods[method];
    }
  }
  Object.freeze(SubClass.prototype);
  return SubClass;
};

var extendClass2 = (function() {
  var Bridge = function() {};  // 빈 브릿지 생성자 생성 (프로토타입만 연결)
  return function(SuperClass, SubClass, subMethods) {
    Bridge.prototype = SuperClass.prototype;
    SubClass.prototype = new Bridge();  // 프로토타입만 상속
    if (subMethods) {
      for (var method in subMethods) {
        SubClass.prototype[method] = subMethods[method];
      }
    }
    Object.freeze(SubClass.prototype);
    return SubClass;
  };
})();

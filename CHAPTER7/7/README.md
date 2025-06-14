var Rectangle = function(width, height) {
  this.width = width;
  this.height = height;
};
Rectangle.prototype.getArea = function() {
  return this.width * this.height;
};
var rect = new Rectangle(3, 4);
console.log(rect.getArea()); // 12

var Square = function(width) {
  Rectangle.call(this, width, width);  // 부모 생성자 호출 (생성자 상속)
};
Square.prototype = new Rectangle();  // 프로토타입 상속 (고전적 상속 방식)

var sq = new Square(5);
console.log(sq.getArea()); // 25

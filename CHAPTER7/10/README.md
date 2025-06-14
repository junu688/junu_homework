var Rectangle = function(width, height) {
  this.width = width;
  this.height = height;
};
Rectangle.prototype.getArea = function() {
  return this.width * this.height;
};
var Square = function(width) {
  Rectangle.call(this, width, width);
};
Square.prototype = Object.create(Rectangle.prototype);  // Object.create()로 프로토타입만 상속
Object.freeze(Square.prototype);  // 불변성 유지

var sq = new Square(5);
console.log(sq.getArea()); // 25

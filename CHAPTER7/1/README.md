var Rectangle = function(width, height) {  
  this.width = width;  // 생성자: width와 height를 프로퍼티로 저장
  this.height = height;
};
Rectangle.prototype.getArea = function() {
  return this.width * this.height;  // 면적 반환 메서드
};
Rectangle.isRectangle = function(instance) {  // 정적 메서드: Rectangle 판별용
  return (
    instance instanceof Rectangle && instance.width > 0 && instance.height > 0
  );
};

var rect1 = new Rectangle(3, 4);
console.log(rect1.getArea()); // 12 (O)
console.log(rect1.isRectangle(rect1)); // Error (X) → 정적 메서드는 클래스명으로 호출해야 함
console.log(Rectangle.isRectangle(rect1)); // true

var Rectangle = class {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }
  getArea() {
    return this.width * this.height;
  }
};
var Square = class extends Rectangle {  // ES6 extends로 상속
  constructor(width) {
    super(width, width);  // super()로 부모 생성자 호출
  }
  getArea() {
    console.log('size is :', super.getArea());  // super로 부모 메서드 호출
  }
};

var arr = [1, 2];  // 배열 선언
Array.prototype.constructor === Array;  // true (Array 프로토타입의 constructor는 Array)
arr.__proto__.constructor === Array;  // true (arr의 __proto__는 Array.prototype)
arr.constructor === Array;  // true (인스턴스에서도 constructor로 접근 가능)

var arr2 = new arr.constructor(3, 4);  // constructor를 활용해 새로운 배열 생성
console.log(arr2);  // [3, 4]

var arr = [1, 2];
Array.prototype.toString.call(arr);  // 1,2 → 기본 배열 toString()
Object.prototype.toString.call(arr);  // [object Array] → 정확한 타입 확인용
arr.toString();  // 1,2

arr.toString = function() {
  return this.join('_');  // toString 오버라이드 → 커스텀 문자열 반환
};
arr.toString();  // 1_2

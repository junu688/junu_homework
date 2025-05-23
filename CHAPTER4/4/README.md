// 4-4: map의 인자 순서를 잘못 지정한 경우
// 첫 번째 인자를 index로 잘못 해석하여 예상치 못한 결과 발생
// 실제로는 index = 요소값, currentValue = 인덱스
var newArr2 = [10, 20, 30].map(function(index, currentValue) {
  console.log(index, currentValue);
  return currentValue + 5; // index가 아닌 인덱스가 더해져 5, 6, 7 반환
});
console.log(newArr2); // [5, 6, 7]
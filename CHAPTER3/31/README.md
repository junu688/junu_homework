### 3-31

```js
Array.prototype.forEach(callback[, thisArg])
Array.prototype.map(callback[, thisArg])
Array.prototype.filter(callback[, thisArg])
Array.prototype.some(callback[, thisArg])
Array.prototype.every(callback[, thisArg])
Array.prototype.find(callback[, thisArg])
Array.prototype.findIndex(callback[, thisArg])
Array.prototype.flatMap(callback[, thisArg])
Array.prototype.from(arrayLike[, callback[, thisArg]])
Set.prototype.forEach(callback[, thisArg])
Map.prototype.forEach(callback[, thisArg])// 많은 배열/컬렉션 메서드는 thisArg를 두 번째 인자로 받아 **콜백 내부의 this**를 지정 가능 this 문제를 피하려면 꼭 thisArg를 활용하거나 화살표 함수를 쓰는 것이 좋음
```

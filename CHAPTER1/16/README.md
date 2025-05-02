### 1-16

```js
var copyObjectDeep = function(target) {
  var result = {};
  if (typeof target === 'object' && target !== null) {
    for (var prop in target) { // 객체, 배열 이면 재귀적 복사
      result[prop] = copyObjectDeep(target[prop]);
    }
  } else { // 원시값 그대로 복사
    result = target;
  }
  return result;
};
```
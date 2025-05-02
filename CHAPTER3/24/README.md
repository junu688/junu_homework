### 3-24

```js
const numbers = [10, 20, 3, 16, 45];
const max = Math.max(...numbers);
const min = Math.min(...numbers);
console.log(max, min); // 45 3전개 연산자(...)로 배열을 개별 인자로 변환 apply보다 간단한 최신 문법
```
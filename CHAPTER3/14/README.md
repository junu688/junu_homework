### 3-14

```js
var func = function(a, b, c) {
  console.log(this, a, b, c);
};

func(1, 2, 3); // Window{ ... } 1 2 3
func.call({ x: 1 }, 4, 5, 6); // { x: 1 } 4 5 6 call은 this를 첫 번째 인자로 직접 지정나머지 인자는 함수의 매개변수로 전달됨
```

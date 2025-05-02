### 3-8

```js
var obj = {
  methodA: function() {
    console.log(this);
  },
  inner: {
    methodB: function() {
      console.log(this);
    },
  },
};
obj.methodA(); // { methodA: f, inner: {...} }    ( === obj)
obj['methodA'](); // { methodA: f, inner: {...} } ( === obj)

obj.inner.methodB(); // { methodB: f }            ( === obj.inner)
obj.inner['methodB'](); // { methodB: f }         ( === obj.inner)
obj['inner'].methodB(); // { methodB: f }         ( === obj.inner)
obj['inner']['methodB'](); // { methodB: f }      ( === obj.inner)this는 호출된 객체를 참조합니다.obj.methodA()처럼 호출하면 this === objobj.inner.methodB()처럼 호출하면 this === obj.inner[] 표기법을 써도 마찬가지입니다. this는 함수가 어떻게 호출되었는지에 따라 결정되며, 작성 방식과는 무관합니다.
```
### 1-11

```js
var user = {
  name: 'Jaenam',
  gender: 'male',
};

var changeName = function(user, newName) {
  return {
    name: newName, // 새로운 객체 생성 (기존 user는 변경되지 않는다)
    gender: user.gender,
  };
};

var user2 = changeName(user, 'Jung');

if (user !== user2) {
  console.log('유저 정보가 변경되었습니다.'); // 출력됨
}
console.log(user.name, user2.name); // Jaenam Jung
console.log(user === user2); // false
```
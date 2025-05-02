### 1-10

```js
var user = {
  name: 'Jaenam',
  gender: 'male',
};

var changeName = function(user, newName) {
  var newUser = user; //user 객체를 참조 복사
  newUser.name = newName; // name 변경되므로 user도 변경됨
  return newUser;
};

var user2 = changeName(user, 'Jung');

if (user !== user2) {
  console.log('유저 정보가 변경되었습니다.'); // 출력되지 않음. 
}
console.log(user.name, user2.name); // Jung Jung
console.log(user === user2); // true
```
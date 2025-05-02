### 1-14

```js
var copyObject = function(target) {
  var result = {};
  for (var prop in target) {
    result[prop] = target[prop];
  }
  return result;
};

var user = {
  name: 'Jaenam',
  urls: {
    portfolio: 'http://github.com/abc',
    blog: 'http://blog.com',
    facebook: 'http://facebook.com/abc',
  },
};
var user2 = copyObject(user);// name은 별개, urls는 참조공유
user2.name = 'Jung';

console.log(user.name === user2.name); // false 문자열 값 다름

user.urls.portfolio = 'http://portfolio.com';
console.log(user.urls.portfolio === user2.urls.portfolio); // true 같은 객체 참조

user2.urls.blog = '';
console.log(user.urls.blog === user2.urls.blog); // true 같은 객체 공유
```
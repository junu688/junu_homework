### 1-15

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

var user2 = copyObject(user); //user 객체 얕은 복사
user2.urls = copyObject(user.urls); //urls도 별도로 복사

user.urls.portfolio = 'http://portfolio.com';
console.log(user.urls.portfolio === user2.urls.portfolio); // false 서로다른 객체임

user2.urls.blog = '';
console.log(user.urls.blog === user2.urls.blog); // false 서로 다른 복사본임
```
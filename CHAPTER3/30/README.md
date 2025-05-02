### 3-30

```js
var report = {
  sum: 0,
  count: 0,
  add: function() {
    var args = Array.prototype.slice.call(arguments);
    args.forEach(function(entry) {
      this.sum += entry;
      ++this.count;
    }, this);
  },
  average: function() {
    return this.sum / this.count;
  },
};
report.add(60, 85, 95);// forEach에 this를 두 번째 인자로 넘겨 내부에서 this.sum 사용 가능콜백 안에서 this가 report 객체를 유지함
console.log(report.sum, report.count, report.average()); // 240 3 80
```
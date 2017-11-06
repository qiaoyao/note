# JS获取几天前的日期

```javascript
function getBeforeDate(n) {
    var d = new Date();
    d.setTime(d.getTime() - n * 60 * 60 * 24 * 1000); // 毫秒
    var year = d.getFullYear();
    var mon = d.getMonth() + 1;
    var day = d.getDate();

    s = year + "-" + (mon < 10 ? ('0' + mon) : mon) + "-" + (day < 10 ? ('0' + day) : day);
    return s;
}

console.log(getBeforeDate(0)); //当前日期 2017-11-06
console.log(getBeforeDate(1)); //昨天日期 2017-11-05
console.log(getBeforeDate(36));//指定日期 2017-10-01
```

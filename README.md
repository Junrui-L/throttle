# throttle
节流函数
```javascript```
var throttle = function (fn, delay) {
    var timer = null;
    return function () {
        var context = this, args = arguments;
        clearTimeout(timer);
        timer = setTimeout(function () {
            fn.apply(context, args);//context调用fn的方法，指针指向了fn
        }, delay);
    }
}
```

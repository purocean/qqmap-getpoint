# 腾讯地图坐标拾取器

解决 Web 开发中选择坐标位置问题

代码来自 https://lbs.qq.com/tool/getpoint/getpoint.html
在这个基础上增加了自定义Key，初始化位置，回调函数功能

## 使用
```html
<script>
function init() {
    var map = document.getElementById('qq-map-iframe');
    var lat = 30.65089;
    var lng = 104.07572;
    var callback = function (val) {
        console.log(val);
    };

    // 初始化位置和回调函数
    if (map.contentWindow.init) {
        map.contentWindow.init(callback, lat, lng);
    }
}
</script>

<iframe id="qq-map-iframe" src="getpoint.html?key=QQ_MAP_KEY" frameborder="0" width="100%" height="620" onload="init()"></iframe>
```

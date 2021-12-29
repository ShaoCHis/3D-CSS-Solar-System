# 3D-Solar-System
demo : http://139.196.194.51:8082(由于服务器的网络限制，所以服务器端并未集成wikipedia的API，暂未实现搜索功能）

## Technology｜技术
```
1｜采用原生HTML、JS、CSS进行开发
2｜构造3D效果采用了transform：rotateX（），即按照xyz轴中的一个x轴进行一定程度的旋转，构造3D效果
3｜缩放等动画利用@keyframes注解与animation-iteration-count和animation-timing-function属性实现
4｜集成wikipedia采用XMLHTTPREQUEST进行请求，API为restAPI，地址为：
   xhr.open('get', '//zh.wikipedia.org/api/rest_v1/page/summary/' + input);input为用户输入；
5｜信息查询浮框采用计时器，搜索成功后作为浮框显示科普内容，在计时20s后自动消失；
```

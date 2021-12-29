# 3D-Solar-System
demo : http://139.196.194.51:8082
(由于服务器的网络限制，所以服务器端并未集成wikipedia的API，暂未实现搜索功能）

## Technology｜技术
```
1｜采用原生HTML、JS、CSS进行开发
2｜构造3D效果采用了transform：rotateX（），即按照xyz轴中的一个x轴进行一定程度的旋转，构造3D效果
3｜缩放等动画利用@keyframes注解与animation-iteration-count和animation-timing-function属性实现
4｜集成wikipedia采用XMLHTTPREQUEST进行请求，API为restAPI，地址为：
   xhr.open('get', '//zh.wikipedia.org/api/rest_v1/page/summary/' + input);input为用户输入；
5｜信息查询浮框采用计时器，搜索成功后作为浮框显示科普内容，在计时20s后自动消失；
```

## AboutThisSystem｜关于项目使用
```
1|首页显示太阳系中八大行星围绕太阳旋转的动态展示（通过设置公转周期可以使行星的速度趋近于真实情况下行星的公转周期）
  同时，行星的轨迹由圆形轨道表示；行星沿着圆形轨道进行移动
2|右侧按钮定义分别如下：
   1）2D按钮，单选框的选择，可以选择2D视图和3D视图的转化，2D视图对应平面视图，3D视图则是旋转角度呈现3D展示
   2）+单选框作为动态和静态的选择，动态选择则是按照距离太阳的距离进行动态旋转；静态视图则是按照距离对八大行星进行排序，静态显示其外观
   3）speed按钮则是按照行星的速度进行展示；
   4）size按钮则是按照行星的相对大小进行显示
   5）distance按钮则是按照行星距离太阳的距离进行显示
   6）search按钮则是进行搜索操作（服务端未集成），搜索结果以悬浮框进行展示，计时20s后自动消失
3|底部按钮即为八大行星的名称进行点击可以显示八大行星公转速度和名称（自定义内容，可以修改）
```

## 系统介绍
本网页主要是进行太阳系的科普工作，wikipedia的API需要进行一定的网络代理才可以进行访问。

## Tips
跨域问题未在代码中解决，因为服务器部署可以使用nginx解决跨域问题，所以代码中未解决，如需跨域请参照以下教程：
```
以Chrome为例：
   windows下：
      C:\Users\Administrator\AppData\Local\Google\Chrome\Application\chrome.exe --disable-web-security --user-data-dir=C:\Program Files (x86)\Google\Chrome\Application
      将文件目录替换为自己的文件目录，主要修改为--disable～（关闭谷歌的跨域）
   macOS/Linux下：
      在一个文件目录下创建一个Chrome的文件夹，然后使用指令open -n /Applications/Google\ Chrome.app/ --args --disable-web-security  --user-data-            dir=/Users/shentao/Documents/MyChrome，将dir=后面的文件目录替换为自己新建的Chrome文件目录即可
```

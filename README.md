## 目录
* #### [开发规范](#开发规范-1)
* #### [开发注意事项](#开发注意事项-1)
* #### [HTML <head>](#html-head-1)
* #### [CSS相关](#css相关-1)
  1. [编写CSS规范](#1编写css规范)
  2. [单行溢出省略号](#2单行溢出省略号)
  3. [多行溢出省略号](#3多行溢出省略号)
  4. [placeholder样式](#4placeholder样式)
  5. [渐变](#5渐变)
  6. [flex页脚置底(兼容至ie10)](#6flex页脚置底兼容至ie10)
  7. [css三角形](#7css三角形)
  8. [tab常用响应式不转行，可左右拉动](#8tab常用响应式不转行可左右拉动)
  9. [让背景图随DIV变化，且居中不变形](#9让背景图随div变化且居中不变形)
  10. [重置样式](#10重置样式)
  11. [div内容垂直布局](#11div垂直布局)
  12. [input框在ios下的内阴影问题](#12input框在ios下的内阴影问题)
  13. [去掉ios下可点元素的灰色块](#13去掉ios下可点元素的灰色块)
  14. [flex制作栅格布局](#14flex制作栅格布局)
  15. [关于移动端下的布局](#15关于移动端下的布局)
* #### [JS相关](#js相关-1)
  1. [获取URL参数值](#1获取url参数值)
  2. [头部提取之后，导航跳转添加对应的active ](#2头部提取之后导航跳转添加对应的active)
  3. [swiper常用参数](#3swiper常用参数)
  4. [锚链接平滑移动](#4锚链接平滑移动)
  5. [数字递增](#5数字递增)
  6. [侧边栏吸边](#6侧边栏吸边)
  7. [AJAX请求](#7ajax请求)
  8. [缓存相关操作](#8缓存相关操作)
  9. [页面向下滚动头部加阴影](#9页面向下滚动头部加阴影)
  10. [跨域](#10跨域)
* #### [Vue相关](#vue相关-1)
  1. [使用sass](#1使用sass)
  2. [vue数据遍历后进行初始化](#2vue数据遍历后进行初始化)
  3. [vue中常用图片上传](#3vue中常用图片上传)
  4. [vue中进行跨域代理及发布注意事项](#4vue中进行跨域代理及发布注意事项)
  5. [使用material-icons](#5使用material-icons)
  6. [监听滚动条到底部](#6监听滚动条到底部)
  7. [关于Vue打包之后文件路径出错的问题](#7关于vue打包之后文件路径出错的问题)
  8. [使用jquery](#8使用jquery)
  9. [组件之间的通信](#9组件之间的通信)
##### [npm使用淘宝镜像](#npm使用淘宝镜像-1)


## 开发规范
<!-- > 不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。     -->
[内容来源 -> http://codeguide.bootcss.com/](http://codeguide.bootcss.com/)

## 开发注意事项

1、编码尽量简洁、对齐，避免无用标签和错误的写法；

2、插件的版本是否统一；

3、全局样式用谁的；

4、样式表的结构是不是继承的写法，会不会互相干扰；

5、样式优先级如下：    
` 通用选择器 * < 元素(类型)选择器 < 类选择器 < 属性选择器 < 伪类 < ID 选择器 < 内联样式 `

6、团队协作下使用Git了吗；

7、不同团队开发，在关于复用的组件以及全局的变量是否有进行沟通；

8、常规SEO：a加title、 rel="nofollow"，img加alt，logo用h1包裹...


## HTML head
```html
<meta charset="UTF-8">
<!-- 设置文档宽度、是否缩放 -->
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<!-- 优先使用IE最新版本和Chrome -->
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
<title></title>
<!-- 关键字 -->
<meta name="keywords" content="">
<!-- 描述 -->
<meta name="description" content="">
<!--[if lt IE 9]>
<script src="https://cdn.staticfile.org/html5shiv/r29/html5.min.js"></script>
<script src="https://cdn.staticfile.org/respond.js/1.4.2/respond.min.js"></script>
<![endif]-->
<!--[if lte IE 8]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!--[if lte IE 7]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!--[if lte IE 6]>
<p style="background:#000;text-align: center;color:#fff;font-size: 16px; line-height: 25px;">你的浏览器太老了，请到<a href="http://browsehappy.com" style="color:#ddd">这里</a>更新，以获取最佳的体验</p>
<![endif]-->
<!-- 360使用Google Chrome Frame -->
<meta name="renderer" content="webkit">
<!-- 百度禁止转码 -->
<meta http-equiv="Cache-Control" content="no-siteapp">
<!-- 定义网页搜索引擎索引方式 -->
<meta name="robots" content="index,follow">
<!-- ios设备 -->
<!-- 添加到主屏后的标题 -->
<meta name="apple-mobile-web-app-title" content="">
<!-- 是否启用WebApp全屏模式 -->
<meta content="yes" name="apple-mobile-web-app-capable">
<meta content="yes" name="apple-touch-fullscreen">
<!-- 设置状态栏的背景颜色 -->
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<!-- Android theme-color用来控制选项卡颜色。 -->
<meta name="theme-color" content="#747474">
<meta name="mobile-web-app-capable" content="yes">
<!-- 关闭chrome浏览器下翻译插件 -->
<meta name="google" value="notranslate" />
<!-- uc强制竖屏 -->
<meta name="screen-orientation" content="portrait">
<!-- QQ强制竖屏 -->
<meta name="x5-orientation" content="portrait">
<!-- UC强制全屏 -->
<meta name="full-screen" content="yes">
<!-- QQ强制全屏 -->
<meta name="x5-fullscreen" content="true">
<!-- UC应用模式 -->
<meta name="browsermode" content="application">
<!-- QQ应用模式 -->
<meta name="x5-page-mode" content="app">
```

## CSS相关
### 1、编写CSS规范
不管项目是不是自己一个人独立开发，我们都应该去规范自己的代码，哪怕是一个很小的项目，如果每个人都把规范做到极致，所有事情都会变得更简单。

在我以往遇到的大部分开发中，用Git合并项目时，遇到最多的冲突就是样式表用来用去不知道在用谁的，改来改去还不好改，特别是开发人员还不坐在一起开发的时候；

如果我们把样式拆分成模块会方便很多，下面是一些例子，譬如在用Less的时候：

![Less目录](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/mulu.png)

这样的目录一目了然哪个文件是哪个部分的

将经常用到的样式单独定义写到_variable.less里

![全局变量](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/variable.png)

然后再把所有的文件引入到main.less

![整合less](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/style.png)

当然预编译处理的样式表文件需要配合webpack这样的打包工具才能更加高效的发挥它的作用，整合并压缩资源文件等

就算是用的原生css来写，在class上写明哪个文件并添加注释，或者在class命名上规范一下（譬如 关于我们： .aboutPage），这样看起来会更清晰

![原生css](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/css.png)

只是用Less举个例子把方法说清楚，至于用原生css还是用css的预编译处理语言这里不作讨论

但是显然用预编译处理语言在开发和贴近规范上会更方便一些，这是推荐使用的。    
如果我们的样式表都是通过嵌套规则来一个个继承的，不管你用哪个都不会有任何冲突，因为彼此之间的关系是很清晰的。

### 2、单行溢出省略号
```css
.demo{
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

### 3、多行溢出省略号
```css
.demo{
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  /* max-height: ??; */
}
```

### 4、placeholder样式
```css
input::-webkit-input-placeholder{
  color:red;
}
input::-moz-placeholder{
  color:red;
}
input:-moz-placeholder{
  color:red;
}
input:-ms-input-placeholder{
  color:red;
}
```
 
### 5、渐变
**从上到下**
```css
.demo{
  background: -webkit-linear-gradient(red, blue);
  background: -o-linear-gradient(red, blue);
  background: -moz-linear-gradient(red, blue);
  background: linear-gradient(red, blue);
}
```
 
**从左到右**
```css
.demo{
  background: linear-gradient(to right, red , blue);
}
```
 
**角度**
```css
.demo{
  background: linear-gradient(to bottom right, red , blue);  /*左上角至右下角*/
  background: linear-gradient(180deg, red, blue);  /*指定角度*/
}
```
 
**多个颜色**
```css
.demo{
  background: linear-gradient(red, green, blue);
}
```
 
### 6、flex页脚置底(兼容至ie10)
```html
<body>
  <header></header>
  <main></main>
  <footer></footer>
</body>
```
```css
html{
  height: 100%;
}
body{
	height: 100%;
	min-height: 100%;
	display: flex;
	flex-direction: column;
}
.main{
	flex: 1 0 auto;
}
.footer{
	flex: 0 0 auto;
}
```

### 7、css三角形
[内容来源 -> http://www.jb51.net/article/42513.htm](http://www.jb51.net/article/42513.htm)

### 8、tab常用响应式不转行，可左右拉动
放在容器里的样式
```css
.demo{
  white-space: nowrap;
  overflow-x: auto;
  display: flex;
  overflow-y: hidden;
}
```

### 9、让背景图随DIV变化，且居中不变形
```css
.demo{
  background-image: url("../images/index/banner.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  background-position: center center;
}
```

### 10、重置样式
[内容来源 -> https://meyerweb.com/eric/tools/css/reset/index.html](https://meyerweb.com/eric/tools/css/reset/index.html)
```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

### 11、div垂直布局
```css
.demo{
  display: table-cell;
  vertical-align: middle;
}
```

### 12、input框在ios下的内阴影问题
```css
input{
  -webkit-appearance: none;
}
```

### 13、去掉ios下可点元素的灰色块
```css
.demo{
  -webkit-tap-highlight-color: transparent;
}
```

### 14、flex制作栅格布局
```
┌─flexbox─────────────────────┐
│ ┌─box-row─────────────────┐ │
│ │ ┌─box-col─┐ ┌───┐ ┌───┐ │ │
│ │ │ 3 │ │ 3 │ │ 3 │ │ 3 │ │ │
│ │ └───┘ └───┘ └───┘ └───┘ │ │
│ └─────────────────────────┘ │
└─────────────────────────────┘
```
```html
<div class="flexbox">
  <div class="box-row">
    <div class="box-col"> 3 </div>
    <div class="box-col"> 3 </div>
    <div class="box-col"> 3 </div>
    <div class="box-col"> 3 </div>
  </div>
</div>
```
```scss
.flexbox{
  overflow: hidden;
  .box-row{
    margin: 0 -10px;
    display: flex;
    flex-wrap: wrap;
    // align-items: flex-start;
  }
  .box-col{
    flex: 0 0 25%;
    min-width: 25%;
    padding: 0 10px;
    margin: 0 0 15px;
  }
}
```

### 15、关于移动端下的布局
**在布局上我个人不建议使用position: fixed来达到固定的效果**

```
┌─page──────────────────────────┐
│ ┌─header────────────────────┐ │
│ │ <          ---          + │ │
│ └───────────────────────────┘ │
│ ┌─page-content──────────────┐ │
│ │                           │ │
│ │ ...                       │ │
│ │                           │ │
│ │                           │ │
│ │                           │ │
│ │                           │ │
│ ┌─tabbar──────┬──────┬──────┐ │
│ │  --  │  --  │  --  │  --  │ │
│ └──────┴──────┴──────┴──────┘ │
└───────────────────────────────┘
```
```html
<div class="page">
  <div class="header"></div>
  <div class="page-contenr">
    ...
  </div>
  <div class="tabbar"></div>
</div>
```
```css
.page{
  position: absolute;
  z-index: 100;
  background-color: #f5f5f5;
  overflow: hidden;
  width: 100%;
  height: 100%;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  box-sizing: border-box;
}
.header{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 50px;
  box-sizing: border-box;
  z-index: 100;
}
.page-content{
  padding: 50px 0;
  height: 100%;
  overflow: auto;
  box-sizing: border-box;
  -webkit-overflow-scrolling:touch;
}
.tabbar{
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 50px;
  z-index: 100;
}
```

## JS相关
### 1、获取URL参数值
获取URL的参数的值。
```js
function getQueryString(name) {
  var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)", "i");
  var r = window.location.search.substr(1).match(reg);
  if (r != null) return unescape(r[2]); return null;
}
```

### 2、头部提取之后，导航跳转添加对应的active
添加到提取的header.html中
```js
$(".navbar-nav a").each(function(){
  $this = $(this);
  if($this[0].href==String(window.location)){
    $(".navbar-nav li").removeClass("active");
    $this.parent("li").addClass("active");
  }
});
```

### 3、swiper常用参数
```html
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
  </div>
  <!-- 如果需要分页器 -->
  <div class="swiper-pagination"></div>
  
  <!-- 如果需要导航按钮 -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
  
  <!-- 如果需要滚动条 -->
  <div class="swiper-scrollbar"></div>
</div>
```
```js
var Swiper1 = new Swiper('.swiper-container', {
  speed: 300,                     //切换速度
  autoplay: {                     //自动播放
    delay: 3000,                  //间隔时间
    disableOnInteraction: false,  //用户操作swiper之后，是否禁止autoplay。
  },
  direction : 'horizontal',       //滑动方向，'horizontal'为横向，'vertical'为竖向
  slidesPerView: 4,               //一屏显示多少个
  slidesPerColumn: 2,             //显示2行
  spaceBetween: 30,               //每个之间的间距
  autoHeight: true,               //高度随内容变化
  watchOverflow: true,            //当没有足够的slide切换时，swiper会失效且隐藏导航
  noSwiping : true,               //使该slide无法拖动，希望文字被选中时可以考虑使用
  noSwipingClass : 'no-swiper',
  centeredSlides : true,          //居中显示
  loop: true,                     //头尾循环
  observer: true,                 //修改swiper自己或子元素时，自动初始化swiper 
  observeParents: true,           //修改swiper的父元素时，自动初始化swiper
  pagination: {                   //分页器
    el: '.swiper-pagination',
    clickable :true               //允许点击分页器切换
  },
  navigation: {                   //前进后退按钮
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev'
  },
  breakpoints: {                  //响应式设置
    1200: {
      slidesPerView: 4,
      spaceBetween: 35
    },
    992: {
      slidesPerView: 3,
      spaceBetween: 35
    },
    768: {
      slidesPerView: 2,
      spaceBetween: 35
    },
    400: {
      slidesPerView: 1,
      spaceBetween: 35
    }
  }
})
```

### 4、锚链接平滑移动
```js
$('.navbar-nav a[href*=#]').click(function() {  
  if (location.pathname.replace(/^\//, '') == this.pathname.replace(/^\//, '') && location.hostname == this.hostname) {  
      var $target = $(this.hash);  
      $target = $target.length && $target || $('[name=' + this.hash.slice(1) + ']');  
      if ($target.length) {  
        var targetOffset = $target.offset().top;  
        $('html,body').animate({  
          scrollTop: targetOffset  
        },700);  
        return false;  
      }  
  }  
});
```

### 5、数字递增
```html
<div id="id">
  <p class="incrementing" data-to="100" data-speed="1500">100</p>
</div>
```
```js
//数字递增
var wrapTop = $("#id").offset().top;
var istrue = true;
$(window).on("scroll",
function() {
  var s = $(window).scrollTop();
  if (s > wrapTop - 600 && istrue) {
    $(".incrementing").each(count);
    function count(a) {
      var b = $(this);
      a = $.extend({},
      a || {},
      b.data("countToOptions") || {});
      b.countTo(a)
    };
    istrue = false;
  };
})
//设置计数
$.fn.countTo = function (options) {
  options = options || {};
  return $(this).each(function () {
    //当前元素的选项
    var settings = $.extend({}, $.fn.countTo.defaults, {
      from:            $(this).data('from'),
      to:              $(this).data('to'),
      speed:           $(this).data('speed'),
      refreshInterval: $(this).data('refresh-interval'),
      decimals:        $(this).data('decimals')
    }, options);
    //更新值
    var loops = Math.ceil(settings.speed / settings.refreshInterval),
        increment = (settings.to - settings.from) / loops;
    //更改应用和变量
    var self = this,
    $self = $(this),
    loopCount = 0,
    value = settings.from,
    data = $self.data('countTo') || {};
    $self.data('countTo', data);
    //如果有间断，找到并清除
    if (data.interval) {
      clearInterval(data.interval);
    };
    data.interval = setInterval(updateTimer, settings.refreshInterval);
    //初始化起始值
    render(value);
    function updateTimer() {
      value += increment;
      loopCount++;
      render(value);
      if (typeof(settings.onUpdate) == 'function') {
        settings.onUpdate.call(self, value);
      }
      if (loopCount >= loops) {
        //移出间隔
        $self.removeData('countTo');
        clearInterval(data.interval);
        value = settings.to;
        if (typeof(settings.onComplete) == 'function') {
          settings.onComplete.call(self, value);
        }
      }
    }
    function render(value) {
      var formattedValue = settings.formatter.call(self, value, settings);
      $self.html(formattedValue);
    }
  });
};
$.fn.countTo.defaults={
  from:0,               //数字开始的值
  to:0,                 //数字结束的值
  speed:1000,           //设置步长的时间
  refreshInterval:100,  //隔间值
  decimals:0,           //显示小位数
  formatter: formatter, //渲染之前格式化
  onUpdate:null,        //每次更新前的回调方法
  onComplete:null       //完成更新的回调方法
};
function formatter(value, settings){
  return value.toFixed(settings.decimals);
}
//自定义格式
$('.incrementing').data('countToOptions',{
  formmatter:function(value, options){
    return value.toFixed(options.decimals).replace(/\B(?=(?:\d{3})+(?!\d))/g, ',');
  }
});
//定时器
$('.incrementing').each(count);
function count(options){
  var $this=$(this);
  options=$.extend({}, options||{}, $this.data('countToOptions')||{});
  $this.countTo(options);
}
```

### 6、侧边栏吸边
侧边栏吸内容的边： 下面例子 #backtop 是侧边栏

原理：（窗口宽度 - 内容块的宽度）/ 2 再减去 #backtop的宽度 就是 #backtop的right值

![侧边栏吸边](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/sidebar.jpg)

```css
#backtop{
  position: fixed;
  width: 110px;
  bottom: 0;
  opacity: 0;
  z-index: 100;
  transition: 0.3s;
}
#backtop.show{opacity: 1;}
```
```js
window.onload = function() {
  var _width = ($(window).width() - $(".container").width())/2;
      _width -= $("#backtop").width();
      _width -= 8   //与内容块之间的距离
      $("#backtop").css("right", _width);
      $("#backtop").addClass("show");
}
$(window).resize(function(){
  var _width = ($(window).width() - $(".container").width())/2;
  _width -= $("#backtop").width();
  _width -= 8
  $("#backtop").css("right", _width);
});
```

### 7、AJAX请求
```js
var json ={
  mid: '123',
  version_timestamp: '456'
}
$.ajax({
  url: '',
  type: 'post',
  dataType: 'json',
  data: json,
  beforeSend: function(){
    $("body").append(bodymask);
  },
  success: function(res){
    $(".bodymask").remove();
    for(var i=0;i<res.Data.length;i++){
      $('select[name="GetHotelList"]').append(
        $('<option value="'+ res.Data[i].Id +'">'+res.Data[i].Name+'</option>')
      )
    }
  }
})
```

### 8、缓存相关操作
```js
if(window.localStorage){
  //存储名字为name值为caibin的变量
  localStorage.setItem("name","caibin");

  //读取保存在localStorage对象里名为name的变量的值
  localStorage.getItem("name");

  // 检查localStorage里是否保存某个变量
  localStorage.hasOwnProperty('name'); // true false

  // 清空localStorage
  localStorage.clear();
｝
```
**对象类型转为包含JSON文本的字符串类型**
```js
SignPointList_Data = JSON.stringify(res.Data);
```
**转为JSON**
```js
SignPointList_Data = JSON.parse(SignPointList_Data);
```

### 9、页面向下滚动头部加阴影
```js
$(window).scroll(function(){
  if ($(document).scrollTop() > 0) {
    $('.header').addClass("shadow");
  } else {
    $('.header').removeClass("shadow");
  }
});
```

### 10、跨域
原因：

1. 发出去的请求不是本域的，协议、域名、端口，任何一个不一样浏览器就认为是跨域（反向代理）
2. 发出去的请求是XHR（XMLHttpRequest）请求，如果不是，即使跨域了也不报错（jsonp）
3. 浏览器限制，如果发现是跨域，浏览器就作校验，校验不通过就报错（禁止浏览器检查）

#### 10-1、反向代理
在hosts文件增加一个表示调用方的虚拟主机
```host
127.0.0.0 test.com
```

**nginx反向代理**
```
nginx-1.11.5
    │
    └─ conf
        │
        └─ vhost
            │
            └─ 新建一个配置文件 test.com.conf
```
test.com.conf 配置如下
```
server{
  listen 80;
  server_name test.com;

  location / {
    proxy_pass http://localhost:8080/;
  }

  location /api {
    proxy_pass http://example.com/api/;
  }
}
```

启动nginx，然后访问test.com
> start nginx.exe

暂停或者重载nginx
> nginx.exe -s stop

> nginx.exe -s reload

**apache反向代理**

找到apache虚拟主机的配置文件 httpd-vhost.conf ，添加配置，然后启动或重启apache
```
<VirtualHost *:80>
  ServerName test.com
  ErrorLog "logs/test.com-error.log"
  CustomLog "logs/test.com-access.log" common
  ProxyPass /api http://example.com/api/
  ProxyPass / http://localhost:8080/
</VirtualHost>
```

#### 10-2、jsonp
jsonp是json的一种补充使用方式，不是官方协议，主要是以script标签请求资源来解决跨域，是一种变通的解决方案，后台需要改动代码。

前后台约定如果参数里带了callback，那它就是一个jsonp请求，返回的时候就返回js代码而不是返回json，js代码的内容就是callback的值作为函数名，返回的数据作为函数的参数，这就是jsonp的实现原理。

jsonp的弊端：

1. 后台需要改动代码支持
2. 只支持GET请求，无法满足实际需求
3. 发送的不是XHR请求，XHR的新特性jsonp都没有，譬如异步和其他各种事件

```
$.ajax({
  url: '',
  type: 'post',
  dataType: 'jsonp',
  ...
```

#### 10-3、禁止浏览器检查
命令行参数启动chrome 禁止浏览器作校验
> chrome --disable-web-security --user-data-dir=g:\temp3

## Vue相关
### 1、使用sass
来源： [https://www.cnblogs.com/crazycode2/p/6535105.html](https://www.cnblogs.com/crazycode2/p/6535105.html)

>npm install --save-dev sass-loader style-loader css-loader

>npm install node-sass --save-dev

打开webpack.base.config.js在loaders里面加上  module -- rules
```js
  rules: [
    ......
    {
      test: /\.scss$/,
      loaders: ["style", "css", "sass"]
    }
  ]
```

然后使用scss
```html
<style lang="scss" src="@/styles/main.scss"></style>
```

### 2、vue数据遍历后进行初始化
```js
that.$axios.get(url).then(function (res) {
  that.rollingNew = res.data.content;
  //重点。在$nextTick方法内进行初始化
  that.$nextTick(() => {  // 下一个UI帧再初始化swiper
    that.initSwiper();
  });
  console.log(that.rollingNew)
})
```

### 3、vue中常用图片上传
```js
changeImg(e) {
  let token = localStorage.getItem('token')
  let _this = this
  let imgLimit = 1024
  let files = e.target.files
  let image = new Image()
  if (files.length > 0) {
    let dd = 0
    let timer = setInterval(function () {
      if (files.item(dd).type !== 'image/png' && files.item(dd).type !== 'image/jpeg' && files.item(dd).type !== 'image/gif') {
        return false
      }
      if (files.item(dd).size > imgLimit * 102400) {
      } else {
        image.src = window.URL.createObjectURL(files.item(dd))
        image.onload = function () {
          // 默认按比例压缩
          let w = image.width
          let h = image.height
          let scale = w / h
          w = 200
          h = w / scale
          // 默认图片质量为0.7，quality值越小，所绘制出的图像越模糊
          let quality = 0.7
          let canvas = document.createElement('canvas')
          let ctx = canvas.getContext('2d')
          // 创建属性节点
          let anw = document.createAttribute('width')
          anw.nodeValue = w
          let anh = document.createAttribute('height')
          anh.nodeValue = h
          canvas.setAttributeNode(anw)
          canvas.setAttributeNode(anh)
          ctx.drawImage(image, 0, 0, w, h)
          let ext = image.src.substring(image.src.lastIndexOf('.') + 1).toLowerCase()
          let base64 = canvas.toDataURL('image/' + ext, quality)
          if (_this.user.profileUrl !== null || _this.user.profileUrl !== undefined || _this.user.profileUrl !== '') {
            _this.user.profileUrl = base64
            //以上部分进行图片转换为base64

            //下面进行base64上传
            .....
            .....
            .....
          }
        }
      }
      if (dd < files.length - 1) {
        dd++
      } else {
        clearInterval(timer)
      }
    }, 1000)
  }
}
```
### 4、vue中进行跨域代理及发布注意事项
#### 1.在config文件中的index.js里，不管dev(开发环境下)与build(发布环境下)都应加入以下代码：
```js
proxyTable: {
  '/api': {
    target: 'http://23.101.9.18:8090/apelink',
    secure: false,
    changeOrigin: true,
  	pathRewrite: {
      '^/api': '/'
    }
  }
},
```
#### 2.在build文件夹中的webpack.prod.conf.js里，含义以下代码:
```js
new OptimizeCSSPlugin({
  cssProcessorOptions: config.build.productionSourceMap
  ? { safe: true, map: { inline: false } }
  : { safe: true }
}),
```
#### 此段代码需要注释掉，目前发现其对于-webkit-box-orient: vertical;会进行消除，
#### 注意：注释掉此代码后，webpack不会对css进行压缩，所以要在utils.js文件里下面代码中加入minimize: true，如下：
```js
const cssLoader = {
  loader: 'css-loader',
  options: {
      sourceMap: options.sourceMap,
      minimize: true
  }
}
```

### 5、使用material-icons
>npm install material-design-icons

main.js全局引入
```js
import 'material-design-icons/iconfont/material-icons.css'
```

### 6、监听滚动条到底部
```js
created(){
  window.onscroll = function(){
    //变量scrollTop是滚动条滚动时，距离顶部的距离
    var scrollTop = document.documentElement.scrollTop||document.body.scrollTop;
    //变量windowHeight是可视区的高度
    var windowHeight = document.documentElement.clientHeight || document.body.clientHeight;
    //变量scrollHeight是滚动条的总高度
    var scrollHeight = document.documentElement.scrollHeight||document.body.scrollHeight;
    //滚动条到底部的条件
    if(scrollTop+windowHeight==scrollHeight){
      //写后台加载数据的函数
      console.log("距顶部"+scrollTop+"可视区高度"+windowHeight+"滚动条总高度"+scrollHeight);
    }   
  }
}
```

或者是用div内滚动到90%
```html
<div v-on:scroll.passive="onScroll" ref="page">
  ......
</div>
```
```js
data () {
  return {
    finish: true
  }
}

onScroll () {
  var scrollTop = this.$refs.page.scrollTop;
  var windowHeight = this.$refs.page.clientHeight;
  var scrollHeight = this.$refs.page.scrollHeight;
  if((scrollTop / (scrollHeight - windowHeight) >= 0.9) && this.finish){
    this.finish = false
    this.$axios.post(url).then(res => {
      ...
      this.finish = true
    })
  }   
}
```

### 7、关于Vue打包之后文件路径出错的问题
#### 1.文件路径不对
找到config文件夹下的index.js文件修改一下位置;

![文件路径不对](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/vue1.png)

 build（上边还有个dev 是开发环境下的配置，不需要改动）下的 assetsPublicPath ：将'/'改为'./'

#### 2.背景图片路径不对

css中写的background-img的路径出错 需要找到build文件夹下的utils.js,修改一下位置

![背景图片路径不对](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/vue2.png)

加入红框内字段即可

### 8、使用jquery

>cnpm install jquery --save

在项目根目录下的build目录下找到**webpack.base.conf.js**文件，在开头使用以下代码引入webpack，因为该文件默认没有引用

```js
var webpack = require('webpack')
```

然后在**module.exports**中添加一段代码

```js
// 原有代码
resolve: {
  extensions: ['.js', '.vue', '.json'],
  alias: {
'vue$': 'vue/dist/vue.esm.js',
'@': resolve('src')
  }
},
// 添加代码+++++++++++++++
plugins: [
  new webpack.ProvidePlugin({
    $: "jquery",
    jQuery: "jquery",
    jquery: "jquery",
    "window.jQuery": "jquery"
  })
],
+++++++++++++++++++++++++
// 原有代码
module: {
  rules: [
// ......
  ]
}
```

最后在main.js里导入，然后重跑一下项目

```js
import 'jquery'
```

如果有 eslint 检查报错，改文件的module.exports中，为env添加一个键值对 jquery: true 就可以了

```js
env: {
  // 原有
  browser: true,
  // 添加
  jquery: true
}
```

### 9、组件之间的通信
[内容来源 -> https://segmentfault.com/a/1190000010530600?utm_source=tag-newest](https://segmentfault.com/a/1190000010530600?utm_source=tag-newest)

组件关系有下面三种：父-->子、子-->父、非父子

#### 9-1、父-->子

父向子传递数据通过props

```
**父组件代码**
<template>
    <header-box :title-txt="showTitleTxt"></header-box>
</template>
<script>
    import Header from './header'
    export default {
        name: 'index',
        components: {
            'header-box': Header
        },
        data () {
            return {
                showTitleTxt: '首页'
            }
        }
    }
</script>
```
```
**子组件代码**
<template>
    <header>
        {{thisTitleTxt}}
    </header>
</template>
<script>
    export default {
        name: 'header-box',
        props: {
            titleTxt: String
        },
        data () {
            return {
                thisTitleTxt: this.titleTxt
            }
        }
    }
</script>
```

#### 9-2、子-->父

子组件向父组件传递分为两种类型。
1. 子组件改变父组件传递的props（你会发现通过props中的Object类型参数传输数据，可以通过子组件改变数据内容。这种方式是可行的，但是不推荐使用，因为官方定义prop是单向绑定）
2. 通过$on和$emit

**通过props实现传递**
```
**父组件代码**
<template>
    <header-box :title-txt="showTitleTxt"></header-box>
</template>
<script>
    import Header from './header'
    export default {
        name: 'index',
        components: {
            'header-box': Header
        },
        data () {
            return {
                showTitleTxt: {
                    name: '首页'
                }
            }
        }
    }
</script>
```
```
**子组件代码**
<template>
    <header @click="changeTitleTxt">
        {{thisTitleTxt.name}}
    </header>
</template>
<script>
    export default {
        name: 'header-box',
        props: {
            titleTxt: Object
        },
        data () {
            return {
                thisTitleTxt: this.titleTxt.name
            }
        },
        metheds: {
            changeTitleTxt () {
                this.titleTxt.name = '切换'
            }
        }
    }
</script>
```

**通过$on,$emit**
```
**父组件代码**
<template>
    <div id="counter-event-example">
      <p>{{ total }}</p>
      <button-counter @increment="incrementTotal"></button-counter>
</div>
</template>
<script>
    import ButtonCounter from './buttonCounter'
    export default {
        name: 'index',
        components: {
            'button-conuter': ButtonCounter
        },
        data () {
            return {
                total: 0
            }
        },
        methods: {
            incrementTotal () {
                this.total++
            }
        }
    }
</script>
```
```
**子组件代码**
<template>
    <button @click="incrementCounter">{{counter}}</button>
</template>
<script>
    export default {
        name: 'button-counter',
        data () {
            return {
                counter: 0
            }
        },
        metheds: {
            incrementCounter () {
                this.$emit('increment')
                this.counter++
            }
        }
    }
</script>
```

#### 9-3、非父子
简单情况下我们可以通过使用一个空的Vue实例作为中央事件总线，（这里也可以使用app实例，而不需要新建一个空Vue实例）

```
**main.js**
let bus = new Vue()
Vue.prototype.bus = bus
```

或者

```
**main.js**
new Vue({
  el: '#app',
  router,
  template: '<App/>',
  components: { App },
  beforeCreate () {
    Vue.prototype.bus = this
  }
})
```

```
**header组件**
<template>
    <header @click="changeTitle">{{title}}</header>
</template>
<script>
export default {
    name: 'header',
    data () {
        return {
            title: '头部'
        }
    },
    methods: {
        changeTitle () {
            this.bus.$emit('toChangeTitle','首页')
        }
    }
}
</script>
```
```
**footer组件**
<template>
    <footer>{{txt}}</footer>
</template>
<script>
export default {
    name: 'footer',
    mounted () {
        this.bus.$on('toChangeTitle', function (title) {
            console.log(title)
        })
    },
    data () {
        return {
            txt: '尾部'
        }
    }
}
```

---

#### npm使用淘宝镜像
>npm install -g cnpm --registry=https://registry.npm.taobao.org

---

```
                                                       _ooOoo_
                                                      o8888888o
                                                      88" . "88
                                                      (| -_- |)
                                                      O\  =  /O
                                                   ____/`---'\____
                                                 .'  \\|     |//  `.
                                                /  \\|||  :  |||//  \
                                               /  _||||| -:- |||||-  \
                                               |   | \\\  -  /// |   |
                                               | \_|  ''\---/''  |   |
                                               \  .-\__  `-`  ___/-. /
                                             ___`. .'  /--.--\  `. . __
                                          ."" '<  `.___\_<|>_/___.'  >'"".
                                         | | :  `- \`.;`\ _ /`;.`/ - ` : | |
                                         \  \ `-.   \_ __\ /__ _/   .-` /  /
                                    ======`-.____`-.___\_____/___.-`____.-'======
                                                       `=---='
                                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
                                                 佛祖保佑    永无BUG


            ┌───┐   ┌───┬───┬───┬───┐ ┌───┬───┬───┬───┐ ┌───┬───┬───┬───┐ ┌───┬───┬───┐    ┌┐   ┌┐   ┌┐
            │Esc│   │ F1│ F2│ F3│ F4│ │ F5│ F6│ F7│ F8│ │ F9│F10│F11│F12│ │P/S│S L│P/B│    └┘   └┘   └┘
            └───┘   └───┴───┴───┴───┘ └───┴───┴───┴───┘ └───┴───┴───┴───┘ └───┴───┴───┘             
            ┌───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───┬───────┐ ┌───┬───┬───┐ ┌───┬───┬───┬───┐
            │~ `│! 1│@ 2│# 3│$ 4│% 5│^ 6│& 7│* 8│( 9│) 0│_ -│+ =│ BacSp │ │Ins│Hom│PUp│ │N L│ / │ * │ - │
            ├───┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─────┤ ├───┼───┼───┤ ├───┼───┼───┼───┤
            │ Tab │ Q │ W │ E │ R │ T │ Y │ U │ I │ O │ P │{ [│} ]│ | \ │ │Del│End│PDn│ │ 7 │ 8 │ 9 │   │
            ├─────┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴┬──┴─────┤ └───┴───┴───┘ ├───┼───┼───┤ + │
            │ Caps │ A │ S │ D │ F │ G │ H │ J │ K │ L │: ;│" '│ Enter  │               │ 4 │ 5 │ 6 │   │
            ├──────┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴─┬─┴────────┤     ┌───┐     ├───┼───┼───┼───┤
            │ Shift  │ Z │ X │ C │ V │ B │ N │ M │< ,│> .│? /│  Shift   │     │ ↑ │     │ 1 │ 2 │ 3 │   │
            ├─────┬──┴─┬─┴──┬┴───┴───┴───┴───┴───┴──┬┴───┼───┴┬────┬────┤ ┌───┼───┼───┐ ├───┴───┼───┤ E││
            │ Ctrl│    │Alt │         Space         │ Alt│    │    │Ctrl│ │ ← │ ↓ │ → │ │   0   │ . │←─┘│
            └─────┴────┴────┴───────────────────────┴────┴────┴────┴────┘ └───┴───┴───┘ └───────┴───┴───┘
```

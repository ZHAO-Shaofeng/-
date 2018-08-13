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
  9. [让背景图随DIV变化，且不变形居中](#9让背景图随div变化且不变形居中)
  10. [重置样式](#10重置样式)
  11. [div内容垂直布局](#11div垂直布局)
  12. [input框在ios中的内阴影问题](#12input框在ios中的内阴影问题)
* #### [JS相关](#js相关-1)
  1. [获取URL参数值](#1获取url参数值)
  2. [头部提取之后，导航跳转添加对应的active ](#2头部提取之后导航跳转添加对应的active)
  3. [swiper常用参数](#3swiper常用参数)
  4. [锚链接平滑移动](#4锚链接平滑移动)
  5. [数字递增](#5数字递增)
  6. [侧边栏吸边](#6侧边栏吸边)
  7. [AJAX请求](#7ajax请求)
* #### [Vue相关](#vue相关-1)
  1. [使用sass](#1使用sass)
  2. [vue数据便利后进行初始化](#2vue数据便利后进行初始化)
  3. [vue中常用图片上传](#3vue中常用图片上传)
  4. [vue中进行跨域代理及发布注意事项。](#4vue中进行跨域代理及发布注意事项)

## 开发规范
> 不管有多少人共同参与同一项目，一定要确保每一行代码都像是同一个人编写的。    
[编码规范传送门](http://codeguide.bootcss.com/)

## 开发注意事项

1、插件的版本是否统一；

2、全局样式用谁的；

3、样式表的结构是不是继承的写法，会不会互相干扰；

4、样式优先级如下：    
` 通用选择器 * < 元素(类型)选择器 < 类选择器 < 属性选择器 < 伪类 < ID 选择器 < 内联样式 `

5、团队协作下使用git了吗；

6、不同团队开发，在关于复用的组件以及全局的变量是否有进行沟通；

7、如非特殊情况，慎用!important，因为使用!important会扰乱原本层叠和权重产生正常的作用顺序，使后期维护带来麻烦；

8、链接加title，图标加alt，logo要用h1包裹！

9、一排的展示布局优先使用swiper，否则后面说要加滑动功能就麻烦一些，不如直接用swiper然后不初始化就行了！


## HTML head
```
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
一个项目不可能从头到尾都是你一个人在开发，哪怕是一个很小的项目，如果每个人都把规范做到极致，所有事情都会变得更简单。在我遇到的大部分开发中，用Git合并项目时，遇到最多的冲突就是样式表用来用去不知道在用谁的，改来改去还不好改；如果我们把样式拆分成模块会方便很多，这样出了问题一看就知道是谁的锅了，譬如在用Less的时候：

![Less目录](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/mulu.png)

这样的目录一目了然哪个文件是哪个部分的

将经常用到的样式单独定义写到_variable.less里

![全局变量](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/variable.png)

然后再把所有的文件引入到style.less

![整合less](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/style.png)

哪怕你是用的原生css来写，如果在class上写明哪个文件并添加注释之后，不觉得这样看起来更清晰吗

![原生css](https://raw.githubusercontent.com/ZHAO-Shaofeng/Related-considerations-for-HTML-CSS-JS/master/github-img/css.png)

只是用Less举个例子想把规范说清楚，至于用原生css还是用css的预编译处理语言这里不作讨论

但是显然用预编译处理语言在开发和贴近规范上会更方便一些，这是推荐使用的。    
如果我们的样式表都是通过嵌套规则来一个个继承的，不管你用哪个都不会有任何冲突，因为彼此之间的关系是很清晰的。

### 2、单行溢出省略号
```
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

### 3、多行溢出省略号
```
overflow : hidden;
text-overflow: ellipsis;
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
```

### 4、placeholder样式
```
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
*  从上到下
```
background: -webkit-linear-gradient(red, blue);
background: -o-linear-gradient(red, blue);
background: -moz-linear-gradient(red, blue);
background: linear-gradient(red, blue);
```
 
*  从左到右
```
background: linear-gradient(to right, red , blue);
```
 
*  角度
```
background: linear-gradient(to bottom right, red , blue);  /*左上角至右下角*/
background: linear-gradient(180deg, red, blue);  /*指定角度*/
```
 
*  多个颜色
```
background: linear-gradient(red, green, blue);
```
 
### 6、flex页脚置底(兼容至ie10)
```
<body>
    <header></header>
    <main></main>
    <footer></footer>
</body>

html{height: 100%;}
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
[传送门](http://www.jb51.net/article/42513.htm)

### 8、tab常用响应式不转行，可左右拉动
放在容器里的样式
```
white-space: nowrap;
overflow-x: auto;
display: flex;
overflow-y: hidden;
```

### 9、让背景图随DIV变化，且不变形居中
让背景图随DIV变化，且不变形居中。
```
background-image: url("../images/index/banner.png");
background-repeat: no-repeat;
background-size: cover;
background-attachment: fixed;
background-position: center center;
```

### 10、重置样式
参考网站：https://meyerweb.com/eric/tools/css/reset/index.html
```
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
```
display: table-cell;
vertical-align: middle;
```

### 12、input框在ios中的内阴影问题
```
-webkit-appearance: none;
```

## JS相关
### 1、获取URL参数值
获取URL的参数的值。
```
function getQueryString(name) {
    var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)", "i");
    var r = window.location.search.substr(1).match(reg);
    if (r != null) return unescape(r[2]); return null;
}
```

### 2、头部提取之后，导航跳转添加对应的active
添加到提取的header.html中
```
$(".navbar-nav a").each(function(){
  $this = $(this);
  if($this[0].href==String(window.location)){
    $(".navbar-nav li").removeClass("active");
    $this.parent("li").addClass("active");
  }
});
```

### 3、swiper常用参数
```
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

var Swiper1 = new Swiper('.swiper-container', {
    autoplay: {		                //自动播放
        delay: 1000,	            //间隔时间
        disableOnInteraction: false,	//用户操作swiper之后，是否禁止autoplay。
    },
    slidesPerView: 4,	            //一屏显示多少个
    slidesPerColumn: 2,	          //显示2行
    spaceBetween: 30,	            //每个之间的间距
    noSwiping : true,	            //使该slide无法拖动，希望文字被选中时可以考虑使用
    noSwipingClass : 'no-swiper',
    centeredSlides : true,	      //居中显示
    loop: true,		                //头尾循环
    observer: true,		            //修改swiper自己或子元素时，自动初始化swiper 
    observeParents: true,	        //修改swiper的父元素时，自动初始化swiper 
    pagination: {		              //分页器
        el: '.swiper-pagination',
        clickable :true         	//允许点击分页器切换
    },
    navigation: {		              //前进后退按钮
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
    },
    breakpoints: {		            //响应式设置
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
```
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
```
<div id="id">
    <p class="incrementing" data-to="20" data-speed="1500">10</p>
</div>

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

```
<style>
#backtop{
  position: fixed;
  width: 110px;
  bottom: 0;
  opacity: 0;
  z-index: 100;
  transition: 0.3s;
}
#backtop.show{opacity: 1;}
</style>

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
```
var json ={
  mid: '123',
  version_timestamp: '456'
}
$.ajax(function(){
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
```
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
#### 对象类型转为包含JSON文本的字符串类型
```
SignPointList_Data = JSON.stringify(res.Data);
```
#### 转为JSON
```
SignPointList_Data = JSON.parse(SignPointList_Data);
```

## Vue相关
### 1、使用sass
https://www.cnblogs.com/crazycode2/p/6535105.html

### 2、vue数据便利后进行初始化
```
that.$axios.get(url).then(function (res) {
  that.rollingNew = res.data.content;
  //重点。在$nextTick方法内进行初始化
  that.$nextTick(() => {  // 下一个UI帧再初始化swiper
    that.initSwiper();
  });
  console.log(that.rollingNew)
})
```

### 3、vue中常用图片上传。
```
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
```
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
```
new OptimizeCSSPlugin({
  cssProcessorOptions: config.build.productionSourceMap
  ? { safe: true, map: { inline: false } }
  : { safe: true }
}),
```
#### 此段代码需要注释掉，目前发现其对于-webkit-box-orient: vertical;会进行消除，
#### 注意：注释掉此代码后，webpack不会对css进行压缩，所以要在utils.js文件里下面代码中加入minimize: true，如下：
```
const cssLoader = {
  loader: 'css-loader',
  options: {
      sourceMap: options.sourceMap,
      minimize: true
  }
}
```

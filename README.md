## 开发注意事项

1、插件的版本是否统一；

2、全局样式用谁的；

3、样式表的结构是不是继承的写法，会不会互相干扰；

4、样式优先级如下：    
` 通用选择器 * < 元素(类型)选择器 < 类选择器 < 属性选择器 < 伪类 < ID 选择器 < 内联样式 `

5、团队协作下使用git了吗；

6、不同团队开发，在关于复用的组件以及全局的变量是否有进行沟通；

7、如非特殊情况，慎用!important，因为使用!important会扰乱原本层叠和权重产生正常的作用顺序，使后期维护带来麻烦；

## CSS常用
### 1、单行溢出省略号
```
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

### 2、多行溢出省略号 
```
overflow : hidden;
text-overflow: ellipsis;
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
```

### 3、placeholder样式
```
input::-webkit-input-placeholder{
  color:red;
}
input::-moz-placeholder{   /* Mozilla Firefox 19+ */
  color:red;
}
input:-moz-placeholder{    /* Mozilla Firefox 4 to 18 */
  color:red;
}
input:-ms-input-placeholder{  /* Internet Explorer 10-11 */ 
  color:red;
}
 ```

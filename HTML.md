## 1.HTML XHTML XML的区别

- HTML: 超文本标记语言
- XHTML：可扩展的超文本标记语言，基于XML，作用与HTML类似，但语法更加严格
- XML：可扩展标记语言，主要用于存储数据和结构

XHTML标签名必须手写，元素必须以双标签形式存在，元素必须被正确嵌套，元素必须有根元素

## 2.HTML5和HTML的区别

HTML5是HTML的新标准，其主要目标是无需任何额外的插件就可以传输所有内容，它包括了动画，视频等丰富的图形界面

**从文档声明**

`HTML`的文档声明是很长的一段代码，而`HTML5` 只需要在文档头部使用`<!DOCTYPE html>`标签即可声明

**从语义结构**

`HTML4.0`没有体现语义化的标签，而`HTML5`加入了很多语义化标签，如`header main footer acticle`等

## 3.DOCTYPE标签

`<!DOCTYPE html>`的作用就是让浏览器进入标准模式，使用最新的`W3C`标准来解析渲染页面，若文档头部不写则浏览器会使用兼容模式来解析和渲染页面

- 标准模式：指浏览器按照`W3C`标准解析文档
- 兼容模式：浏览器通常会为了兼容老旧站点而不使用最新的`W3C`标准来解析文档

## 4.块元素 行内元素 行内块元素

- 块元素
  - 独占一行
  - 可以设置宽高，不设置宽度情况下默认继承父元素的宽度
  - 常见的块元素：`div p h1~h6 ul ol table form`
- 行内元素
  - 相邻的元素会排列在同一行
  - 无法设置宽高，其大小由内容决定
  - 可以设置水平方向的`margin padding`的值，但无法使用`auto`属性居中
  - 常见的行内元素：`span a strong b em i label`等
- 行内块元素
  - 不独占一行
  - 可以设置宽高，默认大小由内容决定
  - 可以设置`margin padding`等属性，但无法使用`auto`属性居中
  - 常见的行内块元素：`button input img iframe`等

## 5.Link和@import导入样式的区别

- link是HTML标签，@import用于CSS文件中导入另一个CSS文件
- link标签在页面加载时就会被加载，@import引用会等到页面加载完在加载
- link标签权重高于@import引用
- @import引用有兼容性问题，而link标签无兼容问题

## 6.label标签

`label`标签用来定义表单控制间的关系，当用户与该标签发生交互的时候，浏览器会自动对焦到绑定的表单标签上

```html
<label for="Name">Number:</label>
<input type=“text“ name="Name" id="Name"/>
```

## 7.标签上的title和alt属性的区别

title属性用于为该元素设置建议性信息，在鼠标移到该元素上面时会显示

alt属性用于在图片未能正常显示时给予文字说明

## 8.语义化的好处

- 便于开发者阅读和写出更加优雅的代码
- 有利于`SEO`：让浏览器爬虫更好地解析，爬虫依赖于标签来确定上下文和各个关键字的权重
- 方便其它设备(如移动设备)解析文档

## 9.iframe的优缺点

- 优点
  - 跨域通信
  - 无刷新文件上传
  - 可以用于加载一些第三方图标或广告等
- 缺点
  - 会阻塞主页面`onload`事件
  - 无法被一些搜索引擎识别
  - 会产生很多页面，不利于管理

## 10.src与href的区别

- href: 指向网络资源所在的位置，并建立该资源和当前元素(锚点)或当前文档(链接)之间的链路，用于超链接
- src：指向外部资源的位置，指向的内容将会嵌入到文档中当前标签所在的位置；在请求src资源时会将其指向的资源下载并应用到文档内，例如js脚本，img图片，iframe等。

## 11.HTML5新特性

- Canvas SVG：用于绘图的元素
- video audio:用于播放视频和音频的媒体
- Drag，Drop：用于拖拽的元素
- Geolocation：用于获取地理位置
- LocalStorage SessionStorage：用于本地离线存储
- web Worker：运行在后台的JavaScript脚本
- webSocket：基于TCP的全双工通信协议
- 语义化标签：header main footer nav section等
- 新的表单控件：date time url email search等

## 12.标准模式和怪异模式的区别

- 盒模型：标准模式中一个元素的宽高是它内容的宽高，怪异模式下元素的宽高还包含了`padding`和`border`
- 行内元素宽高：标准模式下行内元素无法设置宽高，怪异模式下则可以

- 水平居中：标准模式下`margin: 0 auto`可以使元素水平居中，怪异模式下则不行

## 13.标准盒模型和怪异盒模型

HTML中每一个元素都可以看作一个盒模型，一个盒模型由`content + padding + border + margin`组成

- 标准盒模型：设置盒模型的width和height属性其实是设置内容的宽高，盒模型的宽度等于width + padding + border + margin
- 怪异盒模型：设置盒模型的的width和height属性其实是设置了`content + padding + border`的值。例如设置width为100px，padding为10px，那么此时内容区域的宽度只有80px(100 - 20 * 2)

- box-sizing：content-box|border-box|inherit

## 14.前端结构样式和行为分离

结构(HTML)相当于人的骨架，样式(CSS)相当于人的装饰，行为(JavaScript)相当于人的动作，前端将这三者分离开，各自负责各自的内容，各部分可以通过引用进行使用

在分离的基础上，我们需要做到代码的精简，重用，有序

**分离的好处**

- 代码分离，利于团队的开发和后期的维护；
- 减少维护成本，提高可读性和更好的兼容性；

## 15.如何对网站的文件和资源进行优化

- 文件合并，减少http请求
- 文件压缩（`gzip`压缩需要的css和js文件）
- 使用缓存
- 使用`cdn`托管资源
- 网站外链接优化
- meta标签优化,设置title keywords description优化等

## 16.渐进增强和优雅降级的区别

- 渐进增强：优先考虑低版本浏览器的兼容，在保证基本功能可以使用的情况下，再考虑对高级浏览器进行效果，交互等方面的优化
- 优雅降级：一开始就构建完整的功能，然后再针对低版本浏览器进行兼容

## 17.为什么HTML5不需要DTD

HTML5中没有使用SGML或XHTML，不需要参考DTD

## 18.form表单关闭自动完成(自动联想)功能

设置`autocomplete=off`

## 19.几种图片格式的区别

- png：图片背景透明，可以支持很多颜色
- jpg：图片背景不透明，静态图，可压缩
- gif：动态图，支持颜色较少

## 20.meta标签

`meta`标签常用于定义页面的说明，关键字等元数据，这些数据一般服务于浏览器，搜索引擎，并不会直接向用户展示

- charset：规定HTML文档的字符编码
- http-equiv：一般用于设置一些与http请求头相关的信息，例如`content-Type refresh`等
  - X-UA-Compatible：一般用于设置浏览器兼容
- keywords：设置网页关键字
- description：设置网页的描述内容
- viewport：用于移动端的显示优化


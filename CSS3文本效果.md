# CSS3文本效果 #
本章主要探讨 HTML5中 CSS3 中文本效果，其中也包含一些之前讲过的CSS3文本属性。
## 一、文本阴影 ##
CSS3提供了 text-shadow 文本阴影效果，这个属性在之前讲过，只是没有涉及浏览器支持情况
<html>
    <table>
    <tr><td rowspan="2">text-shadow</td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>IE</td><td>Safari</td></tr>
    <tr><td>9.5+</td><td>3.5+</td><td>4+</td><td>10+</td><td>3.1+</td></tr>
    </table>
</html>

这里有几点注意:1.text-shadow在CSS2的时候出现过，但各大浏览器碍于消耗大量资源，迟迟未支持，然后在 CSS2.1 中剔除了。现在，CSS3已经全面支持了：2.最低支持版本上，不同手册和教材都不太同，但版本年代久远，无伤大雅，最准确的可以查询这个网站：http://caniuse.com。最需要注意的只有 IE10才支持，IE9不支持的：3.目前的浏览器不需要给这个属性加上任何前缀，具体查询前缀版本可以访问刚才提供的地址。


<text>
//正值阴影<br>
text-shadow: 1px 1px 1px red;<br>
//负值阴影<br>
text-shadow:-1px -1px 1px red;<br>
//多重阴影叠加<br>
text-shadow:0px 0px 0 rgb(188,178,188),<br>
            1px 0px 0 rgb(173,163,173),<br>
            2px 0px 0 rgb(157,147,157),<br>
            3px 0px 0 rgb(142,132,142),<br>
            4px 0px 0 rgb(126,116,126),<<br>
            5px 0px 0 rgb(111,101,111),<br>
            6px 0px 0 rgb(95,85,95),<br>
            7px 0px 0 rgb(79,69,79)
</text>

## 二、文本裁剪 ##
CSS3提供了 text-overflow 属性来控制文本的溢出部分，它的作用是对溢出的部分裁剪掉，然后判定是否添加省略号。首先我们先看下样式表的属性，如下：
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>clip</td><td>默认值，裁剪文本时不添加 "..."省略号</td></tr>
<tr><td>ellipsis</td><td>裁剪文本时添加"..."省略号</td></tr>
</table>
</html>
<div></div>
<html>
//必须不换行和使用 overflow 控制溢出<br>
P {<br>
    width:160px;<br>
    white-space:nowrap;<br>
    background:silver;<br>
    /*text-overflow:clip;*/<br>
    overflow:hidden;<br>
}
</html>
<br>对于 text-overflow 的支持度，是根据它的属性值来判定的，不同的属性值浏览器支持度不同。<br>
<html>
<table>

## ##
<tr><td>属性值</td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>IE</td><td>Safari</td></tr>
<tr><td>clip</td><td>9.63+</td><td>2.0+</td><td>1.0+</td><td>6.0+</td><td>3.1+</td></tr>
<tr><td>ellipsis</td><td>10.5+</td><td>6.0+</td><td>1.0+</td><td>6.0+</td><td>3.1+</td></tr>
</table>
</html>
<br>
<html>
//在 Opera 早期版本 10.0 ~ 10.1 中，需要使用带前缀 -o- 。<br>
P{
    -o-text-overflow:ellipsis;
    text-overflow:ellipsis;
}<br>
而在 Opera 主流版本中，引擎已经靠拢 webkit,则不需要 -o- 了，目前来说，也不需要兼容 -o- 了。
</html>

## 三、文本描边 ##
CSS3提供了描边属性，即 text-stroke、text-stroke-width、text-stroke-color，目前只有 webkit 引擎的浏览器支持，并且必须加上 -webkit- 前缀才有效。

## 四、文本填充 ##
CSS3提供了一个文本颜色填充功能：text-fill-color,感觉和 color 属性很像。其实在配合其他属性才能达到不一样的效果。
<html>
<table>
<tr><td>属性</td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>IE</td><td>Safari</td></tr>
<tr><td>text-fill-color</td><td>15.0+</td><td>不支持</td><td>4.0</td><td>不支持</td><td>3.1+</td></tr>
</table>
</html>
<html>
<br>//不配合背景样式时，和 color 属性没有区别<br>
p{
    font-size:150px;<br>
    -webkit-text-fill-color:red;<br>
}<br>
  <br>//和CSS3背景的新特性搭配产生渐变文字<br>
  p{
      <br>font-size:150px;<br>
      font-family:黑体;<br>
      background:<br>
            -webkit-linear-gradient(top,#eee,<br>#aaa 50%,#333 51%,#000);
            -webkit-background-clip:text;<br>
            -webkit-text-fill-color:transparent;<br>
  }
</html>
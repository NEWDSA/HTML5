# 一、过渡简介 #
过渡效果一般是通过一些简单的CSS动作触发平滑过渡功能，比如: :hover、:focus、:active、:checked等。CSS3提供了 transition 属性来实现这个功能的过渡功能，主要属性如下表
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>transition-property</td><td>指定过渡或动态模拟的CSS属性</td></tr>
<tr><td>transition-duration</td><td>指定过渡完成所需的时间</td></tr>
<tr><td>transition-timing-function</td><td>指定过渡的函数</td></tr>
<tr><td>transition-delay</td><td>指定过渡或动态模拟的CSS属性</td></tr>
<tr><td>transition</td><td>指定过渡开始出现的延迟时间</td></tr>
</table>
</html>

我们先创建一个没有过渡效果的元素，然后通过:hover 来触发它。在没有任何过渡效果的触发，会立即生硬的执行触发。<br>
<code>
 //设置元素颜色
 div{
     width:200px;
     height:200px;
     background-color:white;
     border:1px solid green;
 }
</code>
## 二、transition-proerty ##
首先设置过渡的第一个属性就是指定过渡的属性。同样，你需要指定你要过渡某个元素的两套样式用于用户和页面交互。那么就使用 transition-property 属性，详细属性值如下表：
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>none</td><td>没有指定任何样式</td></tr>
<tr><td>all</td><td>默认值，指定元素所支持 transition-property属性的样式</td></tr>
<tr><td>指定样式</td><td>指定支持 transition-property的样式</td></tr>
</table>
</html>

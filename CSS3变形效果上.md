# CSS3变形效果[上] #
本章主要讨论 HTML5 中 CSS3 的变形效果，通过变形效果，可以平移、缩放和旋转元素的功能。
## 一、transform ##
CSS3 提供了元素变形效果,也叫做变换。它可以将元素实现旋转、缩放和平移的功能。属性有两个：transform 和 transform-origin。
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>transform</td><td>指定应用的变换功能</td></tr>
<tr><td>transform-origin</td><td>指定变换的起点</td></tr>
</table>
</html>
对于 transform的属性值，具体如下表：
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>none</td><td>无变换</td></tr>
<tr><td>translate(长度或百分数值)<br>translateX(长度或百分数值)translateY(长度或百分数值)</td><td>在水平方向、垂直方向或两个方向上平移元素。</tr>
<tr><td>scale(数值)<br>scaleX(数值)<br>scaleY(数值)</td><td>在水平方向、或垂直方向或两个方向上缩放元素</td></tr>
<tr><td>rotate(角度)</td><td>旋转元素</td></tr>
<tr><td>skew(角度)<br>skewX(角度)<br>skewY(角度)</td><td>在水平方向、垂直方向或两个方向上使元素倾斜一定的角度</td></tr>
<tr><td>matrix(4~6数值，逗号隔开)</td><td>指定自定义变换</td></tr>
</table>
</html>

//向水平和垂直各移动 200像素，也可以使用百分比
transform: translate(200px,200px);

## 二、transform-origin ##
transform-origin 属性可以设置变换的起点。默认情况下，使用元素的中心作为起点。具体设置方案参考如下表：
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>百分数值</td><td>指定元素x轴或y轴的起点</td></tr>
<tr><td>长度值</td><td>指定距离</td></tr>
<tr><td>left<br>center<br>right<br></td><td>指定x轴的距离</td></tr>
<tr><td>top<br>center<br>bottom</td><td>指定y轴的位置</td></tr>
</table>
</html>
这个属性是用来改变变形的基准点的，默认是在元素的中心位置，如果你改变了基准点。它就会按照这个基准点进行变形。<br>

//默认值，以中心点变形<br>
transform-origin:center center;
transform-origin:50% 50%;

//以左上角为基准点变形<br>
transform-origin: left top;<br>
transform-origin: 0px 0px;

## 三、浏览器版本 ##
CSS3 中的变形效果最低版本和需要前缀的版本如下：
<html>
<table>
<tr><td></td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>Safari</td><td>IE</td></tr>
<tr><td>支持需带前缀</td><td>11.5~22</td><td>3.5~15</td><td>4~35</td><td>3.1~8</td><td>9.0+</td></tr>
<tr><td>支持不需带前缀</td><td>23+</td><td>16+</td><td>无</td><td>10.0+</td></tr>
</table>
</html>

//兼容完整版<br>
-webkit-transform:rotate(45deg);<br>
-moz-transform:rotate(45deg);<br>
-0-transform:rotate(45deg);<br>
-ms-transform:rotate(45deg);<br>
transform:rotate(45deg);<br>

-webkit-transform-origin:left top;<br>
-moz-transform-origin:left top;<br>
-o-transform-origin:left top;<br>
-ms-transform-origin:left top;<br>
transform-origin:left top;

# CSS3 变形效果[下] #
本章主要探讨 HTML5 中 CSS3 的变形效果，主要接着上节课的 2D 平面变形转换到 3D 立体变形。
## 3D 变形简介 ##
之前我们学习了元素的平移、旋转、缩放和倾斜等功能。这些效果只是单纯在二维平面的基础上的，我们称之为 2D。那么其实 CSS3也提供了三维立体的一些功能效果，并且目前较新的主流浏览器都比较支持，只不过比 2D 晚一些，对浏览器的版本要求也要高一些。
由于 3D 是立体三维，在 x,y 轴的基础上一般会多出一个 z 轴，深入跃出轴。以下是 3D 变形的属性值表，如下：
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>translate3d(x,y,z)</td><td>3D 方式平移元素，设置x,y和z轴</td></tr>
<tr><td>translateZ(Z)</td><td>设置 3D 方式平移元素的 z 轴</td></tr>
<tr><td>scale3d(x,y,z)</td><td>3D 方式缩放一个元素</td></tr>
<tr><td>scaleZ(z)</td><td>设置 3D 方式缩放元素的 z 轴</td></tr>
<tr><td>rotate3d(x,y,z,a)</td><td>3d 方式旋转元素</td></tr>
<tr><td>rotateX(a)<br>rotateY(a)<br>rotateZ(a)</td><td>分别设置 3D 方式的旋转元素的 x,y和 z 轴</td></tr>
<tr><td>perspective(长度值)</td><td>设置一个透视投影矩阵</td></tr>
<tr><td>matrix3d(多个值)</td><td>定义一个矩阵</td></tr>
</html>

<html>
<table>
<caption>3D 变形比 2D 变形出来的要晚一些，所以如果需要兼容旧的浏览器。可以对照这个表，具体如下：</caption>
<tr><td></td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>Safari</td><td>IE</td></tr>
<tr><td>支持带前缀</td><td>15~22</td><td>10~15</td><td>12~35</td><td>4~8</td><td>无</td></tr>
<tr><td>不支持带前缀</td><td>23+</td><td>16+</td><td>26+</td><td>无</td><td>10.0+</td></tr>
</table>
</html>





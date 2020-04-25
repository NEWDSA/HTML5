# CSS3渐变效果 #
本章主要探讨 HTML5 中 CSS3 背景渐变功能，主要有两种渐变方式：线性渐变和径向（放射性）渐变。
## 一、线性渐变 ##
CSS3提供了 linear-gradient 属性实现背景颜色都渐变功能。在以前，这种效果必须采用图片才能实现的。首先，我们先看一下它的样式表，如下：
<html>
<table>
<tr><td>linear-gradient(方位,起始色,末尾色)<td></tr>
<tr><td>方位</td><td>可选参数，渐变的方位。可以使用的值有:to top、to top right、to right、 to bottom、to bottom left、to left、to top left</td></tr>
<tr><td>起始色</td><td>必选参数,颜色值</td></tr>
<tr><td>末尾色</td><td>必选参数,颜色值</td></tr>
</table>
</html>
<html>
   <br> //两个必须参数<br>
    background-image:linear-gradient(orange,green);<br>
    //增加一个方位量<br>
    background-image:linear-gradient(to top,orange,green)<br><br>
    通过 top、left、right、bottom这四组实现的渐变方向有时比较单一，我们可以使用以角度单位的数值来设置方位。比如 0度 (0deg) 相当于 to top: 角度会沿逆时针方向随着你的角度的增加而增加。

    //通过角度设置方位, 0 ~ 360度之间，可以是负值
    background-image: linear-gradient(45deg,orange,green);

    //多色线性渐变
    background-image:linear-gradient(-45deg,orange,blue,red);

    //通过百分比设置多色线性位置
    background-image:linear-gradient(-45deg,orange 0% green 20%,blue 40%, red 100%);

    默认情况下：起始颜色的百分比位置是0%,末尾颜色的百分比位置是100%,其他位置按照平均值分配。也可以使用px像素来设置，但计算麻烦点。

    //结合背景，并使用透明渐变实现强大的层次感
    background-color: red;
    background-image: linear-gradient(to top right,rgba(0,0,0,0.6),
    rgba(0,0,0,0));

    //重复渐变属性值
    background-image:repeating-linear-gradient(to top,orange 10px,green 30px);

    目前最新的主流浏览器都支持 CSS3 的渐变属性，那么对于之前的浏览器支持程度如何呢？可以参考如下的表:
    
</html>

<html>
<table>
<tr><td></td><td>Opera</td><td>Firefox</td><td>Chrome</td><td>Safari</td><td>IE</td></tr>
<tr><td>部分支持需带前缀</td><td>无</td><td>4~9</td><td>4~9</td><td>4~5</td><td>无</td></tr>
<tr><td>支持须带前缀</td><td>无</td><td>3.6~15</td><td>10~25</td><td>5.1~6</td><td>无</td></tr>
<tr><td>支持不带前缀</td><td>12.1+</td><td>16+</td><td>26+</td><td>6.1+</td><td>10.0+</td><tr>
</table>
</html>

这里提到了部分支持，说明当时可能渐变还尚未完善，但可以通过添加前缀来使用它了。具体哪些没有完善，已经无法考证了，版本太过久远。那么支持带前缀和不支持带前缀的完整格式如下：

//加上兼容前缀<br>
background-image: -webkit-linear-gradient(to top,orange,green);<br>
background-image: -moz-linear-gradient(to top,orange,green);<br>
background-image: -o-linear-gradient(to top,orange,green);<br>
background-image: linear-gradient(to top,orange,green);

## 二、径向渐变 ##
CSS3 提供了径向渐变，也叫放射性渐变：radial-gradient 属性值。它是从一个点向四周发散的方式扩展，属性值样式如下：
<html>
<table border="1">
<tr><td colspan="2">radial-gradient(方位,起始色,末尾色)<td></tr>
<tr><td>方位</td><td>可选参数,径向的方位。可以使用的值有：像素、百分比、固定值,或复合搭配使用</td></tr>
<tr><td>起始色</td><td>必选参数,颜色值</td></tr>
<tr><td>末尾色</td><td>必选参数,颜色值</td></tr>
</table>
//两个必选参数
background-image:radial-gradient(orange,green);

//如果想设置第一个可选参数，有一种做法是设置为: circle(圆形)或 ellipse(椭圆形)。默认是椭圆形。
background-image:radial-gradient(circle,orange,green);
<table>
<tr><td>形状</td><td>说明</td></tr>
<tr><td>circle</td><td>圆形</td></tr>
<tr><td>ellipse</td><td>椭圆形,默认值</td></tr>
</table>
//不单单可以设置形状，还可以设置形状的发散方向<br>
background-image:radial-gradient(circle at top,orange,green);
<table>
<tr><td>方向</td><td>说明</td></tr>
<tr><td>top</td><td>从顶部发散</td></tr>
<tr><td>left</td><td>从右侧发散</td></tr>
<tr><td>right</td><td>从右侧发散</td></tr>
<tr><td>bottom</td><td>从底部发散</td></tr>
<tr><td>center</td><td>从中间散发</td></tr>
<br>//也可以复合方向，比如右下方<br>
background-image:radial-gradient(circle at right bottom,orange,green);<br>
//可以设置发散的距离，即圆的半径长度<br>
background-image:radial-gradient(circle closest-side,orange,green);
</table>
<table>
<tr><td>半径关键字</td><td>说明</td></tr>
<tr><td>closest-side</td><td>指定径向渐变的半径长度为从圆心到离圆心最近的边</td></tr>
<tr><td>closest-corner</td><td>指定径向渐变的半径长度为从圆心到离圆心最近的角</td></tr>
<tr><td>farthest-side</td><td>指定径向渐变的半径长度为从圆心到离圆心最远的边</td></tr>
<tr><td>farthest-corner</td><td>指定径向渐变的半径长度为从圆心到离圆心最远的角</td></tr>
</table>
//关键字有点拗口，可以用像素表示半径，但不接收百分比<br>
background-image:radial-gradient(circle 50px orange,green);<br>
//同样，也有重复背景方式<br>
background-image:repeating-radial-gradient(circle 50px,orange,green);<br>
//两个重复背景只要加上前缀就是兼容模式了<br>
background-image:-webkit-repeating-radial-gradient;<br>
background-image:-moz-repeating-radial-gradient;<br>
background-image:-o-repeating-radial-gradient;<br>
background-image:repating-radial-gradient;<br>
</html>

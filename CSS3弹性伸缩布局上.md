# CSS3 弹性伸缩布局上 #
## 一、布局简介 ##
CSS3 提供了一种新的布局方式:Flexbox 布局，即弹性伸缩布局模型(Flexible Box)。用来提供一个更加有效的方式实现响应式布局。但是用于这个布局方式还处于 W3C 的草案阶段。并且它还分为旧版本、新版本以及混合过渡版本三种不同的编码方式。在发展中，可能还有各种改动。浏览器的兼容性还存在问题。所以，本节课为初步了解即可。
## 二、旧版本 ##
如果属性和属性值为: display:box,那么就是 2009 年7月份设定的工作草案，属于旧版本。它面向的是一些早期浏览器的弹性布局方案。
首先，我们要将几个需要布局模块的父元素设置一下容器属性 display。
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>box</td><td>将容器盒模型作为块级弹性伸缩盒显示(旧版本)</td></tr>
<tr><td>inline-box</td><td>将容器盒模型作为内联级弹性伸缩盒显示(旧版本)</td></tr>
</table>
</html>

## 1.box-orient 属性 ##
box-orient 主要实现盒子内部元素的流动方向。
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>horizontal</td><td>伸缩项目从左到右水平排列</td></tr>
<tr><td>vertical</td><td>伸缩项目从上到下垂直排列</td></tr>
<tr><td>inline-axis</td><td>伸缩项目沿着内联轴排列显示</td></tr>
<tr><td>block-axis</td><td>伸缩项目沿着块轴排列显示</td></tr>
</table>
</html>

## 2.box-direction ##
box-direction 属性主要是设置伸缩布局中的流动顺序。
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>normal</td><td>默认值，正常顺序</td></tr>
<tr><td>reverse</td><td>逆序</td></tr>
</table>
</html>

## 3.box-pack ##
box-pack 属性用于伸缩项目的分布方式。
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>start</td><td>伸缩项目以起始点靠齐</td></tr>
<tr><td>end</td><td>伸缩项目以结束点靠齐</td></tr>
<tr><td>center</td><td>伸缩项目以中心点靠齐</td></tr>
<tr><td>justify</td><td>伸缩项目平局分布，-webkit- 支持，-moz- 不支持</td></tr>
</table>
</html>

## 4.box-algin ##
box-algin 属性用来处理伸缩容器的额外空间。
<html>
<table>
<tr><td>属性值</td><td>说明</td></tr>
<tr><td>start</td><td>伸缩项目以顶部为基准,清理下部额外空间</td></tr>
<tr><td>end</td><td>伸缩项目以底部为基准,清理上部额外空间</td></tr>
<tr><td>center</td><td>伸缩项目以中部为基准,平均清理上下部额外空间</td></tr>
<tr><td>baseline</td><td>伸缩项目以基线为基准,清理额外的空间</td></tr>
<tr><td>stretch</td><td>伸缩项目填充整个容器,默认</td></tr>
</table>
</html>

## 5.box-flex ##
box-flex 属性可以使用浮点数分配伸缩项目的比例

## 6.box-ordinal-group ##
box-ordinal-group 属性可以设置伸缩项目的显示位置。<br>
//将第一个位置的元素，跳转到第三个位置<br>
p:nth-child(1){
    -moz-box-ordinal-group:3;
}



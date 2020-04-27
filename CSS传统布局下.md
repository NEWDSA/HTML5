# CSS传统布局下 #
## 一、定位布局 ##
在使用定位布局前，我们先了解一下定位属性的用法。CSS2提供了position 属性来实现元素的绝对定位和相对定位。
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>static</td><td>默认值,无定位</td></tr>
<tr><td>absolute</td><td>绝对定位，使用 top、right、bottom、left进行位移</td></tr>
<tr><td>relative</td><td>相对定位，使用 top、right、bottom、left进行定位</td></tr>
<tr><td>fixed</td><td>以窗口参考定位，使用 top、right、bottom、left进行定位</td></tr>
</table>
</html>
<br>
//绝对定位，脱离文档流，以窗口文档左上角 0,0 为起点.<br>
所谓脱离文档流的意思，就是本身这个元素在文档流中是占位的，如果脱离了，就不占有文档的位置，好像浮在了空中一般，有了层次感。<br>
由于绝对定位脱离了文档流，出现层次概念。那么每个元素到底在那一层，会不会冲突覆盖。这时通过 z-index 属性来判定它们的层次关系。
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>auto</td><td>默认层次</td></tr>
<tr><td>数字</td><td>设置层次，数字越大，层次越高</td></tr>
</table>
</html>
<br>
//以窗口参考定位，脱离文档流,会随着滚动条滚动而滚动

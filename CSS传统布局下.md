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
//以窗口参考定位，脱离文档流,会随着滚动条滚动而滚动<br>
position:fixed;<br>
//相对定位，不脱离文档流，占位偏移<br>
position:relative;

## box-sizing ##
在盒模型那个章节，我们了解到元素盒子如果加入了内边距 padding 和边框 border 后，它的总长度会增加。那么如果这个元素用于非常精确的布局时，我们就需要进行计算增减。这其实是比较烦人的操作。尤其是动态设置页面布局的时候。<br>
CSS3提供了一个属性 box-sizing,这个属性可以定义元素盒子的解析方式，从而可以选择避免掉布局元素盒子增加内边距和边框的长度增减问题。
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>content-box</td><td>默认值,border 和 padding 设置后用于元素的总长度。</td></tr>
<tr><td>border-box</td><td>border 和 padding 设置后不用于元素的总长度</td></tr>
</table>
</html>
//设置 border-box 让 border 和 padding 不在额外增加元素大小<br>

## 三、resize ##
CSS3 提供了一个 resize 属性，来更改元素尺寸大小。
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>none</td><td>默认值,不允许用户调整元素大小。</td></tr>
<tr><td>both</td><td>用户可以调节元素的宽度和高度。</td></tr>
<tr><td>horizontal</td><td>用户可以调节元素的宽度。</td></tr>
<tr><td>vertical</td><td>用户可以调节元素的高度。</td></tr>
</table>
</html>
<br>
一般普通元素，默认值是不允许的。但如果是表单类的 textarea 元素，默认是允许的。而普通元素需要设置 overflow:auto。配合 resize 才会出现可拖曳的图形。

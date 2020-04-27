# CSS3 多列布局 #
本章主要探讨 HTML5 中 CSS3 提供的多列布局,通过多列布局我们方便的创建流体的多列布局。
## 一、早期多列问题 ##
我们有时想布局成报纸、杂志那样的多列方式(至少两列，一般三列以上)，但早期 CSS 提供的布局方式都有着极大的限制。如果是固体布局，那么使用浮动或定位布局都可以完成。但对于流体的多列，比如三列以上，那只能使用浮动布局进行，而它又有极大的限制。因为它是区块性的。对于动态的内容无法伸缩自适应，基本无能力。<br>
## 属性及版本 ##
CSS3 提供了 columns 多列布局属性等7个属性集合，具体如下：
<html>
<table>
<tr><td>属性</td><td>说明</td></tr>
<tr><td>columns</td><td>集成 column-width 和 column-count两个属性</td></tr>
<tr><td>columns-width</td><td>定义每列宽度</td></tr>
<tr><td>column-count</td><td>定义分分列列数</td></tr>
<tr><td>column-gap</td><td>定义列间距</td></tr>
<tr><td>column-rule</td><td>定义列边框</td></tr>
<tr><td>column-span</td><td>定义多列布局中子元素跨列效果,firefox不支持</td></tr>
<tr><td>column-fill</td><td>控制每列的列高效果，主流浏览器不支持</td></tr>
</table>
</html>
由于 column 属性尚未纳入标准。大多数浏览器必须使用厂商前缀才能访问，好在主流浏览器都可以很好的支持了。下面是主流浏览器的支持和前缀情况。
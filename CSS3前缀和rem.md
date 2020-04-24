# CSS3前缀和rem #
本章主要探讨 HTML5 中 CSS在发展中实行标准化的一些问题。重点探讨 CSS3 中新属性前缀问题和新的单位 rem。
## 一、CSS3 前缀 ##
在CSS3 的很多新属性推出时，这些属性还处在不太稳定的阶段，随时可能被删除而此时的浏览器厂商为了实现这些属性，采用前缀方法。各大厂商前缀列表如下：
<html>
<table>
<tr><td>浏览器</td><td>厂商前缀</td></tr>
<tr><td>Chrome、Safari</td><td>-webkit-</td></tr>
<tr><td>Opera</td><td>-o-</td></tr>
<tr><td>Firefox</td><td>-moz-</td></tr>
<tr><td>Internet Explorer</td><td>-ms-</td></tr>
</table>
</html>

我们之前学习过几个 CSS3 的新属性，比如：box-shadow、border-radius、opacity等。这几个属性我们在前面的使用中，并没有添加所谓的浏览器厂商前缀。那是因为，这些属性已经在主流浏览器或版本成为了标准。具体进化步骤如下：
1.属性尚未提出，这个属性所有浏览器不可用：
2.属性被提出，但未列入标准，浏览器厂商通过私有前缀来支持该属性;
3.属性被列入标准，可以使用前缀或不使用前缀来实现属性特性:
4.属性不需要再使用厂商前缀。具体浏览器支持度如下:

<html>
<table border="1">
        <tr>
            <td>属性</td>
            <td>浏览器</td>
            <td>带前缀版本</td>
            <td>不带前缀</td>
            <td>标准/实验</td>
        <tr>
        <tr>
            <td rowspan="7">border-radius</td>
            <td>IE</td>
            <td>不支持</td>
            <td>9.0</td>
            <td rowspan="7">标准</td>
        <tr>
        <tr>
            <td>Firefox</td>
            <td>3.0需带 -moz-</td>
            <td>4.0+</td>
        <tr>
        <tr>
            <td>Safari</td>
            <td>3.1需带 -webkit-</td>
            <td>5.1+</td>
        <tr>
        <tr>
            <td>Chrome</td>
            <td>不支持</td>
            <td>10.5+</td>
        <tr>
    </table>
</html>
如果是手机等移动端一般采用的是 IOS 或安卓系统，那么基本上它的引擎是 webkit,直接参考 -webkit- 即可。
在 CSS3 手册上， Chrome支持 border-radius的版本为 13.0.而部分教材和文章上写到只要5.0。当然，这里可能表达的含义可能不同。而截至到2015年4月份最新的 Chrome版本已经升级到 41.0了。所以，不管是 5.0还是13.0都是老古董了，没必要深究。Opera 支持 border-radius 版本为 11.5,而目前的版本是 28.0，也无伤大雅了。
而被列入标准的 box-shadow 和 opacity 基本与 border-radius 前缀一致。

## 二、长度单位 rem ##
CSS3引入了一些新的尺寸单位，这里重点推荐一个: rem或者称为(根 em)。目前主流的现代浏览器都很稳定的支持。它和 em、百分比不同的是，它不是与父元素挂钩，而是相对于根元素&lt;html&gt;的文本大小来计算的，这样能更好的统一整体页面的风格。

rem支持度
<html>
<table>
<tr><td>浏览器</td><td>rem 单位</td></tr>
<tr><td>Opera</td><td>11.6+</td></tr>
<tr><td>Firefox</td><td>3.0</td></tr>
<tr><td>Safari</td><td>5.0+</td></tr>
<tr><td>Chrome</td><td>6.0+</td></tr>
<tr><td>IE</td><td>9.0+</td></tr>
</table>
</html>


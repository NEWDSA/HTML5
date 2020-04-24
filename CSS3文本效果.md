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
text-shadow:0px 0px rgb(188,178,188)
</text>

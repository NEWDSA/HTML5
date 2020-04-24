# CSS 其他样式 #
本章主要探讨HTML5中其他剩下几个常用的样式，包括颜色、透明度、盒子的阴影轮廓以及光标的样式
## 一、颜色和透明度 ##
颜色我们之前其实已经用的很多了，比如字体颜色、背景颜色、边框颜色。但除了背景颜色和边框颜色讲解过，字体颜色却没有系统的讲解过。设置字体颜色其实也成为文本块的前景色。
| 属性    | 值   | 说明      | CSS版本 |   |
|-------|-----|---------|-------|---|
| color | 颜色值 | 设置文本前景色 | 1     |   |
CSS3提供了一个属性 opacity，可以设置元素的透明度。
| 属性      | 值   | 说明       | CSS版本 |   |
|---------|-----|----------|-------|---|
| opacity | 0~1 | 设置元素的透明度 | 3     |   |
## 二、盒子阴影和轮廓 ##
### 1.box-shadow ####
CSS3提供了一个非常实用的效果样式，就是阴影效果。通过 box-shadow 属性来实现。样式表如下：
<html>
<table>
<tr><td>属性</td><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td rowspan="7">box-shadow</td><td>hoffset</td><td>阴影的水平偏移量，是一个长度值，正值表示阴影向右偏移，负值表示阴影向左偏移。</td><td>3</td></tr>
<tr><td>voffset</td><td>阴影的垂直偏移量，是一个长度值，正值代表阴影位于元素盒子的下方，负值代表阴影位于元素盒子的上方。</td></tr>
<tr><td>blur</td><td>(可选)指定模糊值，是一个长度值，值越大盒子的边界越模糊，默认值为0，边界清晰。</td><td>3</td></tr>
<tr><td>spread</td><td>(可选)设置阴影延伸半径，是一个长度值，正值代表阴影向盒子各个方向延伸扩大，负值代表阴影沿相反方向缩小</td><td>3</td><tr>
<tr><td>color</td><td>(可选)设置阴影的颜色，如果省略，浏览器会自行选择一个颜色</td><td>3</td></tr>
<tr><td>inset</<td><td>(可选)将外部阴影设置为内部阴影。</td><td>3</td><tr>
</table>
</html>

### 2.outline ###
CSS3还提供了轮廓样式，它和边框一样，只不过它可以在边框的外围再加一层。样式表如下：
| 属性              | 值   | 说明                     | CSS版本 |
|-----------------|-----|------------------------|-------|
| outline\-color  | 颜色  | 外围轮廓的颜色                | 3     |
| outline\-offset | 长度  | 轮廓距离元素边缘的偏移量           | 3     |
| outline\-style  | 样式  | 轮廓样式，和 border\-style一致 | 3     |
| outline\-width  | 长度  | 轮廓宽度                   | 3     |
| outline         | 简写 | <颜色> <样式> <宽度>                    | 3     |
## 三、光标样式 ##
我们不但可以指定页面上的元素样式，就连光标的样式也可以指定。样式表如下：
<html>
<table>
<tr><td>属性</td><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td>cursor</td><td>光标样式</td><td>auto,default,none,context-menu,help,pointer,progress,wait,cell,crosshair,text,vertical-text,alias,copy,move,no-drop,not-allowed,e-resize,n-resize,ne-resize,nw-resize,s-resize,se-resize,sw-resize,w-resize,ew-resize,ns-resize,nesw-resize,nwse-resize,col-resize,row-resize,all-scroll</td><td>1</td></tr>
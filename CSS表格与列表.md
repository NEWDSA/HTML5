# CSS表格与列表 #
本章主要探讨 HTML5 中 CSS 表格和列表，通过表格和列表的样式设置，让表格和列表显示更加多元化
## 表格样式 ##
表格有五种独有样式，样式表如下：
<html>
<table>
<tr>
<td>属性</td><td>值</td><td>说明</td><td>CSS版本</td>
</tr>
<tr>
<td>border-collapse</td><td>边框样式</td><td>相邻单元格边框间距</td><td>2</td>
</tr>
<tr>
<td>border-spacing</td><td>长度值</td><td>相邻单元格的间距</td><td>2</td>
</tr>
<tr>
<td>caption-side</td><td>位置名称</td><td>表格标题位置</td><td>2</td>
</tr>
<tr>
<td>empty-cells</td><td>显示值</td><td>单元格是否显示边框</td><td>2</td>
</tr>
<tr>
<td>table-layout</td><td>布局样式</td><td>指定表格的布局样式</td><td>2</td>
</tr>
</table>
</html>
1.border-collapse
<html>
<table>
 <tr>
 <td>值</td><td>说明</td><td>CSS版本</td>
 </tr>
 <tr>
 <td>separate</td><td>默认值，单元格边框独立</td><td>2</td>
 <tr>
 <td>collapse</td><td>单元格相邻边框被合并</td><td>2</td>
 </tr>
</table>
</html>
2.border-spacing
<html>
<table>
<tr>
 <td>值</td><td>说明</td><td>CSS版本</td>
 </tr>
 <tr>
 <td>长度值</td><td>0表示间距，其他使用CSS长度值</td><td>2</td>
 </tr>
 </table>
</html>
3.table-layout
<html>
<table>
<tr>
<td>值</td><td>说明</td><td>CSS版本</td>
</tr>
<tr>
<td>auto</td><td>默认值，内容过长时,拉伸整个单元格</td><td>2</td>
</tr>
<tr>
<td>fixed</td><td>内容过长时不拉伸整个单元格</td><td>2</td>
</tr>
</table>
</html>

## 二、列表样式 ##
列表有四种独有样式，样式表如下:
<html>
    <table>
    <tr>
    <td>属性</td><td>值</td><td>说明</td><td>CSS版本</td>
    </tr>
    <td>list-style-type</td><td>类型值</td><td>列表中的标记类型</td><td>1/2</td>
    </tr>
    <td>list-style-image</td><td>none或url</td><td>图像作为列表标记</td><td>CSS1本</td>
    </tr>
    </tr>
    <td>list-style-position</td><td>位置值</td><td>排列的相对位置</td><td>1</td>
    </tr>
    </tr>
    <td>list-style</td><td>简写属性</td><td>列表简写形式</td><td>1</td>
    </tr>
    </table>
</html>

list-style-type
<html>
<table>
<tr><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td>none</td><td>没有标记</td><td>1</td></tr>
<tr><td>disc</td><td>实心圈</td><td>1</td></tr>
<tr><td>circle</td><td>空心圈</td><td>1</td></tr>
<tr><td>squaree</td><td>实心方块</td><td>1</td></tr>
<tr><td>decimal</td><td>阿拉伯数字</td><td>1</td></tr>
<tr><td>lower-roman</td><td>小写罗马数字</td><td>1</td></tr>
<tr><td>upper-roman</td><td>大写罗马数字</td><td>1</td></tr>
<tr><td>lower-alpha</td><td>小写英文字母</td><td>1</td></tr>
<tr><td>upper-roman</td><td>大写英文字母</td><td>1</td></tr>
</table>
</html>

list-type-position

<html>
<table>
<tr>
<td>值</td><td>说明</td><tdd>CSS版本</tdd>
</tr>
<tr>
<td>outside</td><td>默认值，标记位于内容框外部</td><tdd>1</tdd>
</tr>
<tr>
<td>inside</td><td>标记位于内容框内部</td><tdd>1</tdd>
</tr>
</table>
</html>

list-type-image
<html>
<table>
<tr><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td>none</td><td>不使用图像</td><td>1</td></tr>
<tr><td>url</td><td>通过url使用图像</td><td>1</td></tr>
</table>
</html>

## 三、其他功能 ##
在&lt;table&gt;中&lt;td&gt;单元格，我们可以使用text-align属性水平对齐，但是垂直对齐就无法操作了。CSS提供了 vertical-align属性用于垂直对齐。
<html>
<table>
<tr><td>值</td><td>说明</td><td>1</td></tr>
<tr><td>baseline</td><td>内容对象与基线对齐</td><td>1</td></tr>
<tr><td>top</td><td>内容对象与顶端对齐</td><td>1</td></tr>
<tr><td>middle</td><td>内容对象与中部对齐</td><td>1</td></tr>
<tr><td>bottom </td><td>内容对象与底部对齐</td><td>1</td></tr>
</table>
</html>

文本内容对齐方式

<html>
<table>
<tr><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td>sub</td><td>垂直对齐文本的下标</td><td>1</td></tr>
<tr><td>super</td><td>垂直对齐文本的上标</td><td>1</td></tr>
</table>
</html>

对普通文本内容对齐方式长度值和百分比（实现垂直居中）

<html>
<table>
<tr><td>值</td><td>说明</td><td>CSS版本</td></tr>
<tr><td>长度值</td><td>设置上下的偏移量</td><td>1</td></tr>
<tr><td>百分比</td><td>设置上下的偏移量</td><td>1</td></tr>
</table>
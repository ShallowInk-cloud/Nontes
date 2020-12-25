#HTML

---

## 标签：

### 1、`<!--...-->`

注释标签用于在源代码中插入注释。注释不会显示在浏览器中。

您可使用注释对您的代码进行解释，这样做有助于您在以后的时间对代码的编辑。当您编写了大量代码时尤其有用。

```html
`<!--这是一个注释，不会显示在浏览器中-->`
```



### 2、`<!DOCTYPE html>`

声明该文档是HTML5文档

``` html
<!DOCTYPE html>
```



### 3、`<a>`

标签定义超链接

``` html
<a href="###"> 网页名称 <a>
```

a标签的href属性用于指向链接地址

标签内部可以添加文字或图片，来为文字和图片增加超链接

| 属性           | 值                                | 描述                                                 |
| :------------- | :-------------------------------- | :--------------------------------------------------- |
| charset        | *char_encoding*                   | HTML5 中不支持。规定被链接文档的字符集。             |
| coords         | *coordinates*                     | HTML5 中不支持。规定链接的坐标。                     |
| download:five: | *filename*                        | 规定被下载的超链接目标。                             |
| href           | *URL*                             | 规定链接指向的页面的 URL。                           |
| hreflang       | *language_code*                   | 规定被链接文档的语言。                               |
| media:five:    | *media_query*                     | 规定被链接文档是为何种媒介/设备优化的。              |
| name           | *section_name*                    | HTML5 中不支持。规定锚的名称。                       |
| rel            | *text*                            | 规定当前文档与被链接文档之间的关系。                 |
| rev            | *text*                            | HTML5 中不支持。规定被链接文档与当前文档之间的关系。 |
| shape          | defaultrectcirclepoly             | HTML5 中不支持。规定链接的形状。                     |
| target         | _blank_parent_self_top*framename* | 规定在何处打开链接文档。                             |
| type:five:     | *MIME type*                       | 规定被链接文档的的 MIME 类型。                       |

### 4、`<abbr>`

标记一个缩写,比如 "WWW" 、 "NATO"

结合使用全局的 title 属性，可以实现当你把鼠标放在缩写上时，会显示简称或者缩写的完整版本。

```html
The <abbr title="People's Republic of China">PRC</abbr> was founded 1949.
```

鼠标放在文字"PRC"上，会显示全称"People's Republic of China"

### 5、`<acronym>`

==**H5中不支持此类标签，请使用`<abbr>`代替该标签**==

```html
<acronym title="World Wide Web">WWW</acronym>
```

与H5中的[`<abbr>`](#4、`<abbr>`)标签功能相同，现在已被替代

### 6、`<address>`

定义文档或文章的作者/拥有者的联系信息

如果` <address> `元素位于` <body> `元素内，则它表示文档联系信息。

如果 `<address> `元素位于 `<article> `元素内，则它表示文章的联系信息。

`<address> `元素中的文本通常呈现为斜体。大多数浏览器会在 address 元素前后添加折行。

`<address> `元素通常连同其他信息被包含在 `<footer> `元素中。

```html
<address>
Written by <a href="mailto:webmaster@example.com">Donald Duck</a>.<br> 
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>
```

### 7、`<applet>`

==**HTML5 中不支持 `<applet>` 标签。请使用标签代替。**==

​	与H5中的[`<object>`](#`<object>`) 标签功能相同，现在已被替代

**必须属性**

| 属性   | 值     | 描述                                         |
| :----- | :----- | :------------------------------------------- |
| code   | *URL*  | 规定 Java applet 的文件名。                  |
| object | *name* | 定义了包含该 applet 的一系列版本的资源名称。 |

**可选属性**

| 属性     | 值                                                        | 描述                                       |
| :------- | :-------------------------------------------------------- | :----------------------------------------- |
| align    | leftrighttopbottommiddlebaselinetexttopabsmiddleabsbottom | 定义 applet 相对于周围元素的对齐方式。     |
| alt      | *text*                                                    | 规定 applet 的替换文本。                   |
| archive  | *URL*                                                     | 规定档案文件的位置。                       |
| codebase | *URL*                                                     | 规定 code 属性中指定的 applet 的基准 URL。 |
| height   | *pixels*                                                  | 定义 applet 的高度                         |
| hspace   | *pixels*                                                  | 定义围绕 applet 的水平间隔。               |
| name     | *unique_name*                                             | 规定 applet 的名称（用在脚本中的）。       |
| vspace   | *pixels*                                                  | 定义围绕 applet 的垂直间隔。               |
| width    | *pixels*                                                  | 定义 applet 的宽度                         |

### 8、`<area>`

`<area> `标签定义图像映射中的区域(可点击的图像)

area 元素总是嵌套在 `<map> `标签中。

`<img> `标签中的 usemap 属性与 map 元素 name 属性相关联，创建图像与映射之间的联系。

```html
<img src="planets.jpg" border="0" usemap="#planetmap" alt="Planets" />

<map name="planetmap" id="planetmap">
  <area shape="circle" coords="180,139,14" href ="venus.html" alt="Venus" />
  <area shape="circle" coords="129,161,10" href ="mercur.html" alt="Mercury" />
  <area shape="rect" coords="0,0,110,260" href ="sun.html" alt="Sun" />
</map>
```

**必须属性**

| 属性 | 值     | 描述                   |
| :--- | :----- | :--------------------- |
| alt  | *text* | 定义此区域的替换文本。 |

**可选属性**

| 属性   | 值                     | 描述                                       |
| :----- | :--------------------- | :----------------------------------------- |
| coords | 坐标值                 | 定义可点击区域（对鼠标敏感的区域）的坐标。 |
| href   | *URL*                  | 定义此区域的目标 URL。                     |
| nohref | nohref                 | 从图像映射排除某个区域。                   |
| shape  | defaultrectcircpoly    | 定义区域的形状。                           |
| target | _blank_parent_self_top | 规定在何处打开 href 属性指定的目标 URL。   |

### 9、`<artical>`

```html
<article>
  <h1>Internet Explorer 9</h1>
  <p>Windows Internet Explorer 9（简称 IE9）于 2011 年 3 月 14 日发布.....</p>
</article>
```

表示的区域为文章内容

### 10、`<aside>`

`<aside> `标签定义其所处内容之外的内容，也可以做侧边栏。

`<aside>` 的内容应该与附近的内容相关。

```html
<p>Me and my family visited The Epcot center this summer.</p>
<aside>
<h4>Epcot Center</h4>
The Epcot Center is a theme park in Disney World, Florida.
</aside>
```

### 11、`<audio>`

```html
<audio src="someaudio.wav">
您的浏览器不支持 audio 标签。
</audio>
```

可以在开始标签和结束标签之间放置文本内容，这样老的浏览器就可以显示出不支持该标签的信息。

| 属性           | 值       | 描述                                                         |
| :------------- | :------- | :----------------------------------------------------------- |
| autoplay:five: | autoplay | 如果出现该属性，则音频在就绪后马上播放。                     |
| controls:five: | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。             |
| loop:five:     | loop     | 如果出现该属性，则每当音频结束时重新开始播放。               |
| muted:five:    | muted    | 规定视频输出应该被静音。                                     |
| preload:five:  | preload  | 如果出现该属性，则音频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
| src:five:      | *url*    | 要播放的音频的 URL。                                         |

### 12、`<b>`

标签规定粗体文本

```html
<p>这是普通文本 - <b>这是粗体文本</b>。</p>
```

### 13、`<base>`

```html
<head>
<base href="http://www.w3school.com.cn/i/" />
<base target="_blank" />
</head>

<body>
<img src="eg_smile.gif" />
<a href="http://www.w3school.com.cn">W3School</a>
</body>
```

`<base> `标签为**页面上的所有链接**规定默认地址或默认目标。

通常情况下，浏览器会从当前文档的 URL 中提取相应的元素来填写相对 URL 中的空白。

使用` <base> `标签可以改变这一点。浏览器随后将不再使用当前文档的 URL，而使用指定的基本 URL 来解析所有的相对 URL。这其中包括 `<a>`、`<img>`、`<link>`、`<form> `标签中的 URL。

### 14、`<basefont>`

```html
<head>
<basefont color="red" size="5" />
</head>

<body>
<h1>This is a header</h1>
<p>This is a paragraph</p>
</body>
```

只有 Internet Explorer 支持 `<basefont> `标签。应该避免使用该标签。

| 属性  | 值                               | 描述                                                     |
| :---- | :------------------------------- | :------------------------------------------------------- |
| color | *rgb(x,x,x)**#xxxxxx**colorname* | 不赞成使用。请使用样式取代它。规定文档中的默认文本颜色。 |
| face  | *font_family*                    | 不赞成使用。请使用样式取代它。规定文档中的默认字体。     |
| size  | *number*                         | 不赞成使用。请使用样式取代它。规定文档中的默认字体大小。 |

### 15、`<bdi>`

```html
<ul>
<li>Username <bdi>Bill</bdi>:80 points</li>
<li>Username <bdi>Steve</bdi>: 78 points</li>
</ul>
```

bdi 指的是 bidi 隔离。

`<bdi> `标签允许您设置一段文本，使其脱离其父元素的文本方向设置。

在发布用户评论或其他您无法完全控制的内容时，该标签很有用。

### 16、`<bdo>`

```html
<bdo dir="rtl">Here is some text</bdo>
```

bdo 元素可覆盖默认的文本方向。

| 属性 | 值       | 描述           |
| :--- | :------- | :------------- |
| dir  | ltr  rtl | 定义文字的方向 |

### 17、`<html>`

它叫做`html`标签，也叫作根标签

告诉浏览器文件的内容是HTML

``` html
<html>
    
</html>
```

### 18、`<head>`

首部文件，包含WEB页面的有关信息，如页面标题。现在可以这样考虑：通过首部可以告诉浏览器关于Web页面的信息

`<head>` 元素是所有头部元素的容器。

`<head> `元素必须包含文档的标题（title），可以包含脚本、样式、meta 信息 以及其他更多的信息。

以下列出的元素能被用在` <head> `元素内部：

> `<title>`
>
> `<style>`
>
> `<base>`
>
> `<link>`
>
> `<meta>`
>
> `<script>`
>
> `<noscript>`

```html
<head>
<meta charset="utf-8">
<title>文档标题</title>
</head>
```

### 19、`<title>`

在`<head>`标记中放入title标记。`<title>`总出现在浏览器窗口的顶部。

`<title> `元素可定义文档的标题。

浏览器会以特殊的方式来使用标题，并且通常把它放置在浏览器窗口的标题栏或状态栏上。同样，当把文档加入用户的链接列表或者收藏夹或书签列表时，标题将成为该文档链接的默认名称。

```html
<html>
    <title>页面的名称</title>
</html>
```

### 20、`<body>`

网页主体包括`<body>`和`</body>`标记以及它们之间的所有内容，这就是你在浏览器看到的部分

```html
<body>
    
</body>
```

### 21、`<h>`

标题总共有六级

```html
<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6></h6>
```

`<h1>`级别最高，以此类推（越高级的标签会用更大的字体显示）

### 22、`<p>`

段落标签，该标签里的内容会独占一行

p 元素会自动在其前后创建一些空白。浏览器会自动添加这些空间，您也可以在样式表中规定。

```html
<p>
    
</p>
```

### 23、`<img>`

图片标签,是一个单标签

`<img> `标签定义 HTML 页面中的图像。

`<img> `标签有两个必需的属性：src 和 alt。

**注释：**从技术上讲，图像并不会插入 HTML 页面中，而是链接到 HTML 页面上。<img> 标签的作用是为被引用的图像创建占位符。

**提示：**通过在` <a>` 标签中嵌套` <img> `标签，给图像添加到另一个文档的链接。

| 属性              | 值                           | 描述                                                         |
| :---------------- | :--------------------------- | :----------------------------------------------------------- |
| align             | top bottom middle left right | HTML5 不支持。HTML 4.01 已废弃。 规定如何根据周围的文本来排列图像。 |
| alt               | *text*                       | 规定图像的替代文本。                                         |
| border            | *pixels*                     | HTML5 不支持。HTML 4.01 已废弃。 规定图像周围的边框。        |
| crossorigin:five: | anonymous use-credentials    | 设置图像的跨域属性                                           |
| height            | *pixels*                     | 规定图像的高度。                                             |
| hspace            | *pixels*                     | HTML5 不支持。HTML 4.01 已废弃。 规定图像左侧和右侧的空白。  |
| ismap             | ismap                        | 将图像规定为服务器端图像映射。                               |
| longdesc          | *URL*                        | HTML5 不支持。HTML 4.01 已废弃。 指向包含长的图像描述文档的 URL。 |
| src               | *URL*                        | 规定显示图像的 URL。                                         |
| usemap            | *#mapname*                   | 将图像定义为客户器端图像映射。                               |
| vspace]           | *pixels*                     | HTML5 不支持。HTML 4.01 已废弃。 规定图像顶部和底部的空白。  |
| width             | *pixels*                     | 规定图像的宽度。                                             |

```html
<img loading="lazy" src="smiley-2.gif" alt="Smiley face" width="42" height="42">
```

### 24、`<style>`

在`<head>`标签内用于描述CSS样式

`<style>` 标签用于为 HTML 文档定义样式信息。


在 style 中，您可以规定在浏览器中如何呈现 HTML 文档。

type 属性是必需的，定义 style 元素的内容。唯一可能的值是 "text/css"。

style 元素位于 head 部分中。

```html
<head>
    <style>		</style>
</head>
```

### 25、`<hr>`

水平线标签，单标签

`<hr> `标签定义 HTML 页面中的主题变化（比如话题的转移），并显示为一条水平线。

`<hr> `元素被用来分隔 HTML 页面中的内容（或者定义一个变化）。

```html
<hr>
```

### 26、`<ul>`

无序列表标签

```html
<ul>
    
</ul>
```

### 27、`<ol>`

有序列表标签

```html
<ol>
    
</ol>
```

### 28、`<li>`

`<li>` 标签定义列表项目。

`<li> `标签可用在有序列表 (`<ol>`) 和无序列表 (`<ul>`) 中。

```html
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>
<ol>
    <li></li>
    <li></li>
    <li></li>
</ol>
```

### 29、`<big>`

`<big>` 标签呈现大号字体效果。

使用`<big> `标签可以很容易地放大字体。

每一个 `<big>` 标签都可以使字体大一号，直到上限 7 号文本，正如字体模型所定义的那样。

但是使用 `<big>` 标签的时候还是要小心，因为浏览器总是很宽大地试图去理解各种标签，对于那些不支持` <big> `标签的浏览器来说，它经常将其认为是粗体字标签。

``` html
<big>
    此处输入想要放大的字体
</big>
```

### 30、`<blockquote>`

`<blockquote>` 标签定义摘自另一个源的块引用。(它本身是一个块元素)

浏览器通常会对` <blockquote> `元素进行缩进。（左右两侧缩进40px的文本）

| 属性 | 值    | 描述             |
| :--- | :---- | :--------------- |
| cite | *URL* | 规定引用的来源。 |

### 31、`<br>`

它是换行标签，也是空标签，因此便签内并没有实际内容

在 HTML 中，`<br>` 标签没有结束标签

在 XHTML 中，`<br>` 标签必须被正确地关闭，比如这样：`<br />` 

```html
<span>文字内容</span>	<br>
```

### 32、`<button>`

`<button>` 标签定义一个按钮。

在 `<button>` 元素内部，您可以放置内容，比如文本或图像。这是该元素与使用 `<input>` 元素创建的按钮之间的不同之处。

**提示：**请始终为` <button> `元素规定 type 属性。不同的浏览器对 `<button> `元素的 type 属性使用不同的默认值。

```html
<button type="button">
    点我！
</button>
```

| 属性                 | 值                                                           | 描述                                                         |
| :------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| autofocus:five:      | autofocus                                                    | 规定当页面加载时按钮应当自动地获得焦点。                     |
| disabled             | disabled                                                     | 规定应该禁用该按钮。                                         |
| form:five:           | *form_id*                                                    | 规定按钮属于一个或多个表单。                                 |
| formaction:five:     | *URL*                                                        | 规定当提交表单时向何处发送表单数据。覆盖 form 元素的 action 属性。该属性与 type="submit" 配合使用。 |
| formenctype:five:    | application/x-www-form-urlencoded multipart/form-data text/plain | 规定在向服务器发送表单数据之前如何对其进行编码。覆盖 form 元素的 enctype 属性。该属性与 type="submit" 配合使用。 |
| formmethod:five:     | get post                                                     | 规定用于发送表单数据的 HTTP 方法。覆盖 form 元素的 method 属性。该属性与 type="submit" 配合使用。 |
| formnovalidate:five: | formnovalidate                                               | 如果使用该属性，则提交表单时不进行验证。覆盖 form 元素的 novalidate 属性。该属性与 type="submit" 配合使用。 |
| formtarget:five:     | _blank _self _parent _top *framename*                        | 规定在何处打开 action URL。覆盖 form 元素的 target 属性。该属性与 type="submit" 配合使用。 |
| name                 | *name*                                                       | 规定按钮的名称。                                             |
| type                 | button reset submit                                          | 规定按钮的类型。                                             |
| value                | *text*                                                       | 规定按钮的初始值。可由脚本进行修改。                         |

### 33、`<canvas>`

`<canvas>` 标签通过脚本（通常是 JavaScript）来绘制图形（比如图表和其他图像）。

`<canvas> `标签只是图形容器，您必须使用脚本来绘制图形。

| 属性         | 值       | 描述             |
| :----------- | :------- | :--------------- |
| height:five: | *pixels* | 规定画布的高度。 |
| width:five:  | *pixels* | 规定画布的宽度。 |

```html
<canvas id="MyCanvas"></canvas>

<script type="text/javascript">
var canvas=document.getElementById('myCanvas');
var ctx=canvas.getContext('2d');
ctx.fillStyle='#FF0000';
ctx.fillRect(0,0,80,100);
</script>
```

### 34、`<caption>`

`<caption>` 标签定义表格的标题。

> `<caption>` **标签必须直接放置到** `<table>`**标签之后**。

您只能对每个表格定义一个标题。

**提示：**通常这个标题会被居中于表格之上。然而，CSS 属性 "text-align" 和 "caption-side" 能用来设置标题的对齐方式和显示位置。

> 它有一个属性：align。但是H4.0.1开始就废弃了，H5并不支持该属性

```html
<table>
    <caption>This is a table</caption>
    <tr>
        行
    	<td>列</td>
    </tr>
</table>
```



### 35、`<center>`

进行水平处理与居中

==**H5不支持此标签**==

| 属性  | 值                 | 描述                     |
| :---- | :----------------- | :----------------------- |
| class | *classname*        | 规定元素的类名           |
| dir   | rtl ltr            | 规定元素中内容的文本方向 |
| id    | *id*               | 规定元素的唯一 id        |
| lang  | *language_code*    | 规定元素中内容的语言代码 |
| style | *style_definition* | 规定元素的行内样式       |
| title | *text*             | 规定元素的额外信息       |

```html
<center>居中内容</center>
```

### 36、`<cite>`

`<cite>` 标签定义作品（比如书籍、歌曲、电影、电视节目、绘画、雕塑等等）的标题。

一般内容会呈现斜体

**注释：**人名不属于作品的标题。

```html
<p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
```

### 37、`<code>`

`<code> `标签是一个短语标签，用来定义计算机代码文本。

**提示：**我们并不反对使用这个标签，但是如果您只是为了达到某种视觉效果而使用这个标签的话，我们建议您使用 CSS ，这样可能会取得更丰富的效果。

| 标签       | 描述                                                         |
| :--------- | :----------------------------------------------------------- |
| `<em>`     | 呈现为被强调的文本。                                         |
| `<strong>` | 定义重要的文本。                                             |
| `<dfn>`    | 定义一个定义项目。                                           |
| `<code>`   | 定义计算机代码文本。                                         |
| `<samp>`   | 定义样本文本。                                               |
| `<kbd>`    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| `<var>`    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

```html
<code>一段电脑代码 print("Hello World")</code>
```

### 38、`<col>`

`<col>` 标签规定了`<colgroup>` 元素内部的每一列的列属性。

通过使用 `<col>` 标签，可以向整个列应用样式，而不需要重复为每个单元格或每一行设置样式。

| 属性     | 值                             | 描述                                                         |
| :------- | :----------------------------- | :----------------------------------------------------------- |
| align    | left right center justify char | HTML5 不支持。规定与 `<col>` 元素相关的内容的水平对齐方式。  |
| char     | *character*                    | HTML5 不支持。规定根据哪个字符来对齐与 `<col> `元素相关的内容。 |
| charoff  | *number*                       | HTML5 不支持。规定第一个对齐字符的偏移量。                   |
| **span** | *number*                       | 规定 `<col>` 元素应该横跨的列数。                            |
| valign   | top middle bottom baseline     | HTML5 不支持。规定与 `<col> `元素相关的内容的垂直对齐方式。  |
| width    | *% pixels relative_length*     | HTML5 不支持。Specifies the width of a `<col> `element       |

```html
<table border="1">
  <colgroup>
    <col span="2" style="background-color:red">
    <col style="background-color:yellow">
  </colgroup>
  <tr>
    <th>ISBN</th>
    <th>Title</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>3476896</td>
    <td>My first HTML</td>
    <td>$53</td>
  </tr>
</table>
```



### 39、`<colgroup>`

`<colgroup> `标签用于对表格中的列进行组合，以便对其进行格式化。

通过使用 `<colgroup>` 标签，可以向整个列应用样式，而不需要重复为每个单元格或每一行设置样式。

**注释：**只能在 `<table> `元素之内，在任何一个 `<caption>` 元素之后，在任何一个 `<thead>`、`<tbody>`、`<tfoot>`、`<tr>` 元素之前使用 `<colgroup> `标签。

**提示：**如果想对 `<colgroup> `中的某列定义不同的属性，请在 `<colgroup> `标签内使用 标签。

```html
<table border="1">
  <colgroup>
    <col span="2" style="background-color:red">
    <col style="background-color:yellow">
  </colgroup>
  <tr>
    <th>ISBN</th>
    <th>Title</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>3476896</td>
    <td>My first HTML</td>
    <td>$53</td>
  </tr>
</table>
```

`<colgroup>`搭配`<col>`一起使用

第个`<col>`标签代表第一列，以此类推...

可以用`<colspan>`一下设置多列

### 40、`<command>`

`<command>` 标签可以定义用户可能调用的命令（比如单选按钮、复选框或按钮）。

当使用`<menu> `元素时，command 元素将作为菜单或者工具栏的一部分显示出来。但是，用 command 规定键盘快捷键时，command元素能被放置在页面的任何位置，但元素不可见。

| 属性             | 值                     | 描述                                                         |
| :--------------- | :--------------------- | :----------------------------------------------------------- |
| checked:five:    | checked                | 规定当页面加载时，command 是否被选中。仅用于 radio 或 checkbox 类型。 |
| disabled:five:   | disabled               | 规定 command 是否可用。                                      |
| icon:five:       | *URL*                  | 规定作为 command 来显示的图像的 URL。                        |
| label:five:      | *text*                 | 必需。规定 command 的名字，对用户可见。                      |
| radiogroup:five: | *groupname*            | 规定可进行切换且将被切换的 command 所属的组名。仅在类型为 radio 时使用。 |
| type:five:       | checkbox command radio | 定义 command 的类型。默认是 "command"。                      |

```html
<menu>
<command type="command" label="Save" onclick="save()">Save</command>
</menu>
```



### 41、`<datalist>`

`<datalist> `标签规定了` <input>`元素可能的选项列表。

`<datalist> `标签被用来在为` <input>` 元素提供"自动完成"的特性。*(用户填写信息时候，可以通过下拉菜单选择填入信息)*

用户能看到一个下拉列表，里边的选项是预先定义好的，将作为用户的输入数据。

请使用 `<input> `元素的 list 属性来绑定 `<datalist> `元素。

```html
<input list="browsers">
<datalist id="browsers">
  <option value="Internet Explorer">
  <option value="Firefox">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
```



### 42、`<dd>`

`<dd> `标签被用来对一个描述列表中的项目/名字进行描述。

`<dd> `标签与  `<dl>`（定义一个描述列表）和`<dt>`（定义项目/名字）一起使用。

在 `<dd>` 标签内，您能放置段落、换行、图片、链接、列表等等。

```html
<dl>
  <dt>Coffee</dt>
    <dd>Black hot drink</dd>
  <dt>Milk</dt>
    <dd>White cold drink</dd>
</dl>
```

> 在`<dt>`标签内的`<dd>`会自动缩进

### 43、`<del>`

`<del> `标签定义文档中已删除的文本。

```html
<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
```

| 属性     | 值                       | 描述                                         |
| :------- | :----------------------- | :------------------------------------------- |
| cite     | *URL*                    | 规定一个解释了文本被删除的原因的文档的 URL。 |
| datetime | *YYYY-MM-DDThh:mm:ssTZD* | 规定文本被删除的日期和时间。                 |

### 44、`<details>`

`<details>` 标签规定了用户可见的或者隐藏的需求的补充细节。

`<details>` 标签用来供用户开启关闭的交互式控件。任何形式的内容都能被放在 `<details> `标签里边。

`<details> `元素的内容对用户是不可见的，除非设置了 open 属性。

```html
<details>
<summary>Copyright 1999-2011.</summary>
<p> - by Refsnes Data. All Rights Reserved.</p>
<p>All content and graphics on this web site are the property of the company Refsnes Data.</p>
</details>
```

| 属性 |                描述                 |
| :--: | :---------------------------------: |
| open | 添加后`<details>`标签内容对用户可见 |

### 45、`<dfn>`

`<dfn> `标签是一个短语标签，用来定义一个定义项目。

**提示：**我们并不反对使用这个标签，但是如果您只是为了达到某种视觉效果而使用这个标签的话，我们建议您使用 CSS ，这样可能会取得更丰富的效果。

| 标签     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| <em>     | 呈现为被强调的文本。                                         |
| <strong> | 定义重要的文本。                                             |
| <dfn>    | 定义一个定义项目。                                           |
| <code>   | 定义计算机代码文本。                                         |
| <samp>   | 定义样本文本。                                               |
| <kbd>    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| <var>    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

```html
<dfn>定义的内容</dfn>
```

### 46、`<dialog>`

`<dialog>` 标签定义一个对话框、确认框或窗口。

| 属性 |                       描述                       |
| :--: | :----------------------------------------------: |
| open | 添加后`<dialog>`是可用的，用户可以与它们进行交互 |

```html
<table border="1">
<tr>
  <th>January <dialog open>This is an open dialog window</dialog></th>
  <th>February</th>
  <th>March</th>
</tr>
<tr>
  <td>31</td>
  <td>28</td>
  <td>31</td>
</tr>
</table>
```

### 47、`<dir>`

**==H5不支持`<dir>`标签，请用CSS替代==**

该标签用来定义目录列表

| 属性    | 值      | 描述                                                         |
| :------ | :------ | :----------------------------------------------------------- |
| compact | compact | HTML5 不支持。HTML 4.01 已废弃。 规定列表必须比常规状态小一号呈现。 |



### 48、`<div>`

<div> 标签定义 HTML 文档中的一个分隔区块或者一个区域部分。
`<div>`标签常用于组合块级元素，以便通过 CSS 来对这些元素进行格式化。

| 属性  | 值                        | 描述                                                         |
| :---- | :------------------------ | :----------------------------------------------------------- |
| align | left right center justify | HTML5 不支持。HTML 4.01 已废弃。 规定 <div> 元素中的内容的对齐方式。 |

```html
<div style="color:#0000FF">
  <h3>这是一个在 div 元素中的标题。</h3>
  <p>这是一个在 div 元素中的文本。</p>
</div>
```

### 49、`<dl>`

`<dl> `标签定义一个描述列表。

`<dl>` 标签与 `<dt>`（定义项目/名字）和`<dd>`（描述每一个项目/名字）一起使用。

```html
<dl>
  <dt>Coffee</dt>
    <dd>Black hot drink</dd>
  <dt>Milk</dt>
    <dd>White cold drink</dd>
</dl>
```

### 50、`<dt>`

`<dt>` 标签与 `<dl>`（定义一个描述列表）和`<dd>`（描述每一个项目/名字）一起使用。

```html
<dl>
  <dt>Coffee</dt>
    <dd>Black hot drink</dd>
  <dt>Milk</dt>
    <dd>White cold drink</dd>
</dl>
```

### 51、`<em>`

`<em> `标签是一个短语标签，用来呈现为被强调的文本。

```html
<em>强调文本</em>
```

### 52、`<embed>`

`<embed> `标签定义了一个容器，用来嵌入外部应用或者互动程序（插件）。

| 属性         | 值          | 描述                                                         |
| :----------- | :---------- | :----------------------------------------------------------- |
| height:five: | *pixels*    | 规定嵌入内容的高度。                                         |
| src:five:    | *URL*       | 规定被嵌入内容的 URL。                                       |
| type:five:   | *MIME_type* | 规定嵌入内容的 MIME 类型。 注：MIME = Multipurpose Internet Mail Extensions。 |
| width:five:  | *pixels*    | 规定嵌入内容的宽度。                                         |

嵌入图片：

```html
<embed type="image/jpg" src="https://static.runoob.com/images/runoob-logo.png" width="258" height="39">
```



嵌入html页面：

```html
<embed type="text/html" src="snippet.html" width="500" height="200">
```



嵌入视频：

```html
<embed type="video/webm" src="video.mp4" width="400" height="300">
```

### 53、`<fieldset>`

`<fieldset> `标签可以将表单内的相关元素分组。

`<fieldset> `标签会在相关表单元素周围**绘制边框**。

| 属性            | 值        | 描述                                 |
| :-------------- | :-------- | :----------------------------------- |
| disabled :five: | disabled  | 规定该组中的相关表单元素应该被禁用。 |
| form:five:      | *form_id* | 规定 fieldset 所属的一个或多个表单。 |
| name:five:      | *text*    | 规定 fieldset 的名称。               |

```html
<form>
  <fieldset>
    <legend>Personalia:</legend>
    Name: <input type="text"><br>
    Email: <input type="text"><br>
    Date of birth: <input type="text">
  </fieldset>
</form>
```

### 54、`<figcaption>`

`<figcaption>`标签为`<figure>`元素定位标题

该元素应该被置于 `<figure>` 元素的第一个或最后一个子元素的位置。

```html
<figure>
  <img loading="lazy" src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
  <figcaption>Fig1. - A view of the pulpit rock in Norway.</figcaption>
</figure>
```

### 55、`<figure>`

`<figure>` 标签规定独立的流内容（图像、图表、照片、代码等等）。

`<figure> `元素的内容应该与主内容相关，同时元素的位置相对于主内容是独立的。如果被删除，则不应对文档流产生影响。

```html
<figure>
  <img loading="lazy" src="img_pulpit.jpg" alt="The Pulpit Rock" width="304" height="228">
</figure>
```



### 56、`<font>`

==**HTML5 不支持 `<font>` 标签。请用 CSS 代替。**==

在 HTML 4.01 中，`<font> 元素`

`<font>` 标签规定文本的字体、字体尺寸、字体颜色。

```html
<font size="3" color="red">这是一些文本!</font>
<font size="2" color="blue">这是一些文本!</font>
<font face="verdana" color="green">这是一些文本!</font>
```



### 57、`<footer>`

`<footer> `标签定义文档或者文档的一部分区域的页脚。

`<footer> `元素应该包含它所包含的元素的信息。

在典型情况下，该元素会包含文档创作者的姓名、文档的版权信息、使用条款的链接、联系信息等等。

在一个文档中，您可以定义多个` <footer>` 元素。

```html
<footer>
  <p>Posted by: Hege Refsnes</p>
  <p><time pubdate datetime="2012-03-01"></time></p>
</footer>
```

### 58、`<form>`

`<form> `标签用于创建供用户输入的 HTML 表单。

`<form>` 元素包含一个或多个如下的表单元素：

> `<input>`

> `<textarea>`

> `<button>`

> `<select>`

> `<option>`

> `<optgroup>`

> `<fieldset>`

> `<label>`

| 属性               | 值                                                           | 描述                                                         |
| :----------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| accept             | *MIME_type*                                                  | HTML5 不支持。规定服务器接收到的文件的类型。（文件是通过文件上传提交的） |
| accept-charset     | *character_set*                                              | 规定服务器可处理的表单数据字符集。                           |
| action             | *URL*                                                        | 规定当提交表单时向何处发送表单数据。                         |
| autocomplete:five: | on off                                                       | 规定是否启用表单的自动完成功能。                             |
| enctype            | application/x-www-form-urlencoded multipart/form-data text/plain | 规定在向服务器发送表单数据之前如何对其进行编码。（适用于 method="post" 的情况） |
| method             | get post                                                     | 规定用于发送表单数据的 HTTP 方法。                           |
| name               | *text*                                                       | 规定表单的名称。                                             |
| novalidate:five:   | novalidate                                                   | 如果使用该属性，则提交表单时不进行验证。                     |
| target             | _blank _self _parent _top                                    | 规定在何处打开 action URL。                                  |

```html
<form action="demo_form.php" method="get">
  First name: <input type="text" name="fname"><br>
  Last name: <input type="text" name="lname"><br>
  <input type="submit" value="提交">
</form>

```

### 59、`<frame>`

==**HTML5 不支持` <frame> `标签。**==

`<frame> `标签定义 `<frameset> `中的子窗口（框架）。

`<frameset>` 中的每个 `<frame> `都可以设置不同的属性，比如 `border、scrolling, noresize `等等。

| 属性         | 值          | 描述                                                   |
| :----------- | :---------- | :----------------------------------------------------- |
| frameborder  | 0 1         | HTML5 不支持。规定是否显示框架周围的边框。             |
| longdesc     | *URL*       | HTML5 不支持。规定一个包含有关框架内容的长描述的页面。 |
| marginheight | *pixels*    | HTML5 不支持。规定框架的上方和下方的边距。             |
| marginwidth  | *pixels*    | HTML5 不支持。规定框架的左侧和右侧的边距。             |
| name         | *name*      | HTML5 不支持。规定框架的名称。                         |
| noresize     | noresize    | HTML5 不支持。规定无法调整框架的大小。                 |
| scrolling    | yes no auto | HTML5 不支持。规定是否在框架中显示滚动条。             |
| src          | *URL*       | HTML5 不支持。规定在框架中显示的文档的 URL。           |

```html
<frameset cols="25%,50%,25%">
  <frame src="frame_a.htm">
  <frame src="frame_b.htm">
  <frame src="frame_c.htm">
</frameset>
```

### 60、`<frameset>`

==**HTML5 不支持 `<frameset>` 标签。**==



`<frameset> `标签定义一个框架集。

`<frameset> `元素被用来组织一个或者多个`<frame>` 元素。每个 <frame> 有各自独立的文档。

`<frameset> `元素规定在框架集中存在多少列或多少行，以及每行每列占用的百分比/像素。

```html
<frameset cols="25%,*,25%">
  <frame src="frame_a.htm">
  <frame src="frame_b.htm">
  <frame src="frame_c.htm">
</frameset>
```

### 61、`<header>`

`<header>` 标签定义文档或者文档的一部分区域的页眉。

`<header> `元素应该作为介绍内容或者导航链接栏的**容器**。

在一个文档中，您可以定义多个 `<header> `元素。

**注释：**`<header> `标签不能被放在 `<footer>`、`<address> `或者另一个` <header> `元素内部

### 62、`<i>`

`<i>` 定义与文本中其余部分不同的部分，并把这部分文本呈现为斜体文本。

`<i> `标签被用来表示科技术语、其他语种的成语俗语、想法、宇宙飞船的名字等等。

在没有其他适当语义的元素可以使用时，请使用` <i> `元素。其他语义的元素如下：

> `<em>`	强调文本
>
> `<strong>`	重要的文本
>
> `<mark>`	被标记/高亮显示的文本
>
> `<cite>`	作品的标题
>
> `<dfn> `	一个定义的项目

```html
<p>He named his car <i>The lightning</i>, because it was very fast.</p>
```

### 63、`<iframe>` 	

`<iframe>` 标签规定一个内联框架。

一个内联框架被用来在当前 HTML 文档中嵌入另一个文档。

| 属性           | 值                                                           | 描述                                                         |
| :------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| align          | left right top middle bottom                                 | HTML5 不支持。HTML 4.01 已废弃。 规定如何根据周围的元素来对齐 <iframe>。 |
| frameborder    | 1 0                                                          | HTML5 不支持。规定是否显示 <iframe> 周围的边框。             |
| height         | *pixels*                                                     | 规定 <iframe> 的高度。                                       |
| longdesc       | *URL*                                                        | HTML5 不支持。规定一个页面，该页面包含了有关 <iframe> 的较长描述。 |
| marginheight   | *pixels*                                                     | HTML5 不支持。规定 <iframe> 的顶部和底部的边距。             |
| marginwidth    | *pixels*                                                     | HTML5 不支持。规定 <iframe> 的左侧和右侧的边距。             |
| name           | *name*                                                       | 规定 <iframe> 的名称。                                       |
| sandbox:five:  | "" allow-forms allow-same-origin allow-scripts allow-top-navigation | 对 <iframe> 的内容定义一系列额外的限制。                     |
| scrolling      | yes no auto                                                  | HTML5 不支持。规定是否在 <iframe> 中显示滚动条。             |
| seamless:five: | seamless                                                     | 规定 <iframe> 看起来像是父文档中的一部分。                   |
| src            | *URL*                                                        | 规定在 <iframe> 中显示的文档的 URL。                         |
| srcdoc:five:   | *HTML_code*                                                  | 规定页面中的 HTML 内容显示在 <iframe> 中。                   |
| width          | *pixels*                                                     | 规定 <iframe> 的宽度。                                       |

```html
<iframe src="http://www.runoob.com"></iframe>
```

### 64、`<input>`

`<input>` 标签规定了用户可以在其中输入数据的输入字段。

`<input>` 元素在` <form>` 元素中使用，用来声明允许用户输入数据的 input 控件。

输入字段可通过多种方式改变，取决于 type 属性。

| 属性           | 值                                                           | 描述                                                         |
| :------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| accept         | audio/* video/* image/* *MIME_type*                          | 规定通过文件上传来提交的文件的类型。 (只针对type="file")     |
| align          | left right top middle bottom                                 | HTML5已废弃，不赞成使用。规定图像输入的对齐方式。 (只针对type="image") |
| alt            | *text*                                                       | 定义图像输入的替代文本。 (只针对type="image")                |
| autocomplete   | on off                                                       | autocomplete 属性规定 `<input> `元素输入字段是否应该启用自动完成功能。 |
| autofocus      | autofocus                                                    | 属性规定当页面加载时 `<input> `元素应该自动获得焦点。        |
| checked        | checked                                                      | checked 属性规定在页面加载时应该被预先选定的` <input> `元素。 (只针对 type="checkbox" 或者 type="radio") |
| disabled       | disabled                                                     | disabled 属性规定应该禁用的 `<input> `元素。                 |
| form           | *form_id*                                                    | form 属性规定 `<input> `元素所属的一个或多个表单。           |
| formaction     | *URL*                                                        | 属性规定当表单提交时处理输入控件的文件的 URL。(只针对 type="submit" 和 type="image") |
| formenctype    | application/x-www-form-urlencoded multipart/form-data text/plain | 属性规定当表单数据提交到服务器时如何编码(只适合 type="submit" 和 type="image")。 |
| formmethod     | get post                                                     | 定义发送表单数据到 action URL 的 HTTP 方法。 (只适合 type="submit" 和 type="image") |
| formnovalidate | formnovalidate                                               | formnovalidate 属性覆盖` <form> `元素的 novalidate 属性。    |
| formtarget     | _blank _self _parent _top *framename*                        | 规定表示提交表单后在哪里显示接收到响应的名称或关键词。(只适合 type="submit" 和 type="image") |
| height         |                                                              | 规定 `<input>`元素的高度。(只针对type="image")               |
| list           | *datalist_id*                                                | 属性引用 `<datalist> `元素，其中包含 `<input>` 元素的预定义选项。 |
| max            | *number date*                                                | 属性规定` <input> `元素的最大值。                            |
| maxlength      | *number*                                                     | 属性规定` <input> `元素中允许的最大字符数。                  |
| min            | *number date*                                                | 属性规定 `<input>`元素的最小值。                             |
| multiple       | multiple                                                     | 属性规定允许用户输入到 `<input> `元素的多个值。              |
| name           | *text*                                                       | name 属性规定 `<input>` 元素的名称。                         |
| pattern        | *regexp*                                                     | pattern 属性规定用于验证 `<input> `元素的值的正则表达式。    |
| placeholder    | *text*                                                       | placeholder 属性规定可描述输入 `<input>` 字段预期值的简短的提示信息 。 |
| readonly       | readonly                                                     | readonly 属性规定输入字段是只读的。                          |
| required       | required                                                     | 属性规定必需在提交表单之前填写输入字段。                     |
| size           | *number*                                                     | size 属性规定以字符数计的 `<input> `元素的可见宽度。         |
| src            | *URL*                                                        | src 属性规定显示为提交按钮的图像的 URL。 (只针对 type="image") |
| step           | *number*                                                     | step 属性规定 `<input> `元素的合法数字间隔。                 |
| type           | button checkbox color date datetime datetime-local email file hidden image month number password radio range reset search submit tel text time url week | type 属性规定要显示的 `<input> `元素的类型。                 |
| value          | *text*                                                       | 指定 `<input> `元素 value 的值。                             |
| width          | *pixels*                                                     | width 属性规定 `<input> `元素的宽度。 (只针对type="image")   |

```html
<form action="demo_form.asp">
  First name: <input type="text" name="fname"><br>
  Last name: <input type="text" name="lname"><br>
  <input type="submit" value="提交">
</form>
```



### 65、`<link>`

`<link> `标签定义文档与外部资源的关系。

`<link> `标签最常见的用途是链接样式表。

| 属性        | 值                                                           | 描述                                                      |
| :---------- | :----------------------------------------------------------- | :-------------------------------------------------------- |
| charset     | *char_encoding*                                              | HTML5 不支持该属性。 定义被链接文档的字符编码方式。       |
| href        | *URL*                                                        | 定义被链接文档的位置。                                    |
| hreflang    | *language_code*                                              | 定义被链接文档中文本的语言。                              |
| media       | *media_query*                                                | 规定被链接文档将显示在什么设备上。                        |
| rel         | alternate archives author bookmark external first help icon last license next nofollow noreferrer pingback prefetch prev search sidebar stylesheet tag up | 必需。定义当前文档与被链接文档之间的关系。                |
| rev         | *reversed relationship*                                      | HTML5 不支持该属性。 定义被链接文档与当前文档之间的关系。 |
| sizes:five: | *Height*x*Width *any                                         | 定义了链接属性大小，只对属性 rel="icon" 起作用。          |
| target      | _blank _self _top _parent *frame_name*                       | HTML5 不支持该属性。 定义在何处加载被链接文档。           |
| type        | *MIME_type*                                                  | 规定被链接文档的 MIME 类型。                              |

```html
<head>
<link rel="stylesheet" type="text/css" href="theme.css">
</head>
```



### 66、`<ins>`

`<ins>` 标签定义已经被插入文档中的文本。

| 属性     | 值                       | 描述                                               |
| :------- | :----------------------- | :------------------------------------------------- |
| cite     | *URL*                    | 规定一个文档的 URL，该文档解释了文本被插入的原因。 |
| datetime | *YYYY-MM-DDThh:mm:ssTZD* | 规定文本被插入的日期和时间。                       |

```html
<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
```



### 67、`<kbd>`

`<kbd> `标签定义键盘文本。

会显示一个按钮边框

| 标签     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| <em>     | 呈现为被强调的文本。                                         |
| <strong> | 定义重要的文本。                                             |
| <dfn>    | 定义一个定义项目。                                           |
| <code>   | 定义计算机代码文本。                                         |
| <samp>   | 定义样本文本。                                               |
| <kbd>    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| <var>    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

```html
<kbd>键盘输入</kbd>
```

### 68、`<keygen>`

`<keygen>` 标签规定用于表单的密钥对生成器字段。

当提交表单时，私钥存储在本地，公钥发送到服务器。

| 属性            | 值         | 描述                                                         |
| :-------------- | :--------- | :----------------------------------------------------------- |
| autofocus:five: | autofocus  | 使 `<keygen> `字段在页面加载时获得焦点。                     |
| challenge:five: | challenge  | 如果使用，则将 keygen 的值设置为在提交时询问。               |
| disabled:five:  | disabled   | 禁用 `<keygen> `元素字段。                                   |
| form:five:      | *form_id*  | 定义该 `<keygen>` 字段所属的一个或多个表单。                 |
| keytype:five:   | rsa dsa ec | 定义密钥的安全算法。                                         |
| name:five:      | *name*     | 定义 `<keygen>` 元素的唯一名称。 name 属性用于在提交表单时搜集字段的值。 |

```html
<form action="demo_keygen.asp" method="get">
  用户名: <input type="text" name="usr_name">
  加密: <keygen name="security">
  <input type="submit">
</form>
```



### 69、`<label>`

`<label> `标签为 input 元素定义标注（标记）。

label 元素不会向用户呈现任何特殊效果。不过，它为鼠标用户改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。

`<label> `标签的 for 属性应当与相关元素的 id 属性相同。

| 属性       | 值           | 描述                                  |
| :--------- | :----------- | :------------------------------------ |
| for        | *element_id* | 规定 label 与哪个表单元素绑定。       |
| form:five: | *form_id*    | 规定 label 字段所属的一个或多个表单。 |

```html
<form action="demo_form.php">
  <label for="male">Male</label>
  <input type="radio" name="sex" id="male" value="male"><br>
  <label for="female">Female</label>
  <input type="radio" name="sex" id="female" value="female"><br><br>
  <input type="submit" value="提交">
</form>
```

### 70、`<legend>`

 `<legend>`元素为`<fieldset>`元素定义标题

| 属性  | 值                    | 描述                                                         |
| :---- | :-------------------- | :----------------------------------------------------------- |
| align | top bottom left right | HTML5 不支持。 HTML 4.01 已废弃。不建议使用。 请使用样式代替。 为 fieldset 中的标题定义对齐方式。 |

```html
<form>
 <fieldset>
  <legend>Personalia:</legend>
  Name: <input type="text" size="30"><br>
  Email: <input type="text" size="30"><br>
  Date of birth: <input type="text" size="10">
 </fieldset>
</form>
```

### 71、`<hgroup>`

`<hgroup> `标签被用来对标题元素进行分组。

当标题有多个层级（副标题）时，`<hgroup> `元素被用来对一系列`<h>`元素进行分组。

```html
<hgroup>
<h1>Welcome to my WWF</h1>
<h2>For a living planet</h2>
</hgroup>

<p>The rest of the content...</p>
```



### 72、`<main>`

`<main> `标签用于指定文档的主体内容。

`<main> `标签中的内容在文档中是唯一的。它不应包含在文档中重复出现的内容，比如侧栏、导航栏、版权信息、站点标志或搜索表单。

注意在一个文档中，`<main> `元素是唯一的，所以不能出现一个以上的` <main> `元素。`<main> `元素不能是以下元素的后代：`<article>`、`<aside>`、`<footer>`、`<header>` 或` <nav>`。

```html
<main>
  <h1>Web 浏览器</h1>
  <p>Google Chrome、Firefox 以及 Internet Explorer 是目前最流行的浏览器。</p>
 
  <article>
    <h1>Google Chrome 浏览器</h1>
    <p>Google Chrome 浏览器是由 Google 开发的一款免费的开源 web 浏览器，于 2008 年发布。</p>
  </article>
 
  <article>
    <h1>Internet Explorer 浏览器</h1>
    <p>Internet Explorer 浏览器由微软开发的一款免费的 web 浏览器，发布于 1995 年。</p>
  </article>
 
  <article>
    <h1>Mozilla Firefox 浏览器</h1>
    <p>Firefox 浏览器是一款来自 Mozilla 的免费开源 web 浏览器，发布于 2004 年。</p>
  </article>
</main>
```



### 73、`<map>`

`<map>` 标签用于客户端图像映射。图像映射指带有可点击区域的一幅图像。

`<img>`中的 usemap 属性可引用 `<map> `中的 id 或 name 属性（取决于浏览器），所以我们应同时向 `<map> `添加 id 和 name 属性。

area 元素永远嵌套在 map 元素内部。area 元素可定义图像映射中的区域。

| 属性 | 值        | 描述                            |
| :--- | :-------- | :------------------------------ |
| name | *mapname* | 必需。为 image-map 规定的名称。 |

```html
<img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">

<map name="planetmap">
  <area shape="rect" coords="0,0,82,126" href="sun.htm" alt="Sun">
  <area shape="circle" coords="90,58,3" href="mercur.htm" alt="Mercury">
  <area shape="circle" coords="124,58,8" href="venus.htm" alt="Venus">
</map>
```

### 74、`<mark>`

`<mark>` 标签定义带有记号的文本。

请在需要突出显示文本时使用` <mark>` 标签。

```html
<p>Do not forget to buy <mark>milk</mark> today.</p>
```

### 75、`<menu>`

==**目前浏览器不支持<menu>标签**==

`<menu> `标签定义了一个命令列表或菜单。

`<menu> `标签通常用于文本菜单，工具条和命令列表选项。

| 属性        | 值                   | 描述                              |
| :---------- | :------------------- | :-------------------------------- |
| label:five: | *text*               | 描述菜单项的标记。                |
| type:five:  | context toolbar list | 描述显示菜单类型. 默认为 "list"。 |

```html
<menu type="toolbar">
<li>
    <menu label="File">
    <button type="button" onclick="file_new()">New...</button>
    <button type="button" onclick="file_open()">Open...</button>
    <button type="button" onclick="file_save()">Save</button>
    </menu>
</li>
<li>
    <menu label="Edit">
    <button type="button" onclick="edit_cut()">Cut</button>
    <button type="button" onclick="edit_copy()">Copy</button>
    <button type="button" onclick="edit_paste()">Paste</button>
    </menu>
</li>
</menu>
```

### 76、`<menuitem>`

`<menuitem> `标签定义用户可以从弹出菜单调用的命令/菜单项目。

| 属性       | 值                   | 描述                                                         |
| :--------- | :------------------- | :----------------------------------------------------------- |
| checked    | checked              | 规定在页面加载后选中命令/菜单项目。仅适用于 type="radio" 或 type="checkbox"。 |
| default    | default              | 把命令/菜单项设置为默认命令。                                |
| disabled   | disabled             | 规定命令/菜单项应该被禁用。                                  |
| icon       | URL                  | 规定命令/菜单项的图标。                                      |
| open       | open                 | 定义 details 是否可见。                                      |
| label      | *text*               | 必需。规定命令/菜单项的名称，以向用户显示。                  |
| radiogroup | *groupname*          | 规定命令组的名称，命令组会在命令/菜单项本身被切换时进行切换。仅适用于 type="radio"。 |
| type       | checkboxcommandradio | 规定命令/菜单项的类型。默认是 "command"。                    |

```html
<menu type="context" id="mymenu">
  <menuitem label="Refresh" onclick="window.location.reload();" icon="ico_reload.png">
  </menuitem>
  <menu label="Share on...">
    <menuitem label="Twitter" icon="ico_twitter.png"
    onclick="window.open('//twitter.com/intent/tweet?text='+window.location.href);">
    </menuitem>
    <menuitem label="Facebook" icon="ico_facebook.png"
    onclick="window.open('//facebook.com/sharer/sharer.php?u='+window.location.href);">
    </menuitem>
  </menu>
  <menuitem label="Email This Page"
  onclick="window.location='mailto:?body='+window.location.href;"></menuitem>
</menu>
```



### 77、`<meta>`

Meta 对象代表 HTML 的 一个 `<meta>` 元素。

`<meta>` 元素可提供有关某个 HTML 元素的元信息 (meta-information)，比如描述、针对搜索引擎的关键词以及刷新频率。

| 属性      | 描述                                          | W3C  |
| :-------- | :-------------------------------------------- | :--- |
| content   | 设置或返回 `<meta> `元素的 content 属性的值。 | Yes  |
| httpEquiv | 把 content 属性连接到一个 HTTP 头部。         | Yes  |
| name      | 把 content 属性连接到某个名称。               | Yes  |
| scheme    | 设置或返回用于解释 content 属性的值的格式。   | Yes  |

```html
<meta>
```

### 78、`<meter>`

`<meter> `标签定义已知范围或分数值内的标量测量。也被称为 gauge（尺度）。

例子：磁盘用量、查询结果的相关性，等等。

**注释：**`<meter> `标签不应用于指示进度（在进度条中）。如果标记进度条，请使用 <progress> 标签。

| 属性    | 值        | 描述                                    |
| :------ | :-------- | :-------------------------------------- |
| form    | *form_id* | 规定 <meter> 元素所属的一个或多个表单。 |
| high    | *number*  | 规定被视作高的值的范围。                |
| low     | *number*  | 规定被视作低的值的范围。                |
| max     | *number*  | 规定范围的最大值。                      |
| min     | *number*  | 规定范围的最小值。                      |
| optimum | *number*  | 规定度量的优化值。                      |
| value   | *number*  | 必需。规定度量的当前值。                |

```html
<meter value="3" min="0" max="10">十分之三</meter>

<meter value="0.6">60%</meter> 
```



### 79、`<nav>`

`<nav> `标签定义导航链接的部分。

```html
<nav>
<a href="index.asp">Home</a>
<a href="html5_meter.asp">Previous</a>
<a href="html5_noscript.asp">Next</a>
</nav>
```



### 80、`<noframes>`

noframes 元素可为那些不支持框架的浏览器显示文本。noframes 元素位于 frameset 元素内部。

```html
<frameset cols = "25%, 25%,*">
  <noframes>
  <body>Your browser does not handle frames!</body>
  </noframes>
  <frame src ="venus.htm" />
  <frame src   ="sun.htm" />
  <frame src ="mercur.htm"   />
</frameset>
```

### 81、`<noscript>`

noscript 元素用来定义在脚本未被执行时的替代内容（文本）。

此标签可被用于可识别` <script> `标签但无法支持其中的脚本的浏览器。

### 82、`<object>`

定义一个嵌入的对象。请使用此元素向您的 XHTML 页面添加多媒体。此元素允许您规定插入 HTML 文档中的对象的数据和参数，以及可用来显示和操作数据的代码。

`<object> `标签用于包含对象，比如图像、音频、视频、Java applets、ActiveX、PDF 以及 Flash。

object 的初衷是取代 img 和 applet 元素。不过由于漏洞以及缺乏浏览器支持，这一点并未实现。

浏览器的对象支持有赖于对象类型。不幸的是，主流浏览器都使用不同的代码来加载相同的对象类型。

而幸运的是，object 对象提供了解决方案。如果未显示 object 元素，就会执行位于` <object>` 和 `</object> `之间的代码。通过这种方式，我们能够嵌套多个 object 元素（每个对应一个浏览器）。

```html
<object classid="clsid:F08DF954-8592-11D1-B16A-00C0F0283628" id="Slider1" 
width="100" height="50">
  <param name="BorderStyle" value="1" />
  <param name="MousePointer" value="0" />
  <param name="Enabled" value="1" />
  <param name="Min" value="0" />
  <param name="Max" value="10" />
</object>
```

| 属性       | 值                 | 描述                                                         |
| :--------- | :----------------- | :----------------------------------------------------------- |
| align      | leftrighttopbottom | 定义围绕该对象的文本对齐方式。                               |
| archive    | *URL*              | 由空格分隔的指向档案文件的 URL 列表。这些档案文件包含了与对象相关的资源。 |
| border     | *pixels*           | 定义对象周围的边框。                                         |
| classid    | *class ID*         | 定义嵌入 Windows Registry 中或某个 URL 中的类的 ID 值，此属性可用来指定浏览器中包含的对象的位置，通常是一个 Java 类。 |
| codebase   | *URL*              | 定义在何处可找到对象所需的代码，提供一个基准 URL。           |
| codetype   | *MIME type*        | 通过 classid 属性所引用的代码的 MIME 类型。                  |
| data       | *URL*              | 定义引用对象数据的 URL。如果有需要对象处理的数据文件,要用 data 属性来指定这些数据文件。 |
| declare    | declare            | 可定义此对象仅可被声明，但不能被创建或例示，直到此对象得到应用为止。 |
| form:five: | *form_id*          | 规定对象所属的一个或多个表单。                               |
| height     | *pixels*           | 定义对象的高度。                                             |
| hspace     | *pixels*           | 定义对象周围水平方向的空白。                                 |
| name       | *unique_name*      | 为对象定义唯一的名称（以便在脚本中使用）。                   |
| standby    | *text*             | 定义当对象正在加载时所显示的文本。                           |
| type       | *MIME_type*        | 定义被规定在 data 属性中指定的文件中出现的数据的 MIME 类型。 |
| usemap     | *URL*              | 规定与对象一同使用的客户端图像映射的 URL。                   |
| vspace     | *pixels*           | 定义对象的垂直方向的空白。                                   |
| width      | *pixels*           | 定义对象的宽度。                                             |

### 83、`<optgroup>`

`<optgroup>` 标签定义选项组。

optgroup 元素用于组合选项。当您使用一个长的选项列表时，对相关的选项进行组合会使处理更加容易。

```html
<select>
  <optgroup label="Swedish Cars">
    <option value ="volvo">Volvo</option>
    <option value ="saab">Saab</option>
  </optgroup>

  <optgroup label="German Cars">
    <option value ="mercedes">Mercedes</option>
    <option value ="audi">Audi</option>
  </optgroup>
</select>
```

| 属性     | 值       | 描述               |
| :------- | :------- | :----------------- |
| label    | *text*   | 为选项组规定描述。 |
| diasbled | diasbled | 规定禁用该选项组   |

### 84、`<option>`

option 元素定义下拉列表中的一个选项（一个条目）。

浏览器将·`<option> `标签中的内容作为·`<select> `标签的菜单或是滚动列表中的一个元素显示。

option 元素位于 select 元素内部。

```html
<select>
  <option value ="volvo">Volvo</option>
  <option value ="saab">Saab</option>
  <option value="opel">Opel</option>
  <option value="audi">Audi</option>
</select>
```

| 属性     | 值       | 描述                                             |
| :------- | :------- | :----------------------------------------------- |
| disabled | disabled | 规定此选项应在首次加载时被禁用。                 |
| label    | *text*   | 定义当使用 <optgroup> 时所使用的标注。           |
| selected | selected | 规定选项（在首次显示在列表中时）表现为选中状态。 |
| value    | *text*   | 定义送往服务器的选项值。                         |

### 85、`<output>`

`<output> `标签定义不同类型的输出，比如脚本的输出。

| 属性       | 值           | 描述                                   |
| :--------- | :----------- | :------------------------------------- |
| for:five:  | *element_id* | 定义输出域相关的一个或多个元素。       |
| form:five: | *form_id*    | 定义输入字段所属的一个或多个表单。     |
| name:five: | *name*       | 定义对象的唯一名称。（表单提交时使用） |

```html
<form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0
   <input type="range" id="a" value="50">100
   +<input type="number" id="b" value="50">
   =<output name="x" for="a b"></output>
</form>  
```

### 86、`<param>`

param 元素允许您为插入 XHTML 文档的对象规定 run-time 设置，也就是说，此标签可为包含它的 `<object>` 或者`<applet>`提供参数。

```html
<object classid="clsid:F08DF954-8592-11D1-B16A-00C0F0283628" id="Slider1" 
width="100" height="50">
  <param name="BorderStyle" value="1" />
  <param name="MousePointer" value="0" />
  <param name="Enabled" value="1" />
  <param name="Min" value="0" />
  <param name="Max" value="10" />
</object>
```

| 属性      | 值            | 描述                                          |
| :-------- | :------------ | :-------------------------------------------- |
| type      | *MIME type*   | 规定参数的 MIME 类型（internet media type）。 |
| value     | *value*       | 规定参数的值。                                |
| valuetype | datarefobject | 规定值的 MIME 类型。                          |
| name      | unique_name   | 定义参数的名字                                |

### 87、`<pre>`

pre 元素可定义预格式化的文本。被包围在 pre 元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体。

`<pre>` 标签的一个常见应用就是用来表示计算机的源代码。

| 属性  | 值     | 描述                                           |
| ----- | ------ | ---------------------------------------------- |
| width | number | 定义每行的最大字符数（通常是 40、80 或 132）。 |

### 88、`<progress>`

`<progress> `标签标示任务的进度（进程）。

**提示：**请结合 `<progress> `标签与 JavaScript 一同使用，来显示任务的进度。

**注释:**`<progress> `标签不适合用来表示度量衡（例如，磁盘空间使用情况或查询结果）。如需表示度量衡，请使用 <meter> 标签代替。

```html
<progress value="22" max="100"></progress> 
```

| 属性  | 值       | 描述                       |
| :---- | :------- | :------------------------- |
| max   | *number* | 规定任务一共需要多少工作。 |
| value | *number* | 规定已经完成多少任务。     |

### 89、`<q>`

`<q> `标签定义短的引用。

浏览器经常在引用的内容周围添加引号。

**`<q> `与` <blockquote> `的区别**

`<q> `标签在本质上与`<blockquote>`是一样的。不同之处在于它们的显示和应用。`<q> `标签用于简短的行内引用。如果需要从周围内容分离出来比较长的部分（通常显示为缩进的块），请使用 `<blockquote>` 标签。

```html
<q>Here is a short quotation here is a short quotation</q>
```

| 属性 | 值       | 描述                             |
| :--- | :------- | :------------------------------- |
| cite | citation | 定义引用的出处或来源（citation） |

### 90、`<wbr>`

Word Break Opportunity (`<wbr>`) 规定在文本中的何处适合添加换行符。

**提示：**如果单词太长，或者您担心浏览器会在错误的位置换行，那么您可以使用` <wbr>` 元素来添加 Word Break Opportunity（单词换行时机）。

```html
<p>
如果想学习 AJAX，那么您必须熟悉 XML<wbr>Http<wbr>Request 对象。
</p>
```

### 91、`<rp>`

`<rp> `标签在 ruby 注释中使用，以定义不支持 ruby 元素的浏览器所显示的内容。

ruby 注释是中文注音或字符。

在东亚使用，显示的是东亚字符的发音。

与 `<ruby>` 以及 `<rt> `标签一同使用：

ruby 元素由一个或多个字符（需要一个解释/发音）和一个提供该信息的 rt 元素组成，还包括可选的 rp 元素，定义当浏览器不支持 "ruby" 元素时显示的内容。

```html
<ruby>
漢 <rt><rp>(</rp>ㄏㄢˋ<rp>)</rp></rt>
</ruby>
```

### 92、`<rt>`

`<rt> `标签定义字符（中文注音或字符）的解释或发音。

ruby 注释是中文注音或字符。

在东亚使用，显示的是东亚字符的发音。

与` <ruby> `以及 `<rt>` 标签一同使用：

ruby 元素由一个或多个字符（需要一个解释/发音）和一个提供该信息的 rt 元素组成，还包括可选的 rp 元素，定义当浏览器不支持 "ruby" 元素时显示的内容。

```html
<ruby>
漢 <rt> ㄏㄢˋ </rt>
</ruby>
```

### 93、`<ruby>`

`<ruby>` 标签定义 ruby 注释（中文注音或字符）。

在东亚使用，显示的是东亚字符的发音。

与 `<ruby> `以及` <rt> `标签一同使用：

ruby 元素由一个或多个字符（需要一个解释/发音）和一个提供该信息的 rt 元素组成，还包括可选的 rp 元素，定义当浏览器不支持 "ruby" 元素时显示的内容。

```html
<ruby>
漢 <rt><rp>(</rp>ㄏㄢˋ<rp>)</rp></rt>
</ruby>
```

### 94、`<s>`

`<s> `标签可定义加删除线文本定义。

但在 HTML 4 和 XHTML 中已经不再赞成使用它了，意思就是不再使用了；==**它早晚有一天将会消失**==。

```html
在 HTML 5 中，<s>仍然支持</s>已经不支持这个标签了。
```

### 95、`<samp>`

| 标签     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| <em>     | 呈现为被强调的文本。                                         |
| <strong> | 定义重要的文本。                                             |
| <dfn>    | 定义一个定义项目。                                           |
| <code>   | 定义计算机代码文本。                                         |
| <samp>   | 定义样本文本。                                               |
| <kbd>    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| <var>    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

```html
<samp>
    
</samp>
```

### 96、`<script>`

`<script>` 标签用于定义客户端脚本，比如 JavaScript。


script 元素既可以包含脚本语句，也可以通过 src 属性指向外部脚本文件。

必需的 type 属性规定脚本的 MIME 类型。

JavaScript 的常见应用时图像操作、表单验证以及动态内容更新。

```html
<script type="text/javascript">
document.write("Hello World!")
</script>
```

### 97、`<section>`

`<section> `标签定义文档中的节（section、区段）。比如章节、页眉、页脚或文档中的其他部分。

| 属性       | 值    | 描述                                         |
| :--------- | :---- | :------------------------------------------- |
| cite:five: | *URL* | section 的 URL，假如 section 摘自 web 的话。 |

```html
<section>
  <h1>PRC</h1>
  <p>The People's Republic of China was born in 1949...</p>
</section>
```

### 98、`<select>`

select 元素可创建单选或多选菜单。

`<select&>` 元素中的`<option>`标签用于定义列表中的可用选项。

| 属性      | 值        | 描述                                   |
| :-------- | :-------- | :------------------------------------- |
| autofocus | autofocus | 规定在页面加载后文本区域自动获得焦点。 |
| disabled  | disabled  | 规定禁用该下拉列表。                   |
| form      | *form_id* | 规定文本区域所属的一个或多个表单。     |
| multiple  | multiple  | 规定可选择多个选项。                   |
| name      | *name*    | 规定下拉列表的名称。                   |
| required  | required  | 规定文本区域是必填的。                 |
| size      | *number*  | 规定下拉列表中可见选项的数目。         |

```html
<select>
  <option value ="volvo">Volvo</option>
  <option value ="saab">Saab</option>
  <option value="opel">Opel</option>
  <option value="audi">Audi</option>
</select>
```

### 99、`<small>`

`<small> `标签呈现小号字体效果。

`<small> `标签和它所对应的 `<big> `标签一样，但它是缩小字体而不是放大。如果被包围的字体已经是字体模型所支持的最小字号，那么 `<small> `标签将不起任何作用。

与 `<big> `标签类似，`<small>` 标签也可以嵌套，从而连续地把文字缩小。每个 `<small> `标签都把文本的字体变小一号，直到达到下限的一号字。

### 100、`<source>`

`<source>` 标签为媒介元素（比如` <video>` 和` <audio>`）定义媒介资源。

`<source>` 标签允许您规定可替换的视频/音频文件供浏览器根据它对媒体类型或者编解码器的支持进行选择。

| 属性  | 值              | 描述                       |
| :---- | :-------------- | :------------------------- |
| media | *media query*   | 规定媒体资源的类型。       |
| src   | *url*           | 规定媒体文件的 URL。       |
| type  | *numeric value* | 规定媒体资源的 MIME 类型。 |

```html
<audio controls>
   <source src="horse.ogg" type="audio/ogg">
   <source src="horse.mp3" type="audio/mpeg">
 Your browser does not support the audio element.
</audio> 
```



### 101、`<span>`

`<span>` 标签被用来组合文档中的行内元素。

```html
<p><span>some text.</span>some other text.</p>
```

### 102、`<strike>`

`<strike>` 标签可定义加删除线文本定义。

**注释：**请使用 <del> 替代它！

### 103、`<strong>`

| 标签     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| <em>     | 呈现为被强调的文本。                                         |
| <strong> | 定义重要的文本。                                             |
| <dfn>    | 定义一个定义项目。                                           |
| <code>   | 定义计算机代码文本。                                         |
| <samp>   | 定义样本文本。                                               |
| <kbd>    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| <var>    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

### 104、`<sub>`

`<sub>` 标签可定义下标文本。

包含在 `<sub> `标签和其结束标签 `</sub>` 中的内容将会以当前文本流中字符高度的一半来显示，但是与当前文本流中文字的字体和字号都是一样的。

**提示：**无论是 `<sub> `标签还是和它对应的`<sup>`，在数学等式、科学符号和化学公式中都非常有用。

```html
这段文本包含 <sub>下标</sub>
```



### 105、`<summary>`

`<summary>` 标签包含 details 元素的标题，"details" 元素用于描述有关文档或文档片段的详细信息。

```html
<details>
<summary>HTML 5</summary>
This document teaches you everything you have to learn about HTML 5.
</details>
```

### 106、`<sup>`

`<sup> `标签可定义上标文本。

包含在 `<sup>` 标签和其结束标签 `</sup>` 中的内容将会以当前文本流中字符高度的一半来显示，但是与当前文本流中文字的字体和字号都是一样的。

**提示：**这个标签在向文档添加脚注以及表示方程式中的指数值时非常有用。如果和 `<a>` 标签结合起来使用，就可以创建出很好的超链接脚注。

```html
这段文本包含 <sup>上标</sup>
```

### 107、`<table>`

`<table>` 标签定义 HTML 表格。


简单的 HTML 表格由 table 元素以及一个或多个 tr、th 或 td 元素组成。

tr 元素定义表格行，th 元素定义表头，td 元素定义表格单元。

更复杂的 HTML 表格也可能包括 caption、col、colgroup、thead、tfoot 以及 tbody 元素.

| 属性        | 值                                        | 描述                                                         |
| :---------- | :---------------------------------------- | :----------------------------------------------------------- |
| align       | leftcenterright                           | 不赞成使用。请使用样式代替。规定表格相对周围元素的对齐方式。 |
| bgcolor     | *rgb(x,x,x)**#xxxxxx**colorname*          | 不赞成使用。请使用样式代替。规定表格的背景颜色。             |
| border      | *pixels*                                  | 规定表格边框的宽度。                                         |
| cellpadding | *pixels**%*                               | 规定单元边沿与其内容之间的空白。                             |
| cellspacing | *pixels**%*                               | 规定单元格之间的空白。                                       |
| frame       | voidabovebelowhsideslhsrhsvsidesboxborder | 规定外侧边框的哪个部分是可见的。                             |
| rules       | nonegroupsrowscolsall                     | 规定内侧边框的哪个部分是可见的。                             |
| summary     | *text*                                    | 规定表格的摘要。                                             |
| width       | *%**pixels*                               | 规定表格的宽度。                                             |

```html
<table border="1">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### 108、`<tbody>`

`<tbody> `标签表格主体（正文）。该标签用于组合 HTML 表格的主体内容。

与`<thead>`和`<tfoot>`结合使用

thead 元素用于对 HTML 表格中的表头内容进行分组，而 tfoot 元素用于对 HTML 表格中的表注（页脚）内容进行分组。

**注释：**如果您使用 thead、tfoot 以及 tbody 元素，您就必须使用全部的元素。它们的出现次序是：thead、tfoot、tbody，这样浏览器就可以在收到所有数据前呈现页脚了。您必须在 table 元素内部使用这些标签。

**提示：**在默认情况下这些元素不会影响到表格的布局。不过，您可以使用 CSS 使这些元素改变表格的外观。

**详细描述**

thead、tfoot 以及 tbody 元素使您有能力对表格中的行进行分组。当您创建某个表格时，您也许希望拥有一个标题行，一些带有数据的行，以及位于底部的一个总计行。这种划分使浏览器有能力支持独立于表格标题和页脚的表格正文滚动。当长的表格被打印时，表格的表头和页脚可被打印在包含表格数据的每张页面上。

```html
<table border="1">
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>

  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>

  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
</table>
```



### 109、`<td>`

`<td>` 标签定义 HTML 表格中的标准单元格。

HTML 表格有两类单元格：

- 表头单元 - 包含头部信息（由 th 元素创建）
- 标准单元 - 包含数据（由 td 元素创建）

td 元素中的文本一般显示为正常字体且左对齐。

````html
<table border="1">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
````

| 属性    | 值                               | 描述                                                         |
| :------ | :------------------------------- | :----------------------------------------------------------- |
| abbr    | *text*                           | 规定单元格中内容的缩写版本。                                 |
| align   | leftrightcenterjustifychar       | 规定单元格内容的水平对齐方式。                               |
| axis    | *category_name*                  | 对单元进行分类。                                             |
| bgcolor | *rgb(x,x,x)**#xxxxxx**colorname* | 不赞成使用。请使用样式取而代之。规定单元格的背景颜色。       |
| char    | *character*                      | 规定根据哪个字符来进行内容的对齐。                           |
| charoff | *number*                         | 规定对齐字符的偏移量。                                       |
| colspan | *number*                         | 规定单元格可横跨的列数。                                     |
| headers | *header_cells'_id*               | 规定与单元格相关的表头。                                     |
| height  | *pixels**%*                      | 不赞成使用。请使用样式取而代之。规定表格单元格的高度。       |
| nowrap  | nowrap                           | 不赞成使用。请使用样式取而代之。规定单元格中的内容是否折行。 |
| rowspan | *number*                         | 规定单元格可横跨的行数。                                     |
| scope   | colcolgrouprowrowgroup           | 定义将表头数据与单元数据相关联的方法。                       |
| valign  | topmiddlebottombaseline          | 规定单元格内容的垂直排列方式。                               |
| wideth  | *pixels**%*                      | 不赞成使用。请使用样式取而代之。规定表格单元格的宽度。       |

### 110、`<textarea>`

`<textarea> `标签定义多行的文本输入控件。

文本区中可容纳无限数量的文本，其中的文本的默认字体是等宽字体（通常是 Courier）。

可以通过 cols 和 rows 属性来规定 textarea 的尺寸，不过更好的办法是使用 CSS 的 height 和 width 属性。

**注释：**在文本输入区内的文本行间，用 "%OD%OA" （回车/换行）进行分隔。

```html

<textarea rows="3" cols="20">
在XXX，你可以找到你所需要的所有的网站建设教程。
</textarea>
```

| 属性        | 值                 | 描述                                               |
| :---------- | :----------------- | :------------------------------------------------- |
| autofocus   | autofocus          | 规定在页面加载后文本区域自动获得焦点。             |
| cols        | *number*           | 规定文本区内的可见宽度。                           |
| disabled    | disabled           | 规定禁用该文本区。                                 |
| form        | *form_id*          | 规定文本区域所属的一个或多个表单。                 |
| maxlength   | *number*           | 规定文本区域的最大字符数。                         |
| name        | *name_of_textarea* | 规定文本区的名称。                                 |
| placeholder | *text*             | 规定描述文本区域预期值的简短提示。                 |
| readonly    | readonly           | 规定文本区为只读。                                 |
| required    | required           | 规定文本区域是必填的。                             |
| rows        | *number*           | 规定文本区内的可见行数。                           |
| wrap        | hardsoft           | 规定当在表单中提交时，文本区域中的文本如何换行。。 |

### 111、`<tfoot>`

`<tfoot> `标签定义表格的页脚（脚注或表注）。该标签用于组合 HTML 表格中的表注内容

| 属性    | 值                         | 描述                                  |
| :------ | :------------------------- | :------------------------------------ |
| align   | rightleftcenterjustifychar | 定义 tfoot 元素中内容的对齐方式。     |
| char    | *character*                | 规定根据哪个字符来进行文本对齐。      |
| charoff | *number*                   | 规定第一个对齐字符的偏移量。          |
| valign  | topmiddlebottombaseline    | 规定 tfoot 元素中内容的垂直对齐方式。 |

```html
<table border="1">
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>

  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>

  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
</table>
```



### 112、`<th>`

定义表格内的表头单元格。

HTML 表单中有两种类型的单元格：

- 表头单元格 - 包含表头信息（由 th 元素创建）
- 标准单元格 - 包含数据（由 td 元素创建）

th 元素内部的文本通常会呈现为居中的粗体文本，而 td 元素内的文本通常是左对齐的普通文本。

```html
<table border="1">
  <tr>
    <th>Company</th>
    <th>Address</th>
  </tr>

  <tr>
    <td>Apple, Inc.</td>
    <td>1 Infinite Loop Cupertino, CA 95014</td>
  </tr>
</table>
```

| 属性    | 值                               | 描述                                                         |
| :------ | :------------------------------- | :----------------------------------------------------------- |
| abbr    | *text*                           | 规定单元格中内容的缩写版本。                                 |
| align   | leftrightcenterjustifychar       | 规定单元格内容的水平对齐方式。                               |
| axis    | *category_name*                  | 对单元格进行分类。                                           |
| bgcolor | *rgb(x,x,x)**#xxxxxx**colorname* | 不推荐使用。请使用样式替代它。规定表格单元格的背景颜色。     |
| char    | *character*                      | 规定根据哪个字符来进行内容的对齐。                           |
| charoff | *number*                         | 规定对齐字符的偏移量。                                       |
| colspan | *number*                         | 设置单元格可横跨的列数。                                     |
| headers | *idrefs*                         | 由空格分隔的表头单元格 ID 列表，为数据单元格提供表头信息。   |
| height  | *pixels**%*                      | 不推荐使用。请使用样式替代它。规定表格单元格的高度。         |
| nowrap  | nowrap                           | 不推荐使用。请使用样式取而代之。规定单元格中的内容是否折行。 |
| rowspan | *number*                         | 规定单元格可横跨的行数。                                     |
| scope   | colcolgrouprowrowgroup           | 定义将表头数据与单元数据相关联的方法。                       |
| valign  | topmiddlebottombaseline          | 规定单元格内容的垂直排列方式。                               |
| width   | *pixels**%*                      | 不推荐使用。请使用样式取而代之。规定表格单元格的宽度。       |

### 113、`<thead>`

`<thead> `标签定义表格的表头。该标签用于组合 HTML 表格的表头内容。

tbody 元素用于对 HTML 表格中的主体内容进行分组，而 tfoot 元素用于对 HTML 表格中的表注（页脚）内容进行分组。

**注释：**如果您使用 thead、tfoot 以及 tbody 元素，您就必须使用全部的元素。它们的出现次序是：thead、tfoot、tbody，这样浏览器就可以在收到所有数据前呈现页脚了。您必须在 table 元素内部使用这些标签。

| 属性    | 值                         | 描述                                  |
| :------ | :------------------------- | :------------------------------------ |
| align   | rightleftcenterjustifychar | 定义 thead 元素中内容的对齐方式。     |
| char    | *character*                | 规定根据哪个字符来进行文本对齐。      |
| charoff | *number*                   | 规定第一个对齐字符的偏移量。          |
| valign  | topmiddlebottombaseline    | 规定 thead 元素中内容的垂直对齐方式。 |

```html
<table border="1">
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>

  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>

  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
</table>
```

### 114、`<time>`

`<time> `标签定义公历的时间（24 小时制）或日期，时间和时区偏移是可选的。

该元素能够以机器可读的方式对日期和时间进行编码，这样，举例说，用户代理能够把生日提醒或排定的事件添加到用户日程表中，搜索引擎也能够生成更智能的搜索结果。

| 属性           | 值         | 描述                                                         |
| :------------- | :--------- | :----------------------------------------------------------- |
| datatime:five: | *datetime* | 规定日期 / 时间。否则，由元素的内容给定日期 / 时间。         |
| pubdata:five:  | *pubdate*  | 指示 `<time> ``元素中的日期 / 时间是文档（或 <article> `元素）的发布日期。 |

```html
<p>我们在每天早上 <time>9:00</time> 开始营业。</p>

<p>我在 <time datetime="2008-02-14">情人节</time> 有个约会。</p>
```

### 115、`<tr>`

`<tr>` 标签定义 HTML 表格中的行。

| 属性    | 值                               | 描述                                                   |
| :------ | :------------------------------- | :----------------------------------------------------- |
| align   | rightleftcenterjustifychar       | 定义表格行的内容对齐方式。                             |
| bgcolor | *rgb(x,x,x)**#xxxxxx**colorname* | 不赞成使用。请使用样式取而代之。规定表格行的背景颜色。 |
| char    | *character*                      | 规定根据哪个字符来进行文本对齐。                       |
| charoff | *number*                         | 规定第一个对齐字符的偏移量。                           |
| valign  | topmiddlebottombaseline          | 规定表格行中内容的垂直对齐方式。                       |

```html
<table border="1">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```



### 116、`<track>`

`<track> `标签为诸如 video 元素之类的媒介规定外部文本轨道。

用于规定字幕文件或其他包含文本的文件，当媒介播放时，这些文件是可见的。

| 属性          | 值                                            | 描述                                                       |
| :------------ | :-------------------------------------------- | :--------------------------------------------------------- |
| default:five: | default                                       | 规定该轨道是默认的，假如没有选择任何轨道。                 |
| kind:five:    | captionschaptersdescriptionsmetadatasubtitles | 表示轨道属于什么文本类型。                                 |
| label:five:   | *label*                                       | 轨道的标签或标题。                                         |
| src:five:     | *url*                                         | 轨道的 URL。                                               |
| srclang:five: | *language_code*                               | 轨道的语言，若 kind 属性值是 "subtitles"，则该属性必需的。 |

```html
<video width="320" height="240" controls="controls">
  <source src="forrest_gump.mp4" type="video/mp4" />
  <source src="forrest_gump.ogg" type="video/ogg" />
  <track kind="subtitles" src="subs_chi.srt" srclang="zh" label="Chinese">
  <track kind="subtitles" src="subs_eng.srt" srclang="en" label="English">
</video>
```



### 117、`<tt>`

`<tt> `标签呈现类似打字机或者等宽的文本效果。

### 118、`<u>`

`<u>` 标签可定义下划线文本。

```html
<p>如果文本不是超链接，就不要<u>对其使用下划线</u>。</p>
```

### 119、`<var>`

| 标签     | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| <em>     | 呈现为被强调的文本。                                         |
| <strong> | 定义重要的文本。                                             |
| <dfn>    | 定义一个定义项目。                                           |
| <code>   | 定义计算机代码文本。                                         |
| <samp>   | 定义样本文本。                                               |
| <kbd>    | 定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。 |
| <var>    | 定义变量。您可以将此标签与 <pre> 及 <code> 标签配合使用。    |

### 120、`<video>`

`<video>` 标签定义视频，比如电影片段或其他视频流。

```html
<video src="movie.ogg" controls="controls">
您的浏览器不支持 video 标签。
</video>
```



| 属性     | 值       | 描述                                                         |
| :------- | :------- | :----------------------------------------------------------- |
| autoplay | autoplay | 如果出现该属性，则视频在就绪后马上播放。                     |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。             |
| height   | *pixels* | 设置视频播放器的高度。                                       |
| loop     | loop     | 如果出现该属性，则当媒介文件完成播放后再次开始播放。         |
| muted    | muted    | 规定视频的音频输出应该被静音。                               |
| poster   | *URL*    | 规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像。 |
| preload  | preload  | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
| src      | *url*    | 要播放的视频的 URL。                                         |
| width    | *pixels* | 设置视频播放器的宽度。                                       |






# CSS

---



## CSS重置

由于很多标签天生自带一些样式，所以我们需要用到CSS重置

例如：

`<p>`标签自带上下边距

`<button>`标签自带边框

`<li>`自带符号与内边距



实际操作如下：

```css
*{
	margin:0;
	padding:0;
	border:0;
	list-style:none;
}
```



重置一个复选框的样式：

```css
-webkit-appearence:none
```







---


## 伪类选择器

 *Pseudo-Classes Selectors(伪类选择器)*

**伪类**：同一个标签，根据其**不同的种状态，有不同的样式**。这就叫做“伪类”。伪类用冒号来表示。

比如div是属于box类，这一点很明确，就是属于box类。但是a属于什么类？不明确。因为需要看用户点击前是什么状态，点击后是什么状态。所以，就叫做“伪类”。

**静态伪类和动态伪类**

伪类选择器分为两种。

（1）**静态伪类**：只能用于**超链接**的样式。如下：

- `:link` 超链接点击之前
- `:visited` 链接被访问过之后

PS：以上两种样式，只能用于超链接。

（2）**动态伪类**：针对**所有标签**都适用的样式。如下：

- `:hover` “悬停”：鼠标放到标签上的时候
- `:active` “激活”： 鼠标点击标签，但是不松手时。
- `:focus` 是某个标签获得焦点时的样式（比如某个输入框获得焦点）



a标签有4种伪类（即对应四种状态）。如下：

- `:link` “链接”：超链接点击之前
- `:visited` “访问过的”：链接被访问过之后
- `:hover` “悬停”：鼠标放到标签上的时候
- `:active` “激活”： 鼠标点击标签，但是不松手时。

> 先lv再ha，先love后hate，先爱后恨



 ``` html
/*让超链接点击之前是红色*/ 	
a:link
	{ 
		color:red; 
	} 	

/*让超链接点击之后是橘黄色*/ 
a:visited
	{ 
		color:orange; 	
	} 

/*鼠标悬停，放到标签上的时候显示绿色*/
a:hover
	{
		color:green; 
	} 

/*鼠标点击链接，但是不松手的时候显示黑色		 
a:active
	{ 		
		color:black;
	}
  
 ```

<center>以上这些状态必须按此顺序排列</center>


| 属性         | 描述                                     | CSS版本 |
| :----------- | :--------------------------------------- | :------ |
| :active      | 向被激活的元素添加样式。                 | 1       |
| :focus       | 向拥有键盘输入焦点的元素添加样式。       | 2       |
| :hover       | 当鼠标悬浮在元素上方时，向元素添加样式。 | 1       |
| :link        | 向未被访问的链接添加样式。               | 1       |
| :visited     | 向已被访问的链接添加样式。               | 1       |
| :first-child | 向元素的第一个子元素添加样式。           | 2       |
| :lang        | 向带有指定 lang 属性的元素添加样式。     | 2       |

***提示：在 CSS 定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。***

***提示：在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。***

***提示：伪类名称对大小写不敏感。***



<p style="text-align:center;background-color:white;color:red;">
    CSS3与伪类选择器
</p>



**:not()**

> 这个选择器的意思是，选中除了谁,括号里面填入不想选中的对象。

> 例如 `div:not(last-of-type) `意思为选中除了最后一个div标签外的所有div标签

**:root**

> **选择根目录的意思**，在我们的html文件里面，他是选 html标签 也就是 html标签选择器。但是呢，如果换成xml呢，他的根目录就不一定是 html了吧。所以有人说 root就是html，那是错误的

> 要用的话，直接写 :root{ background-color:red;} 即可 相当于 html:{ background-color:red;} 

**:target**

> URL后面跟锚点#，指向文档内某个具体的元素。 也就是说，url后面的锚点，指向 某个元素， 那么该元素就会触发 target
>
> ```html
> 就比如说
> <a href="#id">content<a>
> <div id="id">
> new content
> </div>
> 那么点击content链接页面URL后面就会出现#id并触发:target
> ```

**:first-child　**

> 选择父元素下的第一个子元素
>
> 冒号前加想选中的元素
>
> **注意:**如果第一个元素不是你想选择的元素，则不会选中任何元素

**:last-child** 

> 选择父元素下的最后一个子元素
>
> 冒号前加想选中的元素
>
> **注意:**如果最后一个元素不是你想选择的元素，则不会选中任何元素

**:only-child**

> 选择，父元素下的 *独生子*，也就是说，看父元素下面的子元素，是不是仅有一个,如果是的话，则那就选中

**:nth-child(n)**

> 选择父元素下面的 第几个子元素，(n) 可以计算， n是从0 开始的， 但是 css里面的索引是从1 开始的
>
> **注意：**js的数组什么是从0. 但是css是从1开始
>
> *n可以取 odd(奇数) 和 even(偶数)*

**nth-last-child(n)**

> 跟上面的选择器大同小异， 只不过人家是从 最后一位开始查数	 **填(1) 选的是最后一位**



<p style="text-align:center;font-size:20px;color:red;">以上的这5个选择器都会受到 其他元素的影响， 例如父元素下面第一个不是他的话，就选不了。



<p style="text-align:center;font-size:20px;color:red;">但是以下五个选择器，不会受到其他元素的影响。





**:first-of-type**

> 意思是，在父元素下面寻找 第一个所匹配的子元素
>
> 如：下面的ul 和li，在ul 里面找到第一个li

**:last-of-type**

> 在有父元素的里面找最后一个子元素，跟上面的选择器一样， 他选的是第一个， 这个选的是最后一个

**:only-of-type**

> 匹配父元素的所有子元素中唯一的那个子元素

**:nth-of-type(n)**

> 匹配父元素的第n个子元素，跟 **:nth-child(n)** 差不多， 不过 nth-child 会受到其他元素影响， 而nth-of-type 不会

**:nth-of-last-type(n)** 

> 跟 **:nth-of-type(n)** 相反的， **:nth-of-type(n)**是按照 第一个开始查， 这个是按照倒数第一位查

**:empty**

> 匹配里面**没有任何东西**的元素
>
> 也就是说，你选择的那个元素，里面没有东西才可以被选中

**:checked**

> 匹配用户界面上处于选中状态的元素。(用于input type为radio与checkbox时)
>
> 一般在被选中时候，额外增加一些样式或文字等

**:enabled　　**

**:disabled**

> 用于选择 `input`的 正常状态，和 不可操作状态。
>
> 没设置`disabled `属性的` input` 就是正常状态

**:read-only　**

**:read-write**

>read-only 呢 是input 标签上的属性， 设置了这个属性后，就是不可以填写，也不可以操作
>
>该选择器就是选中有read-only属性的标签

> :read-write 也就是选中没有设置:read-only 的元素	用处不大



---

## 选择器

1、基本选择器

```
1、通配符选择器:*;
2、元素选择器:元素标签;
3、class选择器:相当于身份证上的名称;
4、id选择器:相当于身份证号（唯一性）;
```

2、多元素选择器

```
1、多元素选择器E,F 选择所有的E元素或者F元素
2、后代选择器E F 选择所有属于E元素的后代元素F 即E元素包含F即可
3、子元素选择器E > F 选择所有E元素的子元素F，即E元素的下一级元素F
4、毗邻选择器E + F 选择所有紧随E元素的同级元素F，即跟在E元素后的第一个同级兄弟元素
```

3、属性选择器

```
1、[att] 选择所有具有att属性的元素
2、[att=val] 选择所有att属性等于val的元素
3、[att~=val] 选择所有att属性包含val或者等于val的元素 val为单独的一个词
4、[att|=val]选择所有att属性为val或者val-开头的元素
5、[att1][att2=val]选择所有具有att1属性且所有att2属性等于val的元素
6、[att*=val] 选择所有att属性包含val的元素，val可以成为一个词中的一部分
7、[att^=val]选择所有att属性等于val开头的元素，val可成为一个词中的一部分
8、[att$=val]选择所有att属性以val结尾的，val可以为一个词中的一部分
```

4、伪类

```
1、伪类选择器 :link，:visited,:hover,:active;
2、伪类元素选择器 :before;:after;
3、E:target 当 a 标签获取焦点href=""所对应的E元素锚点;
4、E:diabled 表示不可点击的表单控件 ;
5、E:enabled 表示可点击的表单控件;
6、E:checked 表示已选中checkbox或radio
7、E:first-line 表示E元素集合中的第一行
8、E:first:letter 表示E元素中的第一个字符
9、E::selection 表示E元素在用户选择文字时
10、E:not(selector)选择非selector中的每个元素
11、E~F 表示E元素后的所有兄弟F元素

```

在元素之后加上伪类元素：

```
xxx::after{
	content:"";
	····
}
```











5、结构性伪类

```
1、E:nth-child(n) 表示E父级所有子元素集合中的第n个子节点(2n(even)匹配偶数行，2n-1（odd）匹配奇数行);
2、E:nth-last-child(n) 表示E父级所有子元素(从后向前)集合中的第n个子节点;
3、E:nth-of-type(n) 表示E父级的子元素E的集合中第n个节点(区分标签类型);
4、E:nth-last-of-type(n) 表示E父级的子元素E(从后向前)集合中的第n个子节点(区分标签类型)
5、E:empty 表示E元素中没有子节点(不能有空格、回车)，子节点包含文本节点
```





---

## BFC

***块格式上下文规则***（一个浏览器渲染元素的规则）

如果一个文件触发了BFC规则，我们就把它称之为BFC区域

**特点：**

==让父元素触发BFC规则即可达成目的==

1、两个BFC区域之间不会互相影响，也就是说内部子元素出现上下边距，边距不会跑到父元素**外面**影响其他元素，只会在父元素**内部**拉开距离；（平时在设置子元素左右边距是可以达成效果的，但是设置上下边距，却连同父元素一起有了边距，而上下边框却与父元素重合，这些规则虽然很离谱，但都是W3C制定的）

2、如果BFC元素内部有浮动元素，则浮动元素的宽高也会被考虑进去，这样一来无论有多少浮动元素都不会害怕父元素没有高度了。

**触发条件**

```html
<style>
    n{ 
        条件如下：
        float:left/right;
        position:absolute/fixed;
        display:inline-block/tabl-cell等;
        overflow:auto/hidden等;
    }
</style>

```



*以上元素无论是浮动、定位、还是更改元素类型都会大幅度改变页面排版布局，而我们的`overflow`属性却不会，所以我们一般都采用`overflow`属性来触发BFC规则。*

<hr>



## 字体图标的引用

我们常常需要用到别人用CSS写的字体图标（非图片的图形）

下载图形符号的网址（阿里巴巴矢量图标库）：https://www.iconfont.cn/

1、进入网址后可以直接下载你需要的图标，**但是**在有1个以上想要的矢量图时，推荐加入购物车一起下载

2、下载完毕后打开html文件，了解如何使用矢量图

一般有三种使用方式：

一、

**Unicode 引用**

Unicode 是字体在网页端最原始的应用方式，特点是：

- 兼容性最好，支持 IE6+，及所有现代浏览器。
- 支持按字体的方式去动态调整图标大小，颜色等等。
- 但是因为是字体，所以不支持多色。只能使用平台里单色的图标，就算项目里有多色图标也会自动去色。

> 注意：新版 iconfont 支持多色图标，这些多色图标在 Unicode 模式下将不能使用，如果有需求建议使用symbol 的引用方式

Unicode 使用步骤如下：

**第一步：拷贝项目下面生成的 `@font-face`**

```css
@font-face {
  font-family: 'iconfont';
  src: url('iconfont.eot');
  src: url('iconfont.eot?#iefix') format('embedded-opentype'),
      url('iconfont.woff2') format('woff2'),
      url('iconfont.woff') format('woff'),
      url('iconfont.ttf') format('truetype'),
      url('iconfont.svg#iconfont') format('svg');
}
```

**第二步：定义使用 iconfont 的样式**

```css
.iconfont {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```

**第三步：挑选相应图标并获取字体编码，应用于页面**

```html
<span class="iconfont">&#x33;</span>
```

> "iconfont" 是你项目下的 font-family。可以通过编辑项目查看，默认是 "iconfont"。

二、

**font-class 引用**

font-class 是 Unicode 使用方式的一种变种，主要是解决 Unicode 书写不直观，语意不明确的问题。

与 Unicode 使用方式相比，具有如下特点：

- 兼容性良好，支持 IE8+，及所有现代浏览器。
- 相比于 Unicode 语意明确，书写更直观。可以很容易分辨这个 icon 是什么。
- 因为使用 class 来定义图标，所以当要替换图标时，只需要修改 class 里面的 Unicode 引用。
- 不过因为本质上还是使用的字体，所以多色图标还是不支持的。

使用步骤如下：

**第一步：引入项目下面生成的 fontclass 代码：**

```html
<link rel="stylesheet" href="./iconfont.css">
```

**第二步：挑选相应图标并获取类名，应用于页面：**

```html
<span class="iconfont icon-xxx"></span>
```

> " iconfont" 是你项目下的 font-family。可以通过编辑项目查看，默认是 "iconfont"。

三、

**Symbol 引用**(可以展示彩色矢量图)

这是一种全新的使用方式，应该说这才是未来的主流，也是平台目前推荐的用法。相关介绍可以参考这篇[文章](http://127.0.0.1:8848/Hello-Html/034图片字引用/font/demo_index.html) 这种用法其实是做了一个 SVG 的集合，与另外两种相比具有如下特点：

- 支持多色图标了，不再受单色限制。
- 通过一些技巧，支持像字体那样，通过 `font-size`, `color` 来调整样式。
- 兼容性较差，支持 IE9+，及现代浏览器。
- 浏览器渲染 SVG 的性能一般，还不如 png。

使用步骤如下：

**第一步：引入项目下面生成的 symbol 代码：**

```html
<script src="./iconfont.js"></script>
```

**第二步：加入通用 CSS 代码（引入一次就行）：**

```html
<style>
.icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>
```

**第三步：挑选相应图标并获取类名，应用于页面：**

```html
<svg class="icon" aria-hidden="true">
  <use xlink:href="#icon-xxx"></use>
</svg>
```

## 移动端网页适配

第一种方案：百分比适配

例如：在750px宽的页面，按钮宽度不设置90px而设置12%。

但是页面上有这么多元素，每一个都要计算它的百分比大小，想一想都麻烦得要死

第二种方案：使用媒介查询

通过

```css
@media screen and (max-width:1280px){
    
}
@media screen and (max-width:720px){
    
}
​``````
```

市面上有多少屏幕尺寸就写多少条样式

第三种方案：使用rem单位

1 rem = ?? px

当我们设置

```css
html{font-size=20px;}
```

那么1 rem = 20 px

接下来我们页面上的所有元素就可以使用rem这个单位来控制大小了

## 奇奇怪怪的空档区

当在块元素中放入图片时，仔细观察发现图片底部有一个空档，这是怎么回事？

引入了`baseline`属性，当你放一个图片，图片底部那条线就是`baseline`

这来源于英语在书写时的格子，倒数第二行就是我们所说的`baseline`，所有的英文字母都根据`baseline`对齐

而在插入图片时，会自动在后面意淫一个英文单词并且对齐，空白就产生了

解决办法

```css
vertical-align:middle;
这样就会把baseline转化为middleline,就不存在下面空出一截的情况了
```


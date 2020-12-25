# CSS

## 样式

### 1、阴影

```css
box-shadow:0px 0px 0px 0px black inset;
box-shadow: left偏移值 top偏移值 模糊度 扩大范围 影子颜色 影子方向（内/外）;	影子默认方向向外
比如：
box-shadow:0px 0px 5px 0px black;		模糊
box-shadow:5px 5px 0px 0px black;		位移
box-shadow:0px 0px 0px 5px black;		扩大
box-shadow:2px 2px 5px 0px black;		位移模糊
box-shadow:0px 0px 5px 0px black inset;  阴影向内，模糊
```

常见的按钮阴影样式

```css
box-shadow:
	0 29px #CCCCCC inset,
	0 1px  2px 1px #656565,
	0 0 0 6px #CACACA,
	0 0 0 8px #ffffff,
	0 0 0 10px #696969,
	0 2px 3px 11px #CBCBCB;
```

文字阴影

```css
test-shadow:{
    5px 5px 5px #222222
}
```

### 2、渐变背景

```css
background:linear-gradient(to bottom,#d3d3d3,#9e9e9e);
background:linear-gradient(方向,起始颜色,最终颜色);
linear-gradient(线性渐变)
方向：
to bottom
to left
to top
to right
...
也可以写角度
45deg
```

### 3、过渡动画

> transition 属性是一个简写属性，用于设置四个过渡属性：transition-property、transition-duration、transition-timing-function、transition-delay

```css
transition: width 1s ease-in 2s;
transition:过渡的属性 过渡的时间 过渡的方式 延迟时间;
过渡属性：
border-radius 圆角
background-color 背景色
opacity	不透明度
height 高
box-shadow 阴影

过渡的方式：
ease 先快后慢
linear 线性
ease-in 慢速开始
ease-out 慢速结束
ease-in-out 慢速开始 慢速结束
```

深度了解：

贝塞尔曲线

### 4、转换动画

> transform 属性向元素应用 2D 或 3D 转换。该属性允许我们对元素进行旋转、缩放、移动或倾斜

改变偏移量

```css
transform:translateY(Y坐标偏移) translateX(X坐标偏移) translateZ(Z坐标偏移);
transform标签之间可以实现各种动画效果
```

改变变形圆点

```css
transform-origin:20% 50%
第一个是x轴值
第二个是y轴值
来定位
除了比例也可以写成像素的形式
可以设置观察视角
```

改变图像大小

```css
transform:scale(1)
```

改变图像旋转角度

```css
transform:rotateX(10deg) routateY(10deg) rotateZ(10deg)
旋转图像的XYZ轴
注意：Z轴垂直于屏幕
```

在旋转角度的时候要设置透视才能使得旋转更加真实

```css
transform:perspective(500px);
透视（观察）距离，要写在旋转前面才能生效
给父元素增加该属性则是以父元素中心点来观察物体
给单个元素增加该属性则是单独观察该元素

```

使得转换动画呈3D构图

```css
transform-style: preserve-3d;
```

可以通过`position: absolute;`改变图像偏移量的参考位置

### 5、响应式

网页在不同设备，不同大小的窗口上的显示格式

```css
@media screen and (max-width:640px){
--网页在窗口最大宽不超过640px的时候显示这样的样子--
}
@media 是设备名称
screen 是窗口的意思
```

在移动端，如何配置网页

```css
<meta name:"viewport" content="width=device-width" ,initial-scale=0.5>
/*
viewport：网页窗口 width=device-width：网页宽度等于设备宽度 initial-scale：让网页变成原来的几倍
对于initial-scale值并不是随便定的，他根据设备的dpr值，来进行缩放，例如iphone8 的 dpr=2代表原来的1像素内容在手机里变成2像素
dpr=2 则 initial-scale=0.5 ； dpr=3 则 initial-scale=0.333
物理像素（设备能设置的最大分辨率）
设备的独立像素（设备出厂设置的默认像素）
dpr=物理像素/设备独立像素
*/

```

### 6、帧动画

制作帧动画

```css
@keyframe beat /*关键帧名字*/
    /*关键帧*/
{ /*关键帧插入在30%的位置上和100%的位置上*/
    30%{
        transform:scale(1.3); /*30%的时候把内容放大到原来的1.3倍*/
    }
    100%{
        transform:scale(1); /*100%的时候内容恢复原来的样子*/
    }
}
```

使用帧动画

```css
span.heart{
    animation: beat 1.5s 0.5s infinite;/*animation: 动画名称 动画时长 开始时间 执行方式(infinite 反复执行)*/
}
```

### 7、对齐方式

垂直对齐

`vertical-algin`

只适用于`inline-block`元素

```css
vertical-algin:middle;
```

### 8、元素优先级

`z-index`

```css
z-index=100;
/* z-index的值高的元素可以覆盖数值低的元素*/
```

### 9、不透明度

```css
opacity属性
可以直接给元素添加
```



```css
rgba(R,G,B,A)
A为透明度
```




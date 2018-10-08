[TOC]

### pseudo-element（伪元素）
***

#### 定义:
是添加到选择器的关键字，它允许您设置所选元素的特定部分的样式。例如，::first-line可用于更改段落第一行的字体。

#### 语法
>selector::pseudo-element {
  property: value;
}

####  标准元素：
![](https://github.com/yuanchaojie/Notes/blob/master/Sources/pseudo-element-E.g.png?raw=true)

```
::after 
创建一个伪元素，它是所选元素的最后一个子元素。它通常用于将cosmetic content添加到具有该content属性的元素。它默认是内联的。
如:/* Add an arrow after links */
a::after {
  content: "→";
}`
```
#### 参考
><https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements>

### pseudo-class（伪类）
***

#### 定义:
伪类是添加到选择器的关键字，用于指定所选元素的特殊状态。例如，:hover可以在用户将鼠标悬停在按钮上时更改按钮的颜色。

#### 语法
>selector:pseudo-class {
  property: value;
}

####  标准元素：
![](https://github.com/yuanchaojie/Notes/blob/master/Sources/pseudo-classes-E.g.png?raw=true)

```
:nth-last-of-type(n)
匹配其父元素的特定类型的第n个子元素的每个元素，从最后一个子元素开始计算
n can be a number, a keyword, or a formula.(n可以是数字，关键字或公式。)

:nth-last-child()
从最后一个子项开始计算，选择其父项的第n个子元素，无论其类型如何。

```

#### 参考
><https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-classes>

### position
***

#### 定义:
position属性用于指定一个元素在文档中的定位方式。top，right，bottom 和 left 属性则决定了该元素的最终位置。

#### 语法格式
> static | relative | absolute | sticky | fixed

#### 参考
><https://developer.mozilla.org/en-US/docs/Web/CSS/position>











[TOC]

### 元素的位置和尺寸的影响因素：
*** 

<https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/transform>

不同情况下 containing block


#### transform:
 <https://developer.mozilla.org/en-US/docs/Web/CSS/transform>

#### A Complete Guide to Flexbox
<https://css-tricks.com/snippets/css/a-guide-to-flexbox/>

#### A Visual Guide to CSS3 Flexbox Properties
<https://scotch.io/tutorials/a-visual-guide-to-css3-flexbox-properties>


### 用 CSS 实现元素垂直居中，有哪些好的方案？
***

#### 知乎方案
1. 不知道自己高度和父容器高度的情况下, 利用绝对定位只需要以下三行：

	```
	parentElement{
	    position:relative;
	}
	
	childElement{
	    position: absolute;
	    top: 50%;
	    transform: translateY(-50%);
	
	}
	
	```

2. 若父容器下只有一个元素，且父元素设置了高度，则只需要使用相对定位即可


	```
	parentElement{
	    height:xxx;
	}
	
	.childElement {
	  position: relative;
	  top: 50%;
	  transform: translateY(-50%);
	}
	```

3. Flex 布局：不考虑兼容老式浏览器的话，用Flex布局简单直观一劳永逸

	```
	parentElement{
	    display:flex;/*Flex布局*/
	    display: -webkit-flex; /* Safari */
	    align-items:center;/*指定垂直居中*/
	}
	```
	
#### 引用：
><https://www.zhihu.com/question/20543196>


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

### The stacking context
***

#### 定义:
层叠上下文是HTML元素的三维概念，这些HTML元素在一条假想的相对于面向（电脑屏幕的）视窗或者网页的用户的z轴上延伸，HTML元素依据其自身属性按照优先级顺序占用层叠上下文的空间。

**注意：z-index:number number数值越大的层在上面，小的在下面**


#### 形成条件

* Root element of document (HTML).
* Element with a position value "absolute" or "relative" and z-index value other than "auto".
* Element with a position value "fixed" or "sticky" (sticky for all mobile browsers, but not older desktop).
* Element that is a child of a flex (flexbox) container, with z-index value other than "auto".
* Element with a opacity value less than 1 (See the specification for opacity).
* Element with a mix-blend-mode value other than "normal".
* Element with any of the following properties with value other than "none":
    * transform
    * filter
    * perspective
    * clip-path
    * mask / mask-image / mask-border
* Element with a isolation value "isolate".
* Element with a -webkit-overflow-scrolling value "touch".`（-webkit-overflow-scrolling:属性控制元素在移动设备上是否使用滚动回弹效果. auto 无滚动效果 touch 有滚动效果）`
* Element with a will-change value specifying any property that would create a stacking context on non-initial value (see this post).
* Element with acontain value of "layout", or "paint", or a composite value that includes either of them.

#### 参考
><https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/The_stacking_context>

### MIME types
***

MIME（Multipurpose Internet Mail Extensions）多用途网络邮件扩展

**语法：**type/subtype

#### 重要的MIME types：

* application/octet-stream

    这是应用程序文件的默认值。意思是 未知的应用程序文件 ，浏览器一般不会自动执行或询问执行。浏览器会像对待 设置了HTTP头Content-Disposition 值为“附件”的文件一样来对待这类文件。

* text/plain

    文本文件默认值。意思是 未知的文本文件 ，浏览器认为是可以直接展示的。

* multipart/form-data

    multipart/form-data 可用于HTML表单从浏览器发送信息给服务器。作为多部分文档格式，它由边界线（一个由'--'开始的字符串）划分出的不同部分组成。每一部分有自己的实体，以及自己的 HTTP 请求头，Content-Disposition和 Content-Type 用于文件上传领域，最常用的 (Content-Length 因为边界线作为分隔符而被忽略）。
    
#### Importance of setting the correct MIME type

很多web服务器使用默认的 application/octet-stream 来发送未知类型。出于一些安全原因，对于这些资源浏览器不允许设置一些自定义默认操作，导致用户必须存储到本地以使用。常见的导致服务器配置错误的文件类型如下所示：
    
* RAR编码文件。在这种情况，理想状态是，设置真实的编码文件类型；但这通常不可能（可能是服务器所未知的类型或者这个文件包含许多其他的不同的文件类型）。这这种情况服务器将发送 application/x-rar-compressed 作为MIME类型，用户不会将其定义为有用的默认操作。
    
* 音频或视频文件。只有正确设置了MIME类型的文件才能被 `<video> 或<audio>` 识别和播放。
    
* 专有文件类型。是专有文件时需要特别注意。使用 application/octet-stream 作为特殊处理是不被允许的：对于一般的MIME类型浏览器不允许定义默认行为（比如“在Word中打开”）

#### 参考
><https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types>
    

    












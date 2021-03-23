

## 摘要

> 本片是在老师理论知识的指导下进行自己尝试总结(理论有部分搬运了[老师](https://qige.io/)的教程)，自己并做了一些尝试，最后结果还是很丑陋。但是我会不断完善的。


## 一、HTML简介

**HTML**是超文本标记语言（HyperText Markup Language）的缩写。我们用 HTML 来构建 Web 页面即所谓的网页。

在我看来相当于Web的框架。需要与之后学习的CSS(起到修饰作用)，JS(内部行为)共同构建我们所说的网页。

我们可以将这些内容跟上传到互联网，然后让它和别人创建的相链接。

> 右键单击网页，可以查看网络源码，可以看到HTML文档



## 二、HTML文档结构

基本结构：

```html
<!DOCTYPE html>
<html>

<head> 
</head>

<body>

</body>
```

> 总结其基本构架：
>
> - html：元素。这个元素包裹了整个完整的页面，是一个根元素，它元素都嵌套到其中。
> - head：表示标签头，可以加入图标； 这个元素是一个容器，它包含了所有你想包含在HTML页面中但不想在HTML页面中显示的内容。这些内容包括你想在搜索结果中出现的关键字和页面描述，CSS样式，字符集声明等等。
> - body：含你能在页面看到的所有内容，包括文本，图片，音频，游戏等等



相关的一些练习：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <link rel="shortcut icon" href="./images/ICO.svg" type="image/x-icon" />
    <title>LEE</title>
  </head>
  <body>
    <h2><mark>这是我的第一次练习</mark></h2>
    <h4>现在开始了:)</h4>
  </body>
</html>
```

> 相关解释
>
> - meta：这个元素设置文档使用utf-8字符集编码，
> - link：指定页面的图标，出现在浏览器标签上。
> - h1为一级标题，从一级到六级，包括了h1，h2...h6
> - p表示段落
> - mark为高亮



### :fire: HTML元素

HTML 使用"标记"（markup）来注明文本、图片和其他内容，以便于在浏览器中显示。HTML 标记包含一些规定的"元素"如<：`head>，<title>，<body>，<header>，<footer>，<article>`等

检查我们刚创建的 HTML 文档你会发现，整个 HTML 就由一个个元素组成（可以嵌套），而元素则一般由一对标签（tag）构成。

> 注释：==ctrl+/==

**空元素**

元素都拥有**开始标签，内容，结束标签**。但有一些元素只有一个开始标签，通常用来在此元素所在位置插入/嵌入一些东西，如`<br>, <hr>, <input>, <img>, <a>`等等。我们称其为空元素，如下：

> br：换行
>
> input：输入框

**元素的属性**

元素是可以有相关属性的。属性包含元素的额外信息，这些信息不会在浏览器中显示出来。

```html
    <p><br /><br /><mark>元素属性</mark><br /><br /></p>
    <p title="这是title的属性">鼠标放置显示</p>
    <input title="请输入用户名" type="text" />
    <input title="密码" type="password" />
```

>一个属性必须包含如下内容：
>
>1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
>2. 属性名称，后面跟着一个 = 号。
>3. 一个属性值，由一对引号 "" 引起来。



### :fire: 文本格式



> `<mark>highlight</mark>`高亮
>
> `<del>This line of text is meant to be treated as deleted text.</del>`划掉



### :fire: 超链接

没有超链接就没有万维网（World Wide Web）。基本上，我们可以把任何东西加上超链接，不过常用的是文本、图片等。

这里我设计了一个重庆交通大学的超链接

```html
<a href="http://www.cqjtu.edu.cn/" target="_blank"><em>重庆交通大学</em></a>
```

说明：

1. `href`即为要跳转去的地址 ==URL（Uniform Resorce Locator )==
2. `target`属性为`_blank`表示在==新的页面==打开超链接（默认是在当前页面打开即`_self`）
3. 超链接标签包含的内容（当前为文字"百度一下"）即为显示在页面上供用户点击的

**锚点**

锚点，也称为书签，用于标记页面的某个元素或位置。通过锚点，我们可以轻易的在==长页面内==实现跳转。

先使用`id`属性生成某元素的锚点，然后再使用超链接指向该锚点即可。

```html
<h3 id="C1">这是一个锚点</h3>
<a href="#C1"><br />返回头部</a>
```

>**注意：**
>
>1. 元素的`id`值必须是唯一的，也即页面不能再有其它元素的`id`值为`C4`
>2. 超链接中的地址需要有`#`符号



### :fire: 图片及文件路径

```html
    <!-- 图片及文件路径，这个是绝对路径img -->
    <img src="https://riyugo.com/i/2021/03/02/nt32k2.png" alt="MDB Logo" />
    <p>
      <mark><br />CLIMB!!<br /></mark>
    </p>
```

```html
 <!-- 相对路径 -->
    <img src="./images/test1.jpg" alt="MDB Logo" width="400" height="400" />
```



> 图片URL获取需要==图床==，可以采用空间和微博生成，当然也可以用一些免费图床
>
> 以下都可以采用
>
> [薄荷图床](https://riyugo.com/)(国内免费的图床)
>
> [国外免费图床](https://sm.ms/)
>
> [IO图床](https://www.imageoss.com/)

说明：

1. `src`属性为要显示图片文件的位置 URL，即图片文件的路径
2. `alt`属性当获取图片出现问题时显示的文字（占位符）
3. 可为图片指定高宽度，但不建议（可能导致图片变形）

**提示：** 对于小尺寸的图片，现在可采用 **base64** 编码进行，可提高页面加载速度，提升用户体验。[可前往一试](https://c.runoob.com/front-end/59)。(小图比较合适)

```html
<!-- 生成base64编码后的引用方式 -->
<p><br /><mark>ICON</mark><br /><br /></p>
<img
      src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMgAAADI.../>
```

**文件路径**

为获取图片文件，我们需要指定该文件位于何处，这称为文件路径。文件路径有相对路径和绝对路径两种。

上面图片的例子即为绝对路径。下面是相对路径的例子：

- `<img src="picture.jpg">`  该图片文件与当前文档在同一目录中  
- `<img `src="./images/picture.jpg">`  该图片文件在当前目录下的`images`目录中 
- `<img src="../picture.jpg">`  该图片文件在上一级目录中



## 三、结果

这个结果还是很丑陋的，没有CSS的修饰确实没有很好的效果，暂且借用了老师的css文件，实现稍微好看一点儿的效果，这时第一次。

![](https://img-blog.csdnimg.cn/img_convert/339a9e1c402256c95dad3ce60f550faa.png)

![](https://img-blog.csdnimg.cn/img_convert/cab48d00f3297e17a1e7d5224a72212d.png)

![](https://img-blog.csdnimg.cn/img_convert/4d504099fefd17851c104a47f0e12212.png)

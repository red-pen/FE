HTML标签语义化
=============

HTML的标签（tags）都是具有一定含义的（http://w3school.com.cn/html5/html5_reference.asp）。如： `<img />` 表示图像，`<p>` 代表段落，`<ol>` 代表有序列表等。

这种标签的 __语义化__ （Semantic），是HTML在制定的最初就一直遵守的规则，用来将文本等信息结构化，从而方便理解和使用。

###HTML标签语义化的意义

1. 有利于搜索引擎的检索（SEO）  
有利于搜索引擎对网页的结构和内容的分析，更容易查找到关键信息。
2. 便于人的理解  
结构化的HTML文档，更容易被人理解。统一的编写标准，也便于团队协作和进行传播。
3. 脱离样式时仍然结构清晰  
去掉或丢失样式时，仍保持默认样式，不影响页面的可读性。对于无法有效执行CSS的特殊设备（如手机），也会保持可读的结构。
4. 有利于特殊群体的阅读  
很可能有访问者需要借助屏幕阅读器等设备来识别网页内容，语义化的页面更容易将有效信息分离出来。

###错误的代码风格

早期的开发者为了使页面具有丰富的布局，往往使用 `<table>` 将页面划分成多个部分，甚至嵌套多个 `<table>` 来实现特殊布局，这是Web开发最黑暗的时期。`<table>` 标签的作用是以表格的形式呈现数据，而不是用来进行页面布局。

在CSS的功能增强之后，又出现了大批 `“DIV+CSS”` 的倡导者（决定写这篇文章之前，我也是其中之一）。虽然这种方式结束了使用 `<table>` 进行布局的错误，但仍旧没有很好的遵循标签语义化的规则。`<div>` （division）代表了分隔和区块的意思，由于仅有 `display:block` 这一个默认属性，因此用它来进行页面的布局最为合适。但在页面内容上，最好使用 `<h2>` `<p>` 等具有语义的标签，使页面的内容可识别。

###HTML5带来的变化

在近几年的发展中，网页编写风格逐渐趋向统一。  
根据Google的分析数据（<https://developers.google.com/webmasters/state-of-the-web/2005/classes>），有许多网站都在使用相同的 `class name` 来命名页面元素。这些元素是大部分网站需要的，但HTML中并没有匹配的元素可用，所以大部分都是使用 `<div>` 来编写的。

在HTML5中，规则的制定者认识到了这个普遍存在的问题，并增加了许多与 `<div>` 类似的，但更加语义化的标签（<http://w3school.com.cn/html5/html5_reference.asp>）：

     <header> 代表页眉
     <footer> 代表页脚
     <nav> 代表导航链接
     <article> 代表页面主体（如文章）
     <aside> 代表非页面主体（如侧边栏）
     <menu> 代表表单菜单
     等等。

同样，由于HTML5以标签语义化作为指导，也相应的抛弃了一些非语义化的标签（这些标签在XHTML1.0中，也是不推荐使用的）：

     <center> 定义文本居中
     <font> 曾用于定义文本的样式
     <s>、<strike> 曾用于定义带删除线的文本
     <u> 曾用于定义带下划线的文本

等等，建议完全使用CSS代替其功能。

还有另外一些标签的含义和作用被重新定义或区分了：

     <strong> 表示文本的重要（文本显示为加粗效果）
     <b> 文本显示为加粗效果
     <em> 表示阅读时，需要使用强调的语气（文本显示为斜体效果）
     <i> 文本显示为斜体效果

###语义化标签应用指导

对于比较常见的类Wordpress模板，可以使用如下的结构安排页面：

![blog-template](/images/html-semantic-blog-template.png "Wordpress HTML5 模板")

左侧使用了HTML4风格的 `<div>` 标签布局，右侧使用了HTML5的语义化标签布局。语义化的标签更加简洁和直观，更容易理解其含义。

可能会有人担心：HTML5尚未成为推荐的标准，是否会存在兼容性问题？答案是肯定的。不过，无法支持HTML5的浏览器已经很少了（<http://caniuse.com/#feat=html5semantic>），是时候加速它们的死亡了。所以，完全可以大胆地尝试新的语法了。

参考链接：

>1.<http://www.cnblogs.com/yhongyu/archive/2012/06/01/2530891.html>
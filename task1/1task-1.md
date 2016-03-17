##HTML5 header，nav，main，footer标签
HTML中```header```标签定义文档页眉（介绍信息），```header```元素表示一组引导性的帮助，可能包含标题元素，或其他元素，像logo，分节头部，搜索表单等。

HTML```main```元素呈现了文档```body```或应用的主体部分。主体部分由与文档直接相关，或者扩展文档的中心主题，应用的主要功能部分的内容组成。这部分内容在文档中应该是独一无二的，不包含任何在一系列文档中的重复的内容，比如侧边栏，导航栏，版权信息，网站logo，搜索框等。

> * ```main```标签不能是以下元素的继承：```article``` ```aside``` ```footer``` ```header``` ```nav```
> * 在文档中不能出现一个以上的```main```标签

HTML导航栏```nav```描绘含有多个超链接的区域，这个区域包含转到其他页面，或者页面内部其他部分的链接列表。

> * 并不是所有的链接必须使用```nav```元素，它只是用来将一些热门的链接放入导航栏，例如```footer```元素就常用来在页面底部包含一个不常用到，没必要加入```nav```的链接列表。
> * 一个网页也可能含有多个```nav```元素，例如一个是网站内的导航列表，另一个是本页面内的导航列表。
> * 对于屏幕阅读障碍的人可以使用这个元素来确定是否忽略初始内容。

HTML中```footer```元素表示最近一个章节内容或者根节点元素的页脚。一个页脚通常包含该章节作者，版权数据或与文档相关的链接等信息。
##HTML5 section 标签
HTML中 ```section```定义文档中的区段，节。比如章节，页眉，页脚或文档中的其他部分。
简单说```section```就是带有语义的div，表示一段专题性的内容。当一个标签只是为了样式化或方便脚本使用时应该使用div。当元素内容明确地出现在文档大纲中，```section```就是适用的。
示例：文档中的区段
```html
<section>
    <h1>标题</h1>
    <p>内容...</p>
</section>
```

属性：

|属性 |值 |描述|
|-----|---: |:---:|
|cite |URL |```section```的URL，假如```section```摘自web的话|

##HTML5 artical 标签
HTML中```artical```标签，是一个特殊的```section```标签。比```section```更具有明确的语义，代表一个独立的，完整（看这段内容脱离了所在语境还是否是完整的独立的）的相关内容块。一般来说```article```会有标题部分（通常包含在header内），包含footer。

定义外部的内容，外部的内容可以是来自一个外部的新闻提供者的一篇新的文章，或者来自blog的文本，或者来自论坛的文本等。   ---[W3School article标签](http://www.w3school.com.cn/html5/html5_article.asp)

HTML中```article```元素表示文档，页面，应用或网站中独立结构，其意在成为可独立分配的或可复用的结构。如在发布中，可能是论坛帖子，杂志或新闻文章，博客，用户提交的评论，交互式组件，或其他独立的内容项目。   ---[MDN article标签](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article)
> * 当```article```元素嵌套使用时，则该元素代表与外层元素有关的文章。例如，代表博客评论的```artcle```元素可嵌套在代表博客文章的```article```元素中。
> * ```article```元素的作者信息科通过```address```元素提供，但是不适用于嵌套的```article```元素。
> * ```article```元素的发布日期和时间可通过```time```元素的```pubdate```属性表示。

示例：
```html
<article>
        <header>
            <h2>标题</h2>
        </header>
        <section>
            <p>主要内容</p>
        </section>
        <section>
            <article>
                <p>用户评论</p>
                <footer>
                    <p>发表于 <time datetime="2016-03-16 21:00">March 16</time> by 游客</p>
                </footer>
            </article>
        </section>
        <footer>
            <p>发表于 <time datetime="2015-03-01 12:00">March 01</time> by 内容发布者</p>
        </footer>
</article>
```

##HTML strong标签和b标签区别
HTML5之前的版本中，```b```元素是视觉要素，指示浏览器以粗体显示其开始和结束标签之间的内容。HTML5不再提倡纯属呈现因素的元素，所以给b重新下了新定义。
> The b element now represents a span of text to be stylistically offset from the normal prose without conveying any extra importance, such as key words in a document abstract, product names in a review, or other spans of text whose typical typographic presentation is emboldened.

//```b```元素表示一段文字（将这段文字从周围文字凸显出来并不表示特别的强调或重要性），习惯上使用粗体呈现，其使用场合包括文章提要中的关键字或产品评论中的产品名称。意思就是```b```元素没有任何语义，只起呈现方面的作用。

HTML中```strong```元素也是HTML4.01中的元素，是表达要素，是语义更强的文本。在HTML5中```strong```表示HTML页面上的强调，为了表明是重点而加粗。从网站优化方面，规范的```strong```标签更容易被搜索引擎搜索到。


##HTML5 figure标签
HTML中```figure```标签代表一段独立的内容，经常与标题标签```<figcaption>```配合使用，并且作为一个独立的引用单元。这个标签经常包含引用在文章中的图片，插图，表格，代码段等，当这部分转移到附录中或者其他页面时不影响大纲。

示例：
```html
<figure>
    <img src="https://developer.cdn.mozilla.net/media/img/mdn-logo-sm.png" alt="MDN logo" />
    <figcaption>MDN logo</figcaption>
</figure>
```

##HTML table标签
HTML中为了让大表格```table```在下载的时候可以分段显示，因为浏览器解析HTML时，```table```是作为一个整体解释的，使用```tbody```可以优化显示，对```table```进行结构化的分层。如果表格很长，用```tbody```分段可以一部分一部分显示，不用等待整个表格都下载完成，而是下载一块显示一块。

> * ```thead```表格的头 用来放标题之类的东西
> * ```tbody```表格的身体 放数据本体
> * ```tfoot```表格的脚 放表格脚注之类的

##HTML5 aside元素
HTML```aside```元素中连接到页面中其他部分的内容，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。通常表现为侧边栏或者被插入到该内容里。比如工具条，广告，相关链接等。它定义```article```以外的内容，且```aside```的内容应该与```article```的内容相关。

示例：
```html
<article>
    <p>这个电影十分有名...</p>
    <aside>这个电影售卖$87 million</aside>
</article>
```

##HTML label标签
HTML中```label```标签为```input```元素定义标注（标记）。```label```元素不会向用户呈现任何特殊效果。不过它为鼠标用户改进了可用性。这样在```label```元素内点击文本，就会触发此控件。即当用户选择该标签时，浏览器会自动将焦点转到和标签相关的控件上。```label```标签的```for```属性应当与相关元素的```id```属性相同。

表示用户界面的一个条目的标题。它通常关联一个控件，或者将控件放置在```label```元素内，或者是用作其属性。这样的控制称作```label```元素的labeled control。

属性

|属性|值|描述|
|-----|---: |:---:|
|for|id|规定```label```绑定到哪个表单元素|
|form（HTML5）|formid|规定```label```字段所属的一个或多个表单（表单拥有者），<br>如果未指定此属性，```label```元素必须是```form```元素的后代。<br>应用此属性值，你可以将```label```元素放置在文档的任何位<br>置，而不仅仅是作为它的拥有者```form```元素的后代|

示例：

```html
//将表单控件作为标记的内容，隐式
<label>Click me <input type="text" id="user" name="Name" /></label>

//为label标签下的for属性命名一个目标id，显式
<label for="User">Click me</label><input type="text" id="User" name="Name" />
```

参考：

[MDN header](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header)

[MDN nav](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/nav)

[MDN main](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main)

[MDN footer](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer)

[HTML5 中 div section article 的区别](https://www.qianduan.net/html5-differences-in-the-div-section-article/)

[HTML5 中的b/strong，i/em有什么区别](https://www.zhihu.com/question/19551271)

[HTML元素b和strong有什么区别](https://www.zhihu.com/question/20961933)

[MDN figure](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figure)

[table标签中thead,tbody,tfoot的作用](http://www.dreamershop.com/info/n971c8.aspx)

[HTML label标签](http://www.w3school.com.cn/tags/tag_label.asp)

[MDN label](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/label)

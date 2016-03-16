##HTML5 section 标签
```section```定义文档中的区段，节。比如章节，页眉，页脚或文档中的其他部分。
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
|cite |URL |section的URL，假如section摘自web的话|

##HTML5 artical 标签
```artical```标签，是一个特殊的```section```标签。比```section```更具有明确的语义，代表一个独立的，完整（看这段内容脱离了所在语境还是否是完整的独立的）的相关内容块。一般来说```article```会有标题部分（通常包含在header内），包含footer。

定义外部的内容，外部的内容可以是来自一个外部的新闻提供者的一篇新的文章，或者来自blog的文本，或者来自论坛的文本等。   ---[W3School article标签](http://www.w3school.com.cn/html5/html5_article.asp)

```article```元素表示文档，页面，应用或网站中独立结构，其意在成为可独立分配的或可复用的结构。如在发布中，可能是论坛帖子，杂志或新闻文章，博客，用户提交的评论，交互式组件，或其他独立的内容项目。   ---[MDN article标签](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article)
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

```strong```元素也是HTML4.01中的元素，是表达要素，是语义更强的文本。在HTML5中```strong```表示HTML页面上的强调，为了表明是重点而加粗。从网站优化方面，规范的```strong```标签更容易被搜索引擎搜索到。


##HTML figure标签
```figure```标签代表一段独立的内容，经常与标题标签```<figcaption>```配合使用，并且作为一个独立的引用单元。这个标签经常包含引用在文章中的图片，插图，表格，代码段等，当这部分转移到附录中或者其他页面时不影响大纲。

示例：
```html
<figure>
    <img src="https://developer.cdn.mozilla.net/media/img/mdn-logo-sm.png" alt="MDN logo">
    <figcaption>MDN logo</figcaption>
</figure>
```

参考：

[HTML5 中 div section article 的区别](https://www.qianduan.net/html5-differences-in-the-div-section-article/)

[HTML5 中的b/strong，i/em有什么区别](https://www.zhihu.com/question/19551271)

[HTML元素b和strong有什么区别](https://www.zhihu.com/question/20961933)

[MDN figure](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figure)

[table标签中thead,tbody,tfoot的作用](http://www.dreamershop.com/info/n971c8.aspx)

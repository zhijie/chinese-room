> 

# 介绍 #

所有的wiki 页面都存储在项目仓库中/wiki 目录下的 .wiki文件中. 每一个文件的名字都和相应Wiki页面一样.  而且，每一个Wiki文件都包含可选的编译指示行(pragma lines),编译行后是页面内容.

# 编译指示(Pragmas) #

可选的编译指示行给页面提供了元数据和显示这些数据的方法.这些指示行只有在文件顶部时才会被编译. 编译指示行开头是井字符(#)和编译指示名，跟着是一个值.

| **Pragma**   | **Value**  |
|:-------------|:-----------|
| #summary     | One-line summary of the page |
| #labels      | Comma-separated list of labels (filled in automatically via the web UI) |
| #sidebar     | See [Side navigation](http://code.google.com/p/support/wiki/WikiSyntax#Side_navigation) |


# Wiki-style markup #

## 段落(Paragraphs) ##

使用一个或多个空行分隔段落.

## 字形(Typeface) ##

|**Name/Sample**   | **Markup**       |
|:-----------------|:-----------------|
|  _italic_        | `_italic_`       |
|  **bold**         | `*bold*`         |
|  `code`          | ```code```       |
|  `code`          | `{{{code}}}`     |
|  <sup>super</sup>script  | `^super^script`  |
|  <sub>sub</sub>script  | `,,sub,,script`  |
| ~~strikeout~~    | `~~strikeout~~`  |

你可以以某些方式混合使用这些字形:

|       **Markup**                    |        **Result**                 |
|:------------------------------------|:----------------------------------|
| `_*bold* in italics_`               | _**bold** in italics_             |
| `*_italics_ in bold*`               | **_italics_ in bold**             |
| `*~~strike~~ works too*`            | **~~strike~~ works too**          |
| `~~as well as _this_ way round~~`   | ~~as well as _this_ way round~~   |


## 代码(code) ##

你可以用多行代码定界符逐字显示多行代码块:

```
{{{ 
def fib(n): 
if n == 0 or n == 1: 
 return n 
else: 
 # This recursion is not good for large numbers. 
 return fib(n-1) + fib(n-2) 
}}} 
```

结果是这个样子:

```
def fib(n): 
if n == 0 or n == 1: 
 return n 
else: 
 # This recursion is not good for large numbers. 
 return fib(n-1) + fib(n-2) 
```

## 标题(Headings) ##

```
= 标题 = 
== 子标题 == 
=== 第3级 === 
==== 第4级 ==== 
===== 第5级 ===== 
====== 第6级 ====== 
```

## 分隔符(Dividers) ##

一行单独的四个或多个破折号可以成为水平分隔线.


## 列表(Lists) ##

Google Code wikis 支持项目符号列表和编号列表. 列表至少要缩进一个空格才能被识别. 依靠合适的缩进，你可以在列表中嵌套列表:

```
The following is: 
* A list 
* Of bulleted items 
 # This is a numbered sublist 
 # Which is done by indenting further 
* And back to the main bulleted list 

* This is also a list 
* With a single leading space 
* Notice that it is rendered 
# At the same levels 
# As the above lists. 
* Despite the different indentation levels. 
```

The following is:
**A list** Of bulleted items
  1. This is a numbered sublist
  1. Which is done by indenting further
**And back to the main bulleted list**

**This is also a list** With a single leading space
**Notice that it is rendered
# At the same levels
# As the above lists.** Despite the different indentation levels.

## 引用(Quoting) ##

块引用可以在页面中着重显示特殊的文本摘录. 可以使用一个以上的空格缩进实现块引用:

```
Someone once said: 

This sentence will be quoted in the future as the canonical example 
of a quote that is so important that it should be visually separate 
from the rest of the text in which it appears. 
```

Someone once said:

This sentence will be quoted in the future as the canonical example
of a quote that is so important that it should be visually separate
from the rest of the text in which it appears.

## 链接(Links) ##

链接对 Wiki 是极为重要的, 因为它们组成了网络内容. Google Code wiki 允许内部和外部链接, 而且在Wiki能够识别 Wiki关键词(WikiWord)或URL时，Wiki 会自动创建链接.

### 内部Wiki链接(Internal wiki links) ###

wiki的内部链接使用下面的语法. 如果你把Wiki链接到了不存在的页面, 这个链接就会出现一个 !小链接[?](WikiSyntax.md) ,链接到项目提交者或发起者.       点击那个链接就会到你输入页面内容的页面创建形式.

如果你尚未登录, wiki 会链接那一点到不存在的页面的纯文本形式, 而不是页面创建形式. 当你创建目标页面时,对于浏览者来说,这个链接就会成为一个正常的超链接
.

```
WikiSyntax is identified and linked automatically 

Wikipage is not identified, so if you have a page named [Wikipage] you 
need to link it explicitly. 

If the WikiSyntax page is actually about reindeers, you can provide a 
description, so that people know you're actually linking to a page on 
[WikiSyntax reindeer flotillas]. 

If you want to mention !WikiSyntax without it being autolinked, use an 
exclamation mark to prevent linking. 
```

WikiSyntax 会被自动识别和链接

Wikipage 没有被识别, 所以你可以有一个名为[Wikipage](Wikipage.md)的页面,你需要显式链接.

如果 WikiSyntax 页面事实上是关于驯鹿的, 你可以提供一个描述,这样的话大家就知道你要链接到关于
[驯鹿舰队(reindeer flotillas)](WikiSyntax.md)的页面.

如果你想用到 WikiSyntax 而不被自动链接, 在它前面加一个感叹号就可以了.

### 链接到页面内部的锚点 ###

每一个标题都定义了一个同名的 HTML 锚点, 但是其中的空格要用下划线代替. 你可以像这样链接到页面上的特定锚点:

```
[WikiSyntax#Wiki-style_markup] 
```

显示出来就是这样了: [WikiSyntax#Wiki-style\_markup](WikiSyntax#Wiki-style_markup.md).


### 链接到外部页面 ###

可以使用相似的语法从你自己的Wiki页面链接到外部网页:

```
像 http://www.google.com/ 或 ftp://ftp.kernel.org/ 这样的 URL 会被自动变成链接. 

当然也可以提供一些描述性文本. 比如, 下面的链接指向[http://www.google.com Google home page]. 

如果指向一个图片, 图片就会插入到页面中: 

http://code.google.com/images/code_sm.png 

也可以把图片做成链接, 只需把图片的 URL 放到链接描述的位置: 

[http://code.google.com/ http://code.google.com/images/code_sm.png] 
```

像 http://www.google.com/ 或 [ftp://ftp.kernel.org/](ftp://ftp.kernel.org/) 这样的 URL 会被自动变成链接.

当然也可以提供一些描述性文本. 比如, 下面的链接指向[Google home page](http://www.google.com).

如果指向一个图片, 图片就会插入到页面中:

![http://code.google.com/images/code_sm.png](http://code.google.com/images/code_sm.png)

也可以把图片做成链接, 只需把图片的 URL 放到链接描述的位置:

```
[http://code.google.com/ http://code.google.com/images/code_sm.png] 
```

[![](http://code.google.com/images/code_sm.png)](http://code.google.com/)


### 链接到图片 ###

如果你的链接指向一幅图片 (即以`.png`, `.gif`, `.jpg` 或 `.jpeg`结尾), 它就会最为图片插入到页面:

```
http://code.google.com/images/code_sm.png 
```

![http://code.google.com/images/code_sm.png](http://code.google.com/images/code_sm.png)

如果图片是由服务器端的脚本产生的, 你也许要在结尾添加一个没有意义的查询字符串参数,这样的话,URL 就是以支持的文件拓展名结尾了.

```
http://chart.apis.google.com/chart?chs=200x125&chd=t:48.14,33.79,19.77|83.18,18.73,12.04&cht=bvg&nonsense=something_that_ends_with.png 
```

![http://chart.apis.google.com/chart?chs=200x125&chd=t:48.14,33.79,19.77|83.18,18.73,12.04&cht=bvg&nonsense=something_that_ends_with.png](http://chart.apis.google.com/chart?chs=200x125&chd=t:48.14,33.79,19.77|83.18,18.73,12.04&cht=bvg&nonsense=something_that_ends_with.png)

## 表格(Tables) ##

表格是用`||`定界符输入每一个单元的内容做成的. 你可以在表格单元中插入别的内联Wiki语法, 包括自行格式化和链接.

```
|| *Year* || *Temperature (low)* || *Temperature (high)* || 
|| 1900 || -10 || 25 || 
|| 1910 || -15 || 30 || 
|| 1920 || -10 || 32 || 
|| 1930 || _N/A_ || _N/A_ || 
|| 1940 || -2 || 40 || 
```

| **Year** | **Temperature (low)** | **Temperature (high)** |
|:---------|:----------------------|:-----------------------|
| 1900     | -10                   | 25                     |
| 1910     | -15                   | 30                     |
| 1920     | -10                   | 32                     |
| 1930     | _N/A_                 | _N/A_                  |
| 1940     | -2                    | 40                     |








# HTML 支持 #
为了增加Wiki页面的表现力,有一些对 HTML 的支持. HTML 标记只在Wiki页面中有效,在评论中还不行.

HTML 语法可以和Wiki语法协同使用, 但是不提倡到处都这么用.<a href='Hidden comment: Also, avoid blank lines between list items.'></a>

目前支持下列HTML 标记和属性:

<table border='1'>
<thead><th>HTML Tag</th><th>Supported Attributes</th></thead>
<tbody>
<tr><td>a</td><td>title dir lang href</td></tr>
<tr><td>b</td><td>title dir lang</td></tr>
<tr><td>br</td><td>title dir lang</td></tr>
<tr><td>blockquote</td><td>title dir lang</td></tr>
<tr><td>code</td><td>title dir lang language <code>[1]</code></td></tr>
<tr><td>dd</td><td>title dir lang</td></tr>
<tr><td>div</td><td>title dir lang</td></tr>
<tr><td>dl</td><td>title dir lang</td></tr>
<tr><td>dt</td><td>title dir lang</td></tr>
<tr><td>em</td><td>title dir lang</td></tr>
<tr><td>font</td><td>title dir lang face size color</td></tr>
<tr><td>h1</td><td>title dir lang</td></tr>
<tr><td>h2</td><td>title dir lang</td></tr>
<tr><td>h3</td><td>title dir lang</td></tr>
<tr><td>h4</td><td>title dir lang</td></tr>
<tr><td>h5</td><td>title dir lang</td></tr>
<tr><td>i</td><td>title dir lang</td></tr>
<tr><td>img</td><td>title dir lang src alt border height width align</td></tr>
<tr><td>li</td><td>title dir lang</td></tr>
<tr><td>ol</td><td>title dir lang type start</td></tr>
<tr><td>p</td><td>title dir lang align</td></tr>
<tr><td>pre</td><td>title dir lang</td></tr>
<tr><td>q</td><td>title dir lang</td></tr>
<tr><td>s</td><td>title dir lang</td></tr>
<tr><td>span</td><td>title dir lang</td></tr>      <tr><td>strike</td><td>title dir lang</td></tr>      <tr><td>strong</td><td>title dir lang</td></tr>
<tr><td>sub</td><td>title dir lang</td></tr>
<tr><td>sup</td><td>title dir lang</td></tr>
<tr><td>table</td><td>title dir lang align valign cellspacing cellpadding border width height</td></tr>
<tr><td>tbody</td><td>title dir lang align valign cellspacing cellpadding border width height</td></tr>
<tr><td>td</td><td>title dir lang align valign cellspacing cellpadding border width height</td></tr>
<tr><td>tfoot</td><td>title dir lang align valign cellspacing cellpadding border width height</td></tr>
<tr><td>th</td><td>title dir lang align valign cellspacing cellpadding border width height</td></tr>
<tr><td>thead</td><td>title dir lang align valign cellspacing cellpadding border width height colspan rowspan</td></tr>
<tr><td>tr</td><td>title dir lang align valign cellspacing cellpadding border width height colspan rowspan</td></tr>
<tr><td>tt</td><td>title dir lang</td></tr>
<tr><td>u</td><td>title dir lang</td></tr>
<tr><td>ul</td><td>title dir lang type</td></tr>
<tr><td>var</td><td>title dir lang</td></tr>      </tbody>
</table>

`[1]` 代码标记的语言属性是代码块中使用语言的文件拓展名. 这被用作语法亮显的暗示.

## 转义(Escaping)HTML Tags ##

当你想直接在Wiki页面中显示html标记时(而不是被解释), 你需要转义每一个HTML标记.

HTML标记可以像下面表格中显示的那样转义:
<table border='1'>
<thead><th>Markup</th><th>Result</th></thead>
<tbody>
<tr><td> <code>`&lt;hr&gt;`</code></td><td><code>&lt;hr&gt;</code></td></tr>
<tr><td> <code>{{{&lt;hr&gt;}}}</code></td><td><code>&lt;hr&gt;</code></td></tr>
</tbody>
</table>

<br />

# 评论(Comments) #

wiki 为帮助解释Wiki页面的内容支持嵌入式的评论. 评论内容中所有的东西都都从被解释(rendered) 的页面中移除了, 但当编辑或查看页面源码是可见的.

```
<wiki:comment> 
This text will be removed from the rendered page. 
</wiki:comment> 
```

# 小工具(Gadgets) #

你可以用下面的语法在你的Wiki页面中嵌入[小工具](http://www.google.com/webmasters/gadgets/):

```
<wiki:gadget url="http://example.com/gadget.xml" height="200" border="0" />  
```

有效的属性有:
**`url`: 小工具的 URL** `width`: 小工具的宽度
**`height`: 小工具的宽度** `title`: 小工具上方显示的标题
**`border`: "0" 或 "1", 是否要在小工具周围画边框** `up_*`: 小工具的用户喜欢的参数
**`caja`: "0" 或 "1", 是否使用 Caja 渲染小工具. [Caja](http://code.google.com/p/google-caja) 帮助用户不受恶意或第三方小工具的错误的损害.**

使用小工具(WorkingWithGoogleGadgets) 说明了如何为Google Code创建小工具. 那儿也提了几条关于如何更方便地发布小工具和在Google其他产品(例如 iGoogle)中的整合小工具的建议.

有趣的小工具(InterestingDeveloperGadgets) 展出一些可以包含到你的项目页面中的小工具样例.

# 视频(Videos) #

你可以用下面的语法嵌入视频:

```
<wiki:video url="http://www.youtube.com/watch?v=3LkNlTNHZzE"/> 
```

有效地参数有:
**`url`: 视频文件的 URL** `width`: 视频宽度
**`height`: 视频高度**

现在我们支持来自 Youtube 和 Google Video 的视频, 但是别的容器可以添加到[开源小工具计划](http://code.google.com/p/google-code-project-hosting-gadgets/source/browse/#svn/trunk/video).

# 导航(Navigation) #
## 内容目录(Table of Contents) ##

一个内联的内容目录可以从页面标题中产生. 添加下面的语句到页面中要显示内容目录的地方:

```
<wiki:toc max_depth="1" /> 
```

有效地参数是:
**`max_depth`: 要显示的内容目录的最大深度**

## 侧边导航(Side navigation) ##

你可以使用另外一个Wiki页面来给指定侧边栏. [doctype project](http://code.google.com/p/doctype/wiki/Articles) 在Wiki中大量使用了侧边栏.

添加侧边栏的一种方法是像下面一样设定#sidebar 编译指示符. 另外, 如果不想要侧边导航,sidebar 编译指示可以空白.

| #sidebar TableOfContents |
|:-------------------------|

定义的侧边导航要像下面一样使用简单的列表.

```
* [Articles HOWTO articles] 
 * [ArticlesXSS Web security] 
 * [ArticlesDom DOM manipulation] 
 * [ArticlesStyle CSS and style] 
 * [ArticlesTips Tips and tricks] 
* [DOMReference DOM reference] 
* [HTMLElements HTML reference] 
* [CSSReference CSS reference] 
```

也可以在Administer->tab为所有页面设定默认的导航页. 如果同时指定了 #sidebar 编译指示编译指示会优先显示.

# Wiki内容的本地化 #

除了在Administer->tab中为Wiki设定的默认语言外,别的语言也是支持的. 如果有多于一种语言在用户偏爱的语言(例如 浏览器使用的语言)的基础上, Wiki会尝试提供合适的语言. 如果没有那种语言的Wiki页面, Wiki会使用默认语言. 不过评论在各种语言版本的页面中是共享的.

网页新的翻译不能通过web界面添加,而必须通过版本控制仓库(Subversion repository).

要添加一种翻译的页面,先要从Subversion检出(checkout)wiki: <br />
`svn checkout https://`<b>yourproject</b>`.googlecode.com/svn/wiki/` <b>yourdirectory</b> `-username` <b>yourusername</b>

然后在 /wiki/ 下创建一个新的目录,新目录的名字要使用两个字符的 ISO-639 编码. 把所有的译文都放进新的文件夹,然后把这些改变提交(submit)到代码控制仓库(Subversion repository).

下面是有效Wiki目录的一个例子:
```
wiki/ 
ja/ 
   ProjectHistory.wiki 
   StyleGuide.wiki 
zh-Hans/ 
   ProjectHistory.wiki 
   StyleGuide.wiki 
zh-Hant/ 
   ProjectHistory.wiki 
   StyleGuide.wiki 
ProjectHistory.wiki 
StyleGuide.wiki 
```

在这些文件提交到项目的版本控制仓库中后, 就可以通过Wiki的web编辑器编辑了. 灵活仓库(Mercurial repositories)是一样的, 唯一的不同是Wiki在根目录下而不是 `https://wiki.`<b>yourproject</b>`.googlecode.com/hg/` 的 wiki/ 下.

注意: wiki 接受 ISO-639 的两字语言编码的这样一个子集, 在这个子集中的一些编码(比如 zh\_Hans)包含本地特定的编码. 这些本地特定的编码要使用一个连字符(zh-Hans). 一些示例语言编码在下面的表格中指定了.

<table border='1'>
<tbody><tr>
<th> Language (Locale)</th>
<th> Directory Name<br>
</th>
</tr>
<tr>
<td>Arabic</td>
<td>ar</td>
</tr>
<tr>
<td>Bulgarian</td>
<td>bg</td>
</tr>
<tr>
<td>Chinese (China)</td>
<td>zh-Hans</td>
</tr>
<tr>
<td>Chinese (Taiwan)</td>
<td>zh-Hant</td>
</tr>
<tr>
<td>Croatian</td>
<td>hr</td>
</tr>
<tr>
<td>Czech</td>
<td>cs</td>
</tr>
<tr>
<td>Danish</td>
<td>da</td>
</tr>
<tr>
<td>Dutch</td>
<td>nl</td>
</tr>
<tr>
<td>English (United Kingdom)</td>
<td>en-GB</td>
</tr>
<tr>
<td>English (United States)</td>
<td>en-US</td>
</tr>
<tr>
<td>Finnish</td>
<td>fi</td>
</tr>
<tr>
<td>French</td>
<td>fr</td>
</tr>
<tr>
<td>German</td>
<td>de</td>
</tr>
<tr>
<td>Greek</td>
<td>el</td>
</tr>
<tr>
<td>Hebrew</td>
<td>he</td>
</tr>
<tr>
<td>Hungarian</td>
<td>hu</td>
</tr>
<tr>
<td>Italian</td>
<td>it</td>
</tr>
<tr>
<td>Japanese</td>
<td>ja</td>
</tr>
<tr>
<td>Korean</td>
<td>ko</td>
</tr>
<tr>
<td>Norwegian</td>
<td>no</td>
</tr>
<tr>
<td>Polish</td>
<td>pl</td>
</tr>
<tr>
<td>Portuguese (Brazil)</td>
<td>pt-BR</td>
</tr>
<tr>
<td>Romanian</td>
<td>ro</td>
</tr>
<tr>
<td>Russian</td>
<td>ru</td>
</tr>
<tr>
<td>Slovak</td>
<td>sk</td>
</tr>
<tr>
<td>Spanish</td>
<td>es</td>
</tr>
<tr>
<td>Swedish</td>
<td>sv</td>
</tr>
<tr>
<td>Turkish</td>
<td>tr</td>
</tr>
</tbody></table>

The content on this page created by Google is licensed under the Creative Commons Attribution 3.0 License. User-generated content is not included in this license.
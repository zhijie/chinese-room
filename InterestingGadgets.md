# Google Code 上使用的开发小工具 #

谷歌代码项目托管(Google Code Project Hosting) wiki 支持小工具,这样你可以在Wiki页面中引入第三方站点的数据. 这是我们认为有用的几个小工具.

这些工具有以下特点:
  1. 它们定向的用户群是开发人员和开源项目.
  1. 它们提供了项目深层次的信息,这些信息不说出来就很难了解到的.
  1. 它们可以被限定为特定的项目.

如果你有一些符合这些条件的小工具, 请在我们的support group 中说一声,我们会很高兴地展示它们. 也可以查看 [项目托管小工具](http://code.google.com/p/google-code-project-hosting-gadgets/)搜索更多你可以使用的小工具.

**如何使用这些小工具**

如果你想把其中的小工具放到Wiki页面或项目主页, 使用新的 `<wiki:gadget...>` 语法. 下面的每一个例子都有小片代码,你可以直接拷贝粘帖使用.

## Math ML ##
你可以使用一个小工具显示数学公式.

**小工具**
<wiki:gadget url="http://mathml-gadget.googlecode.com/svn/trunk/mathml-gadget.xml" border="0" up\_content="root3x + x^phi + x\_1"/>

**代码**

`<wiki:gadget url="http://mathml-gadget.googlecode.com/svn/trunk/mathml-gadget.xml" border="0" up_content="root3x + x^phi + x_1"/>`

## Google Code ##

你可以使用一个小工具显示任何有 Atom 或 RSS 订阅的博客.

**小工具**
<wiki:gadget url="http://google-code-feed-gadget.googlecode.com/svn/build/prod/feedgadget/feedgadget.xml" up\_feeds="http://googlecode.blogspot.com/atom.xml" up\_gadgetTitle="Featured Projects" width="500px" height="340px" border="0"/>

**代码**

`<wiki:gadget url="http://google-code-feed-gadget.googlecode.com/svn/trunk/gadget.xml" up_feeds="http://google-code-featured.blogspot.com/atom.xml"  width="500px" height="340px" border="0"/>`

把`up_feeds` URL 替换成你的博客的 XML 订阅.  你过你有多个项目博客, 你可以列出多个 URL,URL之间用 '|'分隔.



## MarkMail ##
[MarkMail](http://markmail.org) 是一个搜索邮件列表档案的免费服务. 如果你有一个项目论坛,这些工具会非常有用. 下面是一个 google-web-toolkit 论坛的例子.

**小工具**

&lt;wiki:gadget url="http://markmail.org/gadgets/markmailmini.xqy?l=google-web-toolkit" width="500px" height="340px" border="1"/&gt;

**代码**

`<wiki:gadget url="http://markmail.org/gadgets/markmailmini.xqy?l=google-web-toolkit"/>`

你可以通过修改URL中的参数定制这个小工具, 或者使用[MarkMail Gadget Builder](http://markmail.org/gadgets/builder/). 关于搜索语法的更多信息, 请参考[MarkMail FAQ](http://markmail.org/docs/faq.xqy#searchsyntax).

## Ohloh ##
[Ohloh.net](http://ohloh.net) 为开源开发者提供了一个开发源码软件目录和各种社区功能. 下面是 使我们链接到一些 Ohloh 小工具.

注意: 所有这些都是[Google Web 工具箱](http://code.google.com/p/google-web-toolkit)的示例. 要给你的项目找小工具, [搜索](http://www.ohloh.net/projects/search) Ohloh.net, 到项目页, 再点击小工具链接.

### 统计器(Stats) ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_basic\_stats.xml" height="220" border="1"/&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_basic_stats.xml" height="220" border="1" />`

### 仿真陈述(Factoids) ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_factoids.xml" width="340" height="170" border="0" /&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_factoids.xml" width="340" height="170" border="0" />`

### 项目语言(Project Languages) ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_languages.xml" width="340" height="200" border="1" /&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_languages.xml" width="340" height="200" border="1" />`

### 项目费用(Project Cost) ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_cocomo.xml" height="250" border="0" /&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_cocomo.xml" height="250" border="0" />`

### I Use It ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_users.xml" height="100" border="0" /&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_users.xml" height="100" border="0" />`

### 合伙人徽章(Partner Badge) ###

**小工具**

&lt;wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project\_partner\_badge.xml" height="55" border="0" /&gt;

**代码**

`<wiki:gadget url="http://www.ohloh.net/p/gwt/widgets/project_partner_badge.xml" height="55" border="0" />`
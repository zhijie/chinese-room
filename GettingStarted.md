Project Hosting on Google Code 为开源提供了一个自由协作的开发环境. 每一个项目都有自己的维护人员控制、版本控制或灵活仓库(Subversion/Mercurial repository), 议题跟踪(issue tracker), 维基百科页面(wiki pages), 和下载板块(downloads section). 我们的项目维护服务(Our project hosting service)简单、快捷、可靠、可拓展, 这样一来, 你就可以专心做开源开发了.

这个指南提供了一下信息:



## 贡献开放代码 ##

在建立新的项目之前, 请[搜索](http://code.google.com/hosting/)在本站或网络上任何别的地方已经存在的项目. 最好能帮助做已存在的项目,而不是自己从头做起,
以免重复劳动.

**去[Project Hosting 的主页](http://code.google.com/hosting/)搜索已有项目([如何参加已有项目](http://code.google.com/p/support/wiki/HowToJoinAProject))** 去[创建项目](http://code.google.com/hosting/createProject)页面填写表格. 记住, 挑一个好的标签(查看[Project Hosting 主页](http://code.google.com/hosting/)参考例子).
  * [如何选择许可证](http://opensource.org/licenses/category).
  * [如何选择版本控制系统](ChoosingAVersionControlSystem.md).

## 项目工作 ##

### 定制你的项目 ###

使用 管理员(**Administer**) 标签定制项目. 这个标签只对项目所有者可见(project owners). 下列子标签在创建新项目时是有用的:
**项目概要(**Project Summary**) 子标签 -- 你可以修改一些在创建时设置的选项, 包括建立博客(blogs), 分析学(analytics), 和自定义的项目标志(logo). 这也给项目提供了另外一个建立标签的机会,这有助于别人找到你的项目.** 项目成员(**Project Members**) 子标签 -- 你在项目中可以添加新的拥有者(owners)或提交者(committers).
**源码(**Source**) 子标签 -- 你可以选择非项目组成员修改代码.**

你可能想为提交和议题的改变的通告建立邮件列表. 邮件让项目成员和其他人随时知道可能影响自己的代码的变化. 要建立邮件列表,按照下面的步骤:
# 如果你要创建邮件列表,也许想用[Google Groups](http://groups.google.com/).
# 添加 `(your-project-name)@googlecode.com` 作为所有邮件列表成员接收通告的海报(poster).
# 在你的项目中,点击管理员(**Administer**) 标签.
# 点击 源码(**Source**)子标签.
# 在活动通知区(**Activity notifications**), 输入接收所有提交(**All commits**)通知的邮件列表名,点击保存(**Save Changes**).
# 点击 议题跟踪(**Issue Tracking**)子标签.
# 在活动通知区(**Activity notifications**), 输入接收所有议题改变通知(**All issue changes**)消息的邮件列表名,点击保存(**Save Changes**).

### 操作代码仓库 ###

每个项目都有自己的[版本控制(Subversion)](http://subversion.tigris.org/)或[灵活(Mercurial)](http://www.selenic.com/mercurial/)仓库.
**[了解更多](http://svnbook.red-bean.com/)关于版本控制(Subversion).** [了解更多](http://hgbook.red-bean.com/)关于灵活(Mercurial).

执行下面的操作来检入和检出源码仓库的代码(check code in and out):

# 想查看在命令行下检出项目代码仓库的操作说明,去源码(**Source**)标签下. 任何人,不论他们有没有Google account, 都能匿名检出和浏览代码仓库, 同时项目拥有者和提交者有全部的读写权限. 你可以在[管理员(\*Administer\*)标签](#Customizing_your_Project_on_the_Administer_Tab.md)下添加拥有者(owner)和提交者(committer).
# 如果你计划同步已有的代码库,你\*必须\*在改变项目代码库之前 点击在源码(**Source**)标签页最下端的重置这个代码库(**Reset This Repository**)链接. **这包括创建新的Wiki页面** 因为重置代码库会导致Wiki内容丢失. 在完成这一不值钱不要开始写Wiki页.

在你的项目进行一段时间后, 源码标签(**Source**)下的这几个子标签迟早会有用:

**浏览(**Browse**) 子标签 -- 可以及时浏览你的项目下已存在的文件和目录.** 变化(**Changes**) 子标签 -- 列出代码库已进行的改变. 也可以使用这个子标签进行任何改变的代码审查.

### 给项目写文档 ###

你可以使用维基百科(**Wiki**)标签下的功能给项目创建Wiki页. 我们的Wiki语法是受MoinMoin wiki 语法的启发而来的, 或多或少是它的一个子集. 我们发现MoinMoin 是最流行的开源 wikis 之一,它为用户提供了一个简洁的语法.

按照下面的操作来创建 Wiki:

# 在项目中点击维基(**Wiki**)标签.
# 点击新建页面(**New page**)子标签.
# 输入页面名字(**Page Name**). 这个值必须是字母数字的,而且能有空格. 之后你不能在改变这个名字, 所以请谨慎些.
# 在内容(**Content**)区域输入文字和语法. [了解更多](WikiSyntax.md)关于Wiki语法的内容.
# 点击一个标签(**Labels**)域来查看可用的标签. 标签帮助用户决定这个Wiki页面对用户有多大作用.
# 点击预览(**Preview**), 保存(**Save page**), 或舍弃(**Discard**).

### 跟踪项目工作 ###

议题(**Issues**)标签是掌握项目进行中的特点、任务和错误的很好的方法. 它允许多个项目成员了解别人当前在做什么.

在你点击新建议题(**New issue**)子标签后, 请注意标签(**Labels**)域. 标签是对项目成员有意义的字符串. 当一个议题标签包含波折号时, 例如`Priority-Medium`, 可以把它理解成你可以在这儿使用一个键-值对.

**破折号的前缀是键.** 第一个破折号后的部分是值.

你可以配置议题列表显示所有前缀. 也可以使用"前缀:后缀"(`prefix:value`)搜索在自定义的域下的值.

### 发布共享 ###

当你准备好了发表代码, 你可以使用下载(**Downloads**)标签上传压缩文件. 别人就可以去你的项目的这个标签下下载使用.

在上传之前想好文件名字. 文件名会成为 URL 的一部分, 而且之后不能改变. 最好在后来发布的所有可能会变化的文件的名字中加入版本号.

虽然我们建议你把旧版本的发布标记成“弃用”(`deprecated`), 你也可以从下载删除(**Downloads**)标签删除文件: 点击有要删除的文件名的那一行(不是文件链接)进入下载详细说明页面,然后点击删除('Delete').

## 寻求更多帮助 ##

对于一般的问题, 请查看[FAQ](FAQ.md) wiki . 如果你有尚未回答的问题, 请把它放到[Google Group](http://groups.google.com/group/google-code-hosting).
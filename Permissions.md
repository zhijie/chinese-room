# 怎样配置你的项目权限 #

# 介绍 #

| **Important:**  Google Code only hosts open source projects. <br> The permissions customizations described here not sufficient for hosting proprietary software development projects. </tbody></table>


<br>
<br>
<br>

---


在开放源码软件开发中, 任何人都可以进入项目的源代码中
. 而且, 希望它的开发过程是透明的,允许任何人访问所有问题和项目文件.
透明性允许潜在用户或者贡献者自学和评估项目的状态.
透明性应该成为几乎所有项目在任何时间的规则.
该规则的例外是罕见的但重要的,
尤其是在大型的,非常活跃的项目.

大多数项目业主将永远不再需要配置他们项目的权限.相反,它通常最好的方法就是给项目中的每个人
一个提交者的角色, 并且用简单明了的语言来描述他们想要的职责.  某人在这个事情中犯了一些错误,
最好是在这之后撤销那些改变,
而不是在那之前通过给每个人配置很小的权限来限制他们.


<br>
<hr />

<h1>快速开始</h1>

这里是当你处理特殊情况时或许需要设定权限的按部就班的指导.<br>
如果这些没有一个适合你,那么你或许对你的权限不需要做任何事情.<br>
<br>
<br>
<h2>如何追踪现有的安全漏洞问题?</h2>

有时,在纰漏问题的详细信息之前,你可能需要关闭工作的安全漏洞.<br>
然而, 请记住,潜在的攻击者可能已经独立的发现了这些相同的资料.<br>
<br>
如果这个问题已经被进入:<br>
<ol><li>标记这个问题 <code>限制-查看-提交</code></li></ol>

这将限制进入这个问题，只有那些已经拥有权限的用户才能提交这个项目的源代码.<br>
但是, 要警惕,一些人可能已经看到了这个问题, 而且正在输入的电子邮件通告可能已经发送到项目邮件列表 (如果你配置了这个).<br>
未来问题的电子邮件通告的改变,将只会发送到那些有权限查看问题的用户.<br>
<br>
如果这个问题非常的敏感以至于只有提交者的一部分才能访问,<br>
那么使用一个标签,例如 <code>限制-查看-核心团队</code>.<br>
请参阅下面的细节参考部分.<br>
<br>
<h2>如何设定未来的安全漏洞问题?</h2>


<h1>Details</h1>

Add your content here.  Format your content with:<br>
<ul><li>Text in <b>bold</b> or <i>italic</i>
</li><li>Headings, paragraphs, and lists<br>
</li><li>Automatic links to other wiki pages
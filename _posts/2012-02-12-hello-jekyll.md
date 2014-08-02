---
layout: post
title: 用Jekyll来做博客
categories:
- Technology
tags:
- Jekyll
- Markdown
- 网站
---
我用github的Jekyll来编译网站，太方便了。Yihui的博客介绍为什么他用这个做博客。


    Jekyll完全推翻了传统网站的维护方式，它直接回到了“原点”——作者只需要维护文本文件，每一篇日志就是一个文件，程序会根据模板设置自动把这些文本文件翻译为网页。这些文本文件不用HTML，而是用简化版本的Markdown（MD）或者其它可最终翻译为HTML的伪标记语言。MD的哲学深得我心：把[语法](http://daringfireball.net/projects/markdown/)简化90%，去实现大多数常用的HTML标签，牺牲少数不常用的标签（这些标签仍然可以用原始的HTML代码写）。比如要写无序列表的话，在HTML里面要用

{% highlight html %}
<ul>
  <li>hello</li>
  <li>world</li>
</ul>
{% endhighlight %}

    每一项列表项都用`li`标签围起来，而在MD语法里，只需要一行一行写就行了，每一行开头写一个减号 `-` 就足够，就像自己记笔记一样：

{% highlight text %}
- hello
- world
{% endhighlight %}

    一个字符（确切地说是两个，后面还得跟个空格）和一串要重复敲的字符比，哪个简洁显而易见。简洁的MD语法配合几项YAML设置就是一篇日志，扔进Liquid模版系统，Jekyll就把网站编译出来了。



    使用Jekyll的另一大动力当然是GitHub，它提供编译服务，所以用户只需要用GIT管理文本文件就可以了。要写日志就新建一个文本文件，写完推上去完事，由于GIT支持离线工作，随时随地都可以写，不受网络环境限制。


    日志页面中支持键盘左右方向键或JK键前后导航，这是JavaScript实现的，归功于[Tao Zhang](http://ztpala.com/2012/01/16/jquery-keyboard-navigation/)。文章[RSS订阅](/cn/feed/)依然存在，所有日志的链接也没有变化，只是评论RSS变了，要么订阅[整站评论](http://yihui.disqus.com/latest.rss)，要么订阅单篇文章评论（每个页面的底部）。

我十分赞同。

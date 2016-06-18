---
layout: post
title: Web版上线啦！
permalink: /web-edition/
---

排版良好的PDF确实比较有书的气息，对大多数人来说，随时随地就能打开的网页显然更方便吧。

Web版真是久等了！《一瓶论语》的源代码是LaTeX，直接生成的是[PDF](https://github.com/abolybook/aboly/releases)电子书。Web版是从LaTeX自动转换来的，除了载体不同而作的一点点处理以外，它和PDF版的内容完全一致，并会保持同步更新。

点击[主页](http://www.abolybook.org)的两张封面图片，就分别进入《一瓶论语》和《论语》白文版：

<div style="overflow: auto; width: 100%; margin-bottom: 1.5em;">
<a href="/aboly/" title="《一瓶论语》"><img src="/img/abolycover.png" alt="《一瓶论语》" width="48%" style="display: block; float: left"/></a>
<a href="/ly/" title="《论语》白文版"><img src="/img/lycover.png" alt="《论语》白文版" width="48%" style="display: block; float: right"/></a>
</div>

（如果你是Windows XP用户，建议安装[Firefox浏览器](http://www.firefox.com.cn/)，用它看得更清爽哦。）

因为内容里有很多交叉引用，目前又租不起独立的服务器，所以《一瓶论语》和《论语》白文版都放在单个页面上。《一瓶论语》的页面有1 MB之巨，幸好传输时会被压缩到300 KB左右，加载起来也不会很慢。如果是用内存较小的手机阅读，刚开始可能有些迟钝。

中文网页不方便像PDF那样使用很多字体，所以就改成了不同的颜色。后面还会继续改善它的设计，让尽可能多的人都用得上。

网页当然比PDF灵活很多，即使是静态页面，也可以尝试各种效果。目前优先照顾手机阅读的方便，用各种配置的设备都能大体舒适地阅读才好，所以只在顶层导航条添加了4个按钮，从左到右是：

{: .center}
![目录](/img/web-edition/navbar.png)

- **留言**，跳转到[留言](/ideas/)区，可以在那里发表评论，参与讨论。
- **转转**，随机跳到某一章，便于刷新印象。
- **目录**。
- **设置**。

“目录”按钮显示章节标题的下拉菜单。考虑到网页浏览的便利，我调整了Web版的章节顺序，把不太重要的“前言”和“使用说明”移到“主题索引”之后：

{: .center}
![目录](/img/web-edition/outline-menu.png)

点击菜单标题，就跳转到内文的对应位置。点击标题右边的∨形，就展开次级目录，还可以点击∧形返回上一级：

{: .center}
![次级目录](/img/web-edition/outline-submenu.png)

“设置”菜单里的“显示章号”，用来切换是否显示每一章右上角的标号（PDF版的标号放在每一章之外的左上角）。其它3项跳转到相应的网址。

{: .center}
![目录](/img/web-edition/toggle-settings.png)

根据我的试验，在这样体积的页面上增加动态效果，一般配置的手机处理起来会比较缓慢。所以采取两条路线：

- 今天上线的Web版，目标是在大部分智能手机上流畅地阅读（如果安装了Chrome浏览器，也许效果更好），今后也会越变越轻快。
- 此外还将增加一个“高配置”Web版，适合使用电脑或者高端手机、Pad阅读。它会加上我理想中当然要有、但又不得不放弃了的所有阅读便利。

{: .center}
欢迎支招，敬请期待！:blush:


<div id="disqus_thread"></div>
<script>
    var disqus_config = function () {
        this.page.url = "http://www.abolybook.org/web-edition/";  // Replace PAGE_URL with your page's canonical URL variable
        this.page.identifier = "abolybook_web_edition"; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    (function() {  // DON'T EDIT BELOW THIS LINE
        var d = document, s = d.createElement('script');
        
        s.src = '//abolybook.disqus.com/embed.js';
        
        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>

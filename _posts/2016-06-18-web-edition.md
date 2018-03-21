---
layout: post
title: Web版上线啦！
permalink: /web-edition
---

排版良好的PDF比较有书的气息，可对大多数人来说，随时随地就能打开的网页显然更方便吧。

Web版真是久等了！《一瓶论语》的源代码是LaTeX，直接生成的是[PDF](https://github.com/abolybook/aboly/releases)电子书。Web版是从LaTeX自动转换来的，除了载体不同的必要处理以外，它和PDF版的内容基本一致，只是更新得频繁一点。

点击[主页](http://www.abolybook.org)的两张封面图片，就分别进入《一瓶论语》和《论语》白文版：

<script>
/*! Image Map Resizer (imageMapResizer.min.js ) - v0.6.2 - 2016-06-16
 *  Desc: Resize HTML imageMap to scaled image.
 *  Copyright: (c) 2016 David J. Bradshaw - dave@bradshaw.net
 *  License: MIT
 */
!function(){"use strict";function a(){function a(){function a(a){function c(a){return a*b[1===(d=1-d)?"width":"height"]}var d=0;return a.split(",").map(Number).map(c).map(Math.floor).join(",")}for(var b={width:l.width/m.width,height:l.height/m.height},c=0;j>c;c++)i[c].coords=a(k[c])}function c(){var b=null,c=null;m.onload=function(){b=l.width,c=l.height,(b!==m.width||c!==m.height)&&a()},l.onload=function(){null!==b&&l.width!==b&&a()},m.src=l.src}function d(){function c(){clearTimeout(n),n=setTimeout(a,250)}b(l,"load",a),b(window,"resize",c),b(window,"focus",a),b(window,"readystatechange",a),b(document,"fullscreenchange",a)}function e(a){return a.coords.replace(/ *, */g,",").replace(/ +/g,",")}function f(){return"function"==typeof h._resize}function g(){h._resize=a,i=h.getElementsByTagName("area"),j=i.length,k=Array.prototype.map.call(i,e),l=document.querySelector('img[usemap="#'+h.name+'"]'),m=new Image}var h=this,i=null,j=null,k=null,l=null,m=null,n=null;f()?h._resize():(g(),d(),c())}function b(a,b,c){"addEventListener"in window?a.addEventListener(b,c,!1):"attachEvent"in window&&a.attachEvent("on"+b,c)}function c(){function b(b){if(!b.tagName)throw new TypeError("Object is not a valid DOM element");if("MAP"!==b.tagName.toUpperCase())throw new TypeError("Expected <MAP> tag, found <"+b.tagName+">.");a.call(b)}return function(a){switch(typeof a){case"undefined":case"string":Array.prototype.forEach.call(document.querySelectorAll(a||"map"),b);break;case"object":b(a);break;default:throw new TypeError("Unexpected data type ("+typeof a+").")}}}"function"==typeof define&&define.amd?define([],c):"object"==typeof exports?module.exports=c():window.imageMapResize=c(),"jQuery"in window&&(jQuery.fn.imageMapResize=function(){return this.filter("map").each(a).end()})}(),function(){Array.prototype.map||(Array.prototype.map=function(a){"use strict";if(void 0===this||null===this||"function"!=typeof a)throw new TypeError;for(var b=Object(this),c=b.length>>>0,d=new Array(c),e=arguments.length>=2?arguments[1]:void 0,f=0;c>f;f++)f in b&&(d[f]=a.call(e,b[f],f,b));return d}),Array.prototype.forEach||(Array.prototype.forEach=function(a){"use strict";if(void 0===this||null===this||"function"!=typeof a)throw new TypeError;for(var b=Object(this),c=b.length>>>0,d=arguments.length>=2?arguments[1]:void 0,e=0;c>e;e++)e in b&&a.call(d,b[e],e,b)})}();

window.onload = function() {
    imageMapResize("#abolycovermap");
}
</script>

<div style="overflow: auto; width: 100%; margin-bottom: 1.5em;">
<a href="/aboly" title="《一瓶论语》"><img src="/img/abolycover.png" usemap="#abolycovermap" alt="《一瓶论语》" width="48%" style="display: block; float: left"/></a>
<a href="/ly" title="《论语》白文版"><img src="/img/lycover.png" alt="《论语》白文版" width="48%" style="display: block; float: right"/></a>
</div>

（如果你是Windows XP用户，建议安装[Firefox浏览器](http://www.firefox.com.cn/)，用它看得更清爽。）

[2016-7-8更新] 点击《一瓶论语》封面思维导图的节点，可以跳转到对应的主题索引。

因为内容里有很多交叉引用，目前又租不起独立的服务器，所以《一瓶论语》和《论语》白文版都放在了单个页面上。《一瓶论语》的页面有1 MB之巨，幸好传输时会被压缩到300 KB左右，加载起来也不会很慢。如果是用内存较小的手机阅读，刚开始也许会有些迟钝。

网页不方便像PDF那样使用很多字体，所以就改成了不同的颜色。后面还会继续改善它的设计，让尽量多的人都用得上。

网页比PDF灵活很多，即使是静态页面，也可以尝试各种效果。目前优先照顾手机阅读的方便，用各种配置的设备都能大体舒适地阅读才好，所以只在顶层导航条添加了4个按钮，从左到右是：

{: .center}
![目录](/img/web-edition/navbar.png)

- **转转**，随机跳到某一章，便于刷新印象。
- **留言**，跳转到[留言](/ideas)区，可以在那里发表评论，参与讨论。
- **目录**。
- **设置**。

“目录”按钮显示章节标题的下拉菜单。考虑到网页浏览的便利，Web版的章节顺序作了调整，把不太重要的“前言”和“使用说明”移到“主题索引”之后：

{: .center}
![目录](/img/web-edition/outline-menu.png)

点击菜单标题，就跳转到内文的对应位置。点击标题右边的∨形，就展开次级目录，然后可以点击∧形返回上一级：

{: .center}
![次级目录](/img/web-edition/outline-submenu.png)

“设置”菜单里的“显示章号”，用来切换是否显示每一章右上角的序号（PDF版的章号放在每一章之外的左上角）。其它3项跳转到相应的网址。

{: .center}
![目录](/img/web-edition/toggle-settings.png)

[2016-6-20更新] 章号也可以点击，它会在两个版本的相同章之间切换。如果只想读原文，偶尔才去看注解，或者反过来，这样会很方便。

根据试验，在目前体积的页面上添加动态效果，一般配置的手机处理起来比较缓慢。所以会采取两条路线：

- 今天上线的Web版，目标是在大部分智能手机上流畅地阅读（如果安装了Chrome浏览器，也许效果更好），今后也会越变越轻快。
- 此外还将增加一个“高配置”Web版，适合使用电脑或者高端手机、Pad阅读。它会加上我理想中当然要有、但又不得不放弃了的所有阅读便利。

{: .center}
欢迎支招，敬请期待！:blush:


<div id="disqus_thread"></div>
<script>
var disqus_config = function () {
    this.page.url = "http://www.abolybook.org/web-edition";  // Replace PAGE_URL with your page's canonical URL variable
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

<map name="abolycovermap" id="abolycovermap">
<area shape="circle" coords="308,451,22" href="/aboly#topiczheng4" alt="政" title="政">
<area shape="circle" coords="365,451,18" href="/aboly#topiczhong1" alt="忠" title="忠">
<area shape="circle" coords="164,504,18" href="/aboly#topiczhi4a" alt="智" title="智">
<area shape="circle" coords="361,351,18" href="/aboly#topicshu4" alt="恕" title="恕">
<area shape="circle" coords="187,451,22" href="/aboly#topicxue2" alt="学" title="学">
<area shape="circle" coords="247,390,39" href="/aboly#topicjunzi" alt="君子" title="君子">
<area shape="circle" coords="308,329,22" href="/aboly#topicli3" alt="礼" title="礼">
<area shape="circle" coords="348,491,18" href="/aboly#topicyongren" alt="贤" title="贤">
<area shape="circle" coords="185,329,22" href="/aboly#topicren2" alt="仁" title="仁">
<area shape="circle" coords="330,276,18" href="/aboly#topicqian1" alt="谦" title="谦">
<area shape="circle" coords="145,369,18" href="/aboly#topiczhi4" alt="志" title="志">
<area shape="circle" coords="133,472,18" href="/aboly#topicyi4a" alt="艺" title="艺">
<area shape="circle" coords="348,410,18" href="/aboly#topicde2" alt="德" title="德">
<area shape="circle" coords="308,508,18" href="/aboly#topichui4" alt="惠" title="惠">
<area shape="circle" coords="186,272,18" href="/aboly#topicyi4" alt="义" title="义">
<area shape="circle" coords="128,329,18" href="/aboly#topicyou3" alt="友" title="友">
<area shape="circle" coords="227,288,18" href="/aboly#topicxiao4" alt="孝" title="孝">
<area shape="circle" coords="267,491,18" href="/aboly#topiclian2" alt="廉" title="廉">
<area shape="circle" coords="286,276,18" href="/aboly#topicjing4" alt="敬" title="敬">
<area shape="circle" coords="133,429,18" href="/aboly#topicwen2" alt="文" title="文">
<area shape="circle" coords="145,288,18" href="/aboly#topicxin4" alt="信" title="信">
<area shape="circle" coords="208,504,18" href="/aboly#topicheng2" alt="恒" title="恒">
<area shape="circle" coords="360,307,18" href="/aboly#topicwen1" alt="温" title="温">
<area shape="default" href="/aboly" alt="《一瓶论语》" title="《一瓶论语》">
</map>

---
title: 变卦
subtitle: CSS / JavaScript 《易经》64卦酷炫实现
titleImg: /img/post/2014-08-11-how-i-made-biangua-02.png
time: 2014.08.11 18:32:00
layout: post
tags:
- 中文
- CSS
- JavaScript
- Project
shortUrl: http://goo.gl/8p81lL
excerpt: 本文是对<a href="http://zhangwenli.com/biangua" target="_blank">“变卦”网页</a>的详细说明。《易经》64卦，每卦由6爻组成，2的6次方就是64。仅一爻的由阳变阴，由阴变阳，就可以让整个卦象发生根本的改变。“<a href="http://zhangwenli.com/biangua" target="_blank">变卦</a>”，让每一爻的变化尽收眼底。
series: How I made ...
---

> #### 关于本文

> 本文是对<a href="http://zhangwenli.com/biangua" target="_blank">“变卦”网页</a>的详细说明。《易经》64卦，每卦由6爻组成，2的6次方就是64。仅一爻的由阳变阴，由阴变阳，就可以让整个卦象发生根本的改变。“<a href="http://zhangwenli.com/biangua" target="_blank">变卦</a>”，让每一爻的变化尽收眼底。

# 八卦与六十四卦

我们现在已经很少用到“八卦”的本意了，更多是与“娱乐”相关的含义了。那么，八卦究竟是什么意思呢？

> <img class="inline-img" src="{{ site.loadingImg }}" data-src="{{ site.url }}/img/post/2014-08-11-how-i-made-biangua-01.png" />

> 八卦是《易经》的基本概念，可代表一切自然现象的动静状态，由三个爻组成。“爻”是最基本的符号，意指交错，以奇画（“-”称阳爻）或偶画（“--”称阴爻）表示。爻有阴、阳两种仪态，若两两相重则形成四象（老阳、少阴、少阳、老阴）。四象再增加一爻，就形成八卦。

> 爻自下而上排列。“三个”爻的含义，象征着“天人地”（上有天、下为地、人在其中）。“卦”有悬挂的意思，也代表将各种现象的标示竖立起来以便于观察。

> 摘自 *<a href="http://zh.wikipedia.org/wiki/%E5%85%AB%E5%8D%A6" target="_blank">维基百科</a>*

## 八卦

鉴于来看我博客的很多都是程序猿，这么说可能更容易明白：八卦中每一卦由三爻组成，每个爻是“-”（阳）或者“--”（阴），所以就像是二进制编码一样，三爻就是3比特，能表达8种数字，这就是八卦啦！

这八个卦各有一个名字，卦名分别是*乾*、*坤*、*坎*、*离*、*震*、*巽*、*艮*、*兑*。令人惊讶的是，他们几乎可以表示任何事物。对于自然现象，他们分别指天、*地*、*水*、*火*、*雷*、*风*、*山*、*泽*；对于动物，他们可以指*马*、*牛*、*豕*、*雉*、*龙*、*鸡*、*狗*、*羊*；对于家庭关系，还可以指*父亲*、*母亲*、*中男*、*中女*、*长男*、*长女*、*少男*、*少女*。如此种种，不一而足。似乎也正是只有这样表述上的多样性，八卦才能用来预测复杂的卜筮对象。

## 六十四卦

传说八卦最初是周文王用来告诉百姓未来会发生什么（比如明天会不会下雨啦，取这个老婆以后会不会升官发财啦），可事情的变化可能性非常多，以至于八种状态不够完全来表述这种可能性的集合。因此，把两个三爻的卦叠起来，就是六爻一卦，那么现在我们有二进制6比特了，很快可以算出来2的6次方就是64了吧！——这就是《易经》六十四卦的由来。

八卦图已经如此复杂，六十四卦的话，对于初学者就很难记熟每一卦卦名了。

> <img src="{{ site.loadingImg }}" data-src="{{ site.url }}/img/post/2014-08-11-how-i-made-biangua-03.png" />

> 摘自 *<a href="http://zh.wikipedia.org/wiki/%E6%98%93%E7%B6%93" target="_blank">维基百科</a>*

## 变卦

简单地说，每一个卦象直接都有着微妙的联系。比如<a href="http://zhangwenli.com/biangua/#000000" target="_blank">坤</a>这一卦六爻都是阴（由两个三阴爻的坤卦组成），但你若是卜筮得到这一卦的话，你不仅仅需要分析这个卦象本身，还要考虑到卦象潜在的变化。《易经》中的卦是由下而上开始发生变化的，坤卦的第一爻（最下爻）变成阳以后，就变成了<a href="http://zhangwenli.com/biangua/#100000" target="_blank">复</a>卦。因此，你还要分析复卦的特性。对此，我的知识实在是太过浅薄，还是不要误人子弟了。

简而言之，《易经》是非常复杂的一套学问。你可以觉得迷信或者愚昧，但是作为一部影响了数千年中华文明最重要的作品（我认为其影响程度甚至超过了《论语》），说几千年的古人都是笨蛋才信这些，实在有些说不过去。当然，你完全可以不信它的卜筮作用，但未尝不值得研究点皮毛。

# 关于<a href="http://zhangwenli.com/biangua" target="_blank">“变卦”网页</a>

我算是《易经》的初学者，谈不上多么喜欢，但觉得里面有很有玄机所以很有敬畏之心。这次做“变卦”，一是想有一个清晰的变化过程来更好地理解变卦，另一方面也是想展示一下CSS和JavaScript能实现的酷炫效果。

## 数据来源

<a href="http://ctext.org/zhs" target="_blank">中国哲学书电子化计划</a>提供了非常丰富的经典古籍资料。由于网站声明严禁爬数据，我只能手动一点点复制，将近两个小时……

## “变卦”的效果实现

这其实也不难，只是一个障眼法。

我在每一爻中间放了一个分隔元素，如果是阳爻，其颜色就和爻的颜色一样，因而就看不见分隔元素了；如果是阴爻，那么分隔就和背景色一样，这样就像断成两半的爻了。

## 具体的代码实现

如果你想了解更多细节实现的话，可以<a href="https://github.com/Ovilia/biangua" target="_blank">在GitHub查看源码</a>，也欢迎<a href="#disqus_thread">留言</a>跟我交流相关实现。

如果你喜欢<a href="http://zhangwenli.com/biangua" target="_blank">“变卦”</a>的话，点下分享给好友吧，谢谢支持！
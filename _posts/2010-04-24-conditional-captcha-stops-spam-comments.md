---
layout: post
title: Conditional CAPTCHA：进一步阻拦垃圾评论
categories:
- Technology
tags:
- Akismet
- Conditional CAPTCHA
- Wordpress
- 垃圾评论
- 插件
---

用WordPress的都知道，Akismet是个不错的防垃圾评论的插件，判断的准确率还比较高，但长期以来我一直很恼火一件事，就是Akismet把那些判为垃圾评论的评论都放在垃圾队列中，最快也要一个月才自动删除，这样如果偶尔出现误判，我就得从几百条垃圾评论中眼巴巴去把误判的评论恢复过来。这些广告机器人每天都不厌其烦地发呀发，一天就是两三百条广告，我大多数时候都懒得看垃圾队列中有没有误判的，直接一键清空，所以有时候可能会殃及无辜。

昨天终于厌倦了，心想算了，还是去找个插件吧，肯定存在解决办法的。于是乎找到了一个叫Conditional CAPTCHA的插件，这个插件是Akismet之后的第二道防线：如果Akismet放行，它就不再过问，如果Akismet判为垃圾评论，它就继续弹出一个reCAPTCHA框让评论者输入验证码，这样的话，那些垃圾机器人压根儿就无法把评论发到我的数据库中，直接被删除了。

这下整个世界清净了。

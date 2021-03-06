---
layout: post
title: 画曲线的通用办法：描点法画图
categories:
- R language
tags:
- curve()
- gamma()
- R
- 杀牛用铅笔刀
- 画图
- 通用办法
---

初中的时候老师便教我们拿着直尺和圆规作图，那时候恐怕还没几个人会用电脑，直到初中毕业，我才第一次见电脑。那时候画曲线怎样画呢？记得就是在某个`x`区间上取一系列点，然后计算`y = f(x)`，把这些点描在笛卡尔坐标系中，然后用铅笔手工连起来。这个办法很笨很原始，但很有效，奇怪的是，到计算机如此发达的今天，仍然有人不断问如何用软件画曲线，仿佛中学时学的东西都还给数学老师了。例如，若干天前，有人问我如何用R画这个曲线：


$latex f(x)=(\sqrt{2}*\Gamma(x/2)*2)/(\sqrt{x-1}*\Gamma(x-1))$



我只好提醒他回忆中学的描点法。R里面的`gamma()`和`curve()`函数是现成的，把数学公式写成相应的代码就可以了：

    
    curve((sqrt(2) * gamma(x/2) * 2)/(sqrt(x - 1) * gamma(x - 1)), 2, 50)
    # 当然，如果你非要按照x = seq(2, 50, ...)然后计算f(x)然后plot(x, f(x), type = "l")
    # 那也可以，只不过curve()就是干这事的，不必麻烦分两步走了


[caption id="attachment_1019" align="aligncenter" width="480" caption="描点法画函数曲线"][![描点法画函数曲线](http://yihui.name/cn/wp-content/uploads/2009/06/curve-of-a-function.png)](http://yihui.name/cn/2009/06/from-points-to-curves/curve-of-a-function/)[/caption]

如同某些网文说人一辈子的守则在幼儿园都已经教完了，就看你长大还记不记得。所以每当面对一个貌似复杂的问题时，首先要想想幼儿园有没有学过。

“武功再高，也怕菜刀”绝对是真理，哈哈。

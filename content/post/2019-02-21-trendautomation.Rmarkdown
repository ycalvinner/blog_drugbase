---
title: 趋势分析自动化
author: Yao Shuliang
date: '2019-02-21'
slug: trendautomation
categories:
  - TrendAnalysis
tags: []
---

## GMP关于年度产品质量回顾的要求

**根据GMP第八节，应当按照操作规程，每年对所有生产的药品按品种进行产品质量回顾分析，以确认工艺稳定可靠，以及原辅料、成品现行质量标准的适用性，及时发现不良趋势，确定产品及工艺改进的方向。应当考虑以往回顾分析的历史数据，还应当对产品质量回顾分析的有效性进行自检。**

根据GMP要求，我们每年都会做年度产品质量回顾，同时，趋势分析也是其中比较重要的一个方面，但是在这个过程中往往遇到的比较多的问题：

- SPC中，连续多点上升或下降，发生在好几个月前，调查无从下手。
- SPC中，个别点较高，调查无从下手。

往往这时，我是我们最为苦恼的时候。

## 解决办法

有没有什么解决办法呢？有！那就是趋势分析自动化：

- 它不但能让我们日常在短时间内能做出趋势图，方便我们日常高频次的去非正式回顾。
- 还可以以GMP用途，作为日常趋势回顾，来配合其它的比如限度评估的策略。

下面我们来展示几种软件的趋势分析自动化的示例。

## R 语言

我开发了一个基于R语言的网页应用的电子系统，它可以实现多种功能，而功能之一，就是趋势分析自动化。我们只需要打开网址，就可以自动显示趋势图。（[更多彩蛋请点此](http://www.drugqm.com/?id=28)）

![TrendAnalysisAutomation.gif](http://www.drugqm.com/zb_users/upload/2017/12/201712301514644152171677.gif)


## JMP

我们可以定义一个脚本，只要运行一下，自动读取电脑上的excel数据，并绘制出图形。脚本和效果如下：

>dt1 = Open(
	"C:\Users\...\JMP_SPC.xlsx",
	Worksheets( "Sheet1" ),
	columns(
		New Column( "A含量", Numeric, "Continuous", Format( "Best", 12 ) )
	),
	Import Settings(
		End Of Line( CRLF, CR, LF ),
		End Of Field( Comma, CSV( 1 ) ),
		Strip Quotes( 0 ),
		Use Apostrophe as Quotation Mark( 0 ),
		Use Regional Settings( 0 ),
		Scan Whole File( 1 ),
		Treat empty columns as numeric( 0 ),
		CompressNumericColumns( 0 ),
		CompressCharacterColumns( 0 ),
		CompressAllowListCheck( 0 ),
		Labels( 1 ),
		Column Names Start( 1 ),
		Data Starts( 2 ),
		Lines To Read( "All" ),
		Year Rule( "20xx" )
	)
);
Overlay Plot( Y( :A含量 ), Separate Axes( 1 ) ,Connect Thru Missing( 1 ))

点击运行脚本文件：

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_JMP_1.png)

自动读取结果并绘图

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_JMP_2.png)


## Minitab

Minitab绘图也是比较方便的，我们来介绍一下。

和其它软件一样，Minitab有多种数据导入方式，而其中比较方便的一个，就是菜单中的"编辑->工作表链接->管理链接"，它可以动态读取Excel中的数据，并且，在图形上右键单击，勾选“自动更新图形”后，只要excel数据填了新数据，它会自动更新，让我们来看一下怎么设置吧。

__选择"编辑->工作表链接->管理链接"，出现如下窗口__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_Minitab_1.png)

__点击“添加”，然后按图示和根据实际，填写相关信息__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_Minitab_2.png)

__确定，数据自动导入到工作表中，绘制图形，在图形上右键单击，勾选“自动更新图形”__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_Minitab_3.png)

__Excel更新，Minitab中的图会自动更新__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_Minitab_4.png)





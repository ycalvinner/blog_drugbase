---
title: 趋势分析自动化
author: Yao Shuliang
date: '2019-02-21'
slug: trendautomation
categories:
  - TrendAnalysis
tags: []
---
## 趋势分析的两大类：

- 在药品质量管理活动中，我们往往有很多的数据需要进行趋势分析，并起草报告。例如“年度产品质量回顾”。
- 另外，我们可能往往还需要有一个方便的方式来更快速的以更高频次访问数据。例如：一个电子系统，能自动生成我们想看的图形。

对于趋势分析报告来说，同时也可以基于第2条，因为一个方便的获取趋势分析图形的途径，能让我们更快速的完成报告。

>想象一下以下场景：  
不断的点点点……呀，出来一张趋势图，copy, paste。然后 继续点点点……呀，又出来一张趋势图，copy, paste。然后……  
咦？有张图做错了，重新点点点……呀，出来了，copy, paste……  
呼，终于弄完了……  

这里，一方面，我们只能靠手工去生成图形，另一方面，手工操作容易犯错，第三方面，错了以后纠正的时间和操作成本高。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_General.jpg)

就像这篇文章里提到的一样,"all result from data should be reproducible"。这里一方面是指结果要容易重现，另一方面是指结果要可以重现。（当你面对一个结果的时候，鬼知道做这个结果的人都做了什么具体的操作）

## 本文章的目的：

所以，本文就着重在两个方面来讲：

- 趋势分析自动化：用于日常的高频快速趋势图。
- 报告生成自动化：用于可重复结果的报告的快速生成。
    - 利用趋势分析自动化，自动生成图形。
    - 当你某个结果错了的时候，鼠标点几个，改一下设置，直接重新生成即可。


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

## 示例数据

本贴所有数据均使用此数据：

[点此下载](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Data%20Demo.xlsx)


## R语言：Utility Trend Analysis Application

我开发了一个基于R语言的数据分析电子系统，它是一个网页应用。目前没有帐号控制，但是大家可以作为非GMP用途用作日常查看趋势图。总的来说还是非常方便的。

地址：http://apps.drugqm.com:3838/sample-apps/Trend_Automation/

分析数据范围：公用工程系统数据，包括总需氧菌，电导，TOC


### 使用介绍：

#### 趋势分析自动化

1. 首先打开网址，如图，点击OK或弹出窗口外部区域，即可关闭弹出窗口：

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_1.png)

2. 然后点击顶部导航栏的**Water-WFO** 或者 **Water-PW**，这里点击**Water-PW**。点击**Browse**上传文件（上面的示例文件或者自己的数据按示例文件整理。注意如果使用本电子系统，示例文件的工作薄名和列名不能修改，内容可以修改。），然后选择日期范围，点击**Apply**。右侧即显示图形。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_1_1.png)

如果想不显示所有点，只想显示其中一部分，则点击**Individual**，然后下面会出现一个文本框，点击一下，则可以选择数据中包含的点。确认日期范围，所有筛选均选择完后，点击**Apply**。图形则会自动更新。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_1_2.png)

如果想看图中某些点的**采样日期**，**取样点名称**，**测试结果**等信息，则可直接在图上拖选需要查看的点，数据会在页面最下方显示。


![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_3.png)

到这里，趋势分析自动化就结束了，下面来看一下报告的自动生成。

#### 报告自动生成。

所有条件设置完成后，点击**Open/Close Report Mode**下方，选中**Yes**，则每个图形上下方均会出现一个文本框，填入相应的内容。然后选择**Document Format**为**WORD**，然后点击**Download**，直接保存或打开下载的文档。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_4.png)

我们可以看到，图和描述自动生成了一个Word文档。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_R_5.png)


最有意思的是，如果你发现内容填错了，或者日期范围错了，或者点选错了等等，只需要回去重新设置一下，点击**Apply**，然后再下载一下报告，则内容会自动更新。


## JMP

如果我们的数据存在Excel文件里，我们可以选择“文件->新建->脚本”,把下面脚本粘过去，脚本如下：

>dt1 = Open(  
	"D:\Data Demo.xlsx",                          //文件路径
	Worksheets( "WFO-Data-Input" ),               //工作薄名称
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

如果我们的数据存在Excel文件里，我们可以选择“文件->新建->脚本”,把下面脚本粘过去，脚本如下：

>dt2 = open("D:\WFO-Data-Input.jmp");


点击运行，JMP就会打开一个数据窗口，并把数据读进来了。

**注意，此时脚本窗口先别关。**

然后我们手工去做图。比如，我做了一个时间序列图，得到如下图：

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_JMP_1.png)

点击窗口左上角的小红图标->保存脚本->至数据表，我们会发现数据表里多了一个名字，右键单击，选择编辑，则发现，这是JMP里做图的一段脚本，复制到上面打开文件的脚本后面，成品如下：

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_JMP_2.png)

>dt2 = open("D:\WFO-Data-Input.jmp");  
Overlay Plot( Y( :Result ), Separate Axes( 1 ) ,Connect Thru Missing( 1 ))

好，现在保存这个脚本，存下来。

下次我们直接打开这个脚本，运行即可，或者打开JMP，在脚本文件上右击，点击运行。就自动出图了。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/Trend_JMP_3.png)


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

**目前Minitab支持的软件有Excel, SPSS, Access。**


**注意Minitab和JMP，可以使用自身的工作表存储数据，不必一定要存在excel中。**

对于Minitab来说，可以用其自身存储数据，然后存成.MPJ文件，即一个Minitab Project文件。则以后图形和数据表就都存在这个文件中了。



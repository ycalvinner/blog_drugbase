---
title: 基于Minitab, JMP, SPSS, R做回归分析
author: Jonie
date: '2019-04-03'
slug: regression-analysis-with-minitab-jmp-and-r
categories:
  - Statistics
tags:
  - JMP
  - R
  - Minitab
  - SPSS
  - Regression
---

在稳定性实验考察的数据分析中，用的最多的往往是一般线性模型，现在软件选择这么多，该如何区分一些参数呢？下面做简要介绍。

### Type：检验的平方和

- I：序贯型，嵌套设计
- II：平衡设计，仅主效应
- III：调整型
- IV：不完整数据

### Contrasts(对比):

- Minitab/JMP无此项
- R/SPSS有。

>**R中:**
`options(contrasts=c(unordered="contr.treatment",ordered="contr.poly"))`为默认选项。此选项在方差分析或回归分析建模时，如果有因子，可以使用此参数。第一个是无序因子的参数，第二个是有序因子的参数。同时，也可以通过在建模时指定`contrasts`参数。比如`td_fit<-lm(Potency~Lot*Time,data=td,contrasts = list(Lot="contr.sum"))`

- R（系数对比）:    

首先介绍一下系数对比。

    - contr.helmert:
    - contr.poly
    - contr.SAS: SPSS默认使用此对比方式，设置此项时，R语言返回结果与SPSS的参数估计值相同。
    - contr.sum: JMP默认使用此对比方式，设置此项时，R语言返回结果与JMP的协变量，交互效应，截距参数       估计值相同。
    - contr.treatment：Minitab默认使用此对比方式，设置此项时，R语言返回结果与Minitab的参数估计值相       同。


- R(方差分析表）

方差分析表来讲，Minitab, JMP, SPSS在`模型`,`误差`,`合计`上一致。但回归项下各主效应和交互效应的平方和不同。   

    - contr.helmert/contr.sum/contr.poly:设置此项时，R语言返回结果与SPSS的参数估计值相同。
    - contr.SAS: 无具体描述
    - contr.treatment：无具体描述
    

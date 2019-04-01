---
title: Kernel Quantile Estimation
author: Jonie
date: '2019-03-31'
slug: kernel-quantile-estimation
categories:
  - Statistics
tags:
  - Statistical
  - nonparametric
  - Limit Evaluation
---

### Firstly, let's generate a dataset with continous data.


```r
set.seed(1)

(rand_data<-round(c(rnorm(5,10,2),rnorm(5,80,4)),0))
```

```
##  [1]  9 10  8 13 11 77 82 83 82 79
```

### JMP 

We can use JMP to fit the `smooth curve` model in JMP which has another name `Kernel Density Estimation`. Then we can use this model to calculate the quantile.

![JMP Result for this data](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/kernel_jmp1.png)

### R

Of course, you have another choice to finish this work with R. there're sereval ways to do this.

Details refer to [Wikipedia](https://en.wikipedia.org/wiki/Kernel_density_estimation)

**Way 1**

You can use `density` function in `stat` package to fit estimate the model and used as a parameter in function `quantile.density` in `spatstat` package to calculate the quantile.


```r
library(spatstat)
```

```
## Loading required package: spatstat.data
```

```
## Loading required package: nlme
```

```
## Loading required package: rpart
```

```
## 
## spatstat 1.59-0       (nickname: 'J'ai omis les oeufs de caille') 
## For an introduction to spatstat, type 'beginner'
```

```
## 
## Note: R version 3.5.1 (2018-07-02) is more than 9 months old; we strongly recommend upgrading to the latest version
```

```r
quantile.density(density(rand_data),c(0.00135,0.5,0.99865))
```

```
##    0.135%       50%   99.865% 
## -46.63139  45.30272 137.63139
```


**Way 2**

You canalso use `density` function in `stat` package to fit estimate the model and use `uniroot` function to calculate the root result which. sometimes, the result is the same with JMP, if it is not consist with the result in JMP, it may be caused by the bw value, and you can specify the bw value to get the same value. Of course, the result in JMP is not the "correct result", you can calculate the quantile with appropriate method.


```r
quantile_kde<-function(z,p=.95,bw=density(z)$bw){
  g <- function(x, z, bw, p) sum(pnorm(x-z, sd=bw))/length(z) - p
  uniroot(g,range(density(z)$x)+c(-1,1),z=z,bw=bw,p=p)$root
}

for(i in c(0.00135,0.5,0.99865)){
  cat(sprintf("The %f quantile is %f\n",i,quantile_kde(rand_data,i)))
}
```

```
## The 0.001350 quantile is -48.703622
## The 0.500000 quantile is 45.357844
## The 0.998650 quantile is 139.628200
```



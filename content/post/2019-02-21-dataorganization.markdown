---
title: Data Organization
author: 'Jonie'
date: '2019-02-21'
slug: dataorganization
categories: []
tags: []
---

## 格式要求

- 没有空行或空列
- 没有合并单元格
- 数值性数据不应包含符号，比如百分号。
- 重复内容应该包含相同内容。
- 每个单元格只填写一个信息元素。
- 只有一个标题行。
- 相同变量的所有元素应该在同一列。
- 前后一致。
- 数据值和非数据型数据不在同一列混放。
- 缺失值留空，不要用N/A（可以用NA）。
- 始终如一的保持输入格式要求，比如特殊字符，空值，大小写，等等
- 不用格式表示特殊意义，如需要，可以加一列字段表示。比如，性别用颜色进行区分，我们可以加一列，并分别用M表示男性，用F表示女性。

## 稳定性数据格式

__原始格式__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/DataOrganization_stability_1.png?q-sign-algorithm=sha1&q-ak=AKIDSwYvglgsip3upueA2Q5Wk1255ht1cjKe&q-sign-time=1550725544;1550727344&q-key-time=1550725544;1550727344&q-header-list=&q-url-param-list=&q-signature=f299eac3d26d75bfcf52a71ed5787f3be763e6c0&x-cos-security-token=87d90f01c643880b560e2af4d24dcf1e1aac1fcf10001)


__修改后__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/DataOrganization_stability_2.png?q-sign-algorithm=sha1&q-ak=AKIDpeVmeepard0Ef3xSEBxh4MdRwfDA6YvH&q-sign-time=1550725577;1550727377&q-key-time=1550725577;1550727377&q-header-list=&q-url-param-list=&q-signature=98cdc00c27b1ac368e077fa267b52b5937e149e8&x-cos-security-token=8cf2625fd456fd70c8abbbfb2b82c72e1f30552f10001)

## 环境监测数据

__修改前__

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/DataOrganization_stability_2.png?q-sign-algorithm=sha1&q-ak=AKIDpeVmeepard0Ef3xSEBxh4MdRwfDA6YvH&q-sign-time=1550725577;1550727377&q-key-time=1550725577;1550727377&q-header-list=&q-url-param-list=&q-signature=98cdc00c27b1ac368e077fa267b52b5937e149e8&x-cos-security-token=8cf2625fd456fd70c8abbbfb2b82c72e1f30552f10001)

__修改后-1__

可以使用这种格式，也是比较通用的格式。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/DataOrganization_2.png?q-sign-algorithm=sha1&q-ak=AKIDfZxU00zO0AfaenkUh4TpsWq5lMw6mTf6&q-sign-time=1550725681;1550727481&q-key-time=1550725681;1550727481&q-header-list=&q-url-param-list=&q-signature=86487168457fc8a9a77128f973801c0ab83f5a8c&x-cos-security-token=2b05673a9e481304d8e67e9eb17ae14202daa32a10001)

__修改后-2__

也可以使用这种格式。

![](https://blog-1255638709.cos.ap-chengdu.myqcloud.com/DataOrganization_3.png?q-sign-algorithm=sha1&q-ak=AKIDdBEvL0uSLzdh3vmfZlr6V3epll0TVfz5&q-sign-time=1550725710;1550727510&q-key-time=1550725710;1550727510&q-header-list=&q-url-param-list=&q-signature=7469306eac7d0ae58281a938c8cb4028682777c0&x-cos-security-token=084845a440f1ec753514cf3075af7f6dce4baee410001)

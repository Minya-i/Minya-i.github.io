---
title: newpapername
date: 2022-01-17 17:34:43
tags:
---



# 前端工作中遇到的技巧

## Object.freeze()

> 经过 Object.freeze() 方法的对象无法进行更新响应
>
> Object.freeze() 方法用于冻结对象，禁止对于该对象的属性进行修改（由于`数组本质也是对象`，因此该方法可以对数组使用）

注意：

1. Object.freeze() 和 const 变量声明不同,也不承担 const 的功能

2. const的行为像 let。它们唯一的区别是， const定义了一个无法重新分配的变量。 通过 const声明的变量是具有块级作用域的，而不是像 var声明的变量具有函数作用域。

3. Object.freeze()接受一个对象作为参数，并返回一个相同的不可变的对象。这就意味着我们不能添加，删除或更改对象的任何属性。

4. const和Object.freeze()并不同，const是防止变量重新分配，而Object.freeze()是使对象具有不可变性。

   

在工作中使用：

* 在utils封装

<img src="https://gitee.com/HuangGanGan_www/my_picture_bed/raw/master/img/companyWork/image-20211231110034081.png" alt="image-20211231110034081" style="zoom:67%;" />

*  在Vue中使用：

<img src="https://gitee.com/HuangGanGan_www/my_picture_bed/raw/master/img/companyWork/image-20211231110255630.png" alt="image-20211231110255630" style="zoom:67%;" />

<img src="https://gitee.com/HuangGanGan_www/my_picture_bed/raw/master/img/companyWork/image-20211231110229253.png" alt="image-20211231110229253" style="zoom:67%;" />
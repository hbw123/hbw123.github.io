---
layout:     post
title:      链表
subtitle:   链表
date:       2020-05-26
author:     HBW
header-img: img/post-bg-cook.jpg
catalog: true
tags:
    - 数据结构
    - 面试
    - 链表
typora-root-url: ../img
---

### **定义**

链表是一种物理[存储单元](https://baike.baidu.com/item/%E5%AD%98%E5%82%A8%E5%8D%95%E5%85%83/8727749)上非连续、非顺序的[存储结构](https://baike.baidu.com/item/%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84/350782)，[数据元素](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E5%85%83%E7%B4%A0/715313)的逻辑顺序是通过链表中的[指针](https://baike.baidu.com/item/%E6%8C%87%E9%92%88/2878304)链接次序实现的。链表由一系列结点（链表中每一个元素称为结点）组成，结点可以在运行时动态生成。每个结点包括两个部分：一个是存储[数据元素](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E5%85%83%E7%B4%A0)的数据域，另一个是存储下一个结点地址的[指针](https://baike.baidu.com/item/%E6%8C%87%E9%92%88/2878304)域。 相比于[线性表](https://baike.baidu.com/item/%E7%BA%BF%E6%80%A7%E8%A1%A8/3228081)[顺序结构](https://baike.baidu.com/item/%E9%A1%BA%E5%BA%8F%E7%BB%93%E6%9E%84/9845234)，操作复杂。由于不必须按顺序存储，链表在插入的时候可以达到O(1)的复杂度，比另一种线性表顺序表快得多，但是查找一个节点或者访问特定编号的节点则需要O(n)的时间，而线性表和顺序表相应的时间复杂度分别是O(logn)和O(1)。

使用链表结构可以克服[数组](https://baike.baidu.com/item/%E6%95%B0%E7%BB%84/3794097)链表需要预先知道数据大小的缺点，链表结构可以充分利用计算机内存空间，实现灵活的内存动态管理。但是链表失去了[数组](https://baike.baidu.com/item/%E6%95%B0%E7%BB%84/3794097)随机读取的优点，同时链表由于增加了结点的[指针](https://baike.baidu.com/item/%E6%8C%87%E9%92%88/2878304)域，空间开销比较大。链表最明显的好处就是，常规[数组](https://baike.baidu.com/item/%E6%95%B0%E7%BB%84/3794097)排列关联项目的方式可能不同于这些数据项目在[记忆体](https://baike.baidu.com/item/%E8%AE%B0%E5%BF%86%E4%BD%93/3029693)或[磁盘](https://baike.baidu.com/item/%E7%A3%81%E7%9B%98/2842227)上顺序，数据的存取往往要在不同的排列顺序中转换。链表允许插入和移除表上任意位置上的[节点](https://baike.baidu.com/item/%E8%8A%82%E7%82%B9/865052)，但是不允许[随机存取](https://baike.baidu.com/item/%E9%9A%8F%E6%9C%BA%E5%AD%98%E5%8F%96/4610937)。链表有很多种不同的类型：[单向链表](/2020/05/27/linkedlist_2/)，[双向链表](https://baike.baidu.com/item/%E5%8F%8C%E5%90%91%E9%93%BE%E8%A1%A8/2968731)以及[循环链表](https://baike.baidu.com/item/%E5%BE%AA%E7%8E%AF%E9%93%BE%E8%A1%A8/3228465)。


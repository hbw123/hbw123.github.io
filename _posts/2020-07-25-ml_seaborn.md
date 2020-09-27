---
layout:     post
title:      Seaborn使用教程
subtitle:   Seaborn
date:       2020-07-25
author:     HBW
header-img: img/post-bg-cook.jpg
catalog: true
tags:
    - 人工智能
    - 机器学习
    - Seaborn
---
### Seaborn简介

Seaborn是基于matplotlib的图形可视化python包。它提供了一种高度交互式界面，便于用户能够做出各种有吸引力的统计图表。

Seaborn是在matplotlib的基础上进行了更高级的API封装，从而使得作图更加容易，在大多数情况下使用seaborn能做出很具有吸引力的图，而使用matplotlib就能制作具有更多特色的图。应该把Seaborn视为matplotlib的补充，而不是替代物。同时它能高度兼容numpy与pandas数据结构以及scipy与statsmodels等统计模式

### 安装

```python
pip install seaborn 
```

### 用法

```markdown
1. sns.图名(x='X轴 列名', y='Y轴 列名', hue='分组绘图参数', data=原始数据df对象)
```

### Seaborn架构

1. **风格管理**

   - 绘图风格设置

     ```markdown
     1. {darkgrid, whitegrid, dark, white, ticks}
     2. sns.set_style('ticks')
     ```

   - 颜色风格设置

     ```markdown
     1. {deep, muted, pastel, dark, bright, colorblind}
     2. color_palette=sns.color_palette('dark')
     3. sns.set_palette(color_palette)
     ```

2. **绘图方法**

   - 数据集的分布可视化

     ```markdown
     1. 单变量分析
     	sns.distplot(df.result)  直方图和拟合曲线
     2. 多变量分析
     	sns.scatterplot(x='x',y='y',data=X) 散点图
     	sns.pairplot(X) 两两特征对比图
     	sns.kdeplot(X) 等高线图
     	sns.stripplot(x='x',y='y',data=df) 特征值分布图 有重叠
     	sns.stripplot(x='x',y='y',data=df,jitter=True)特征值分布图 无重叠
     	sns.swarmplot(x='x',y='y',data=df)特征值分布图 树状
     	盒图
     	1. IQR：统计学概念 四分位距  指的是四分之一到四分之三的距离
     	2. 离群点：一个值大于四分之三位+1.5IQR或者小于四分之一-1.5IQR
     	sns.boxplot(x='x',y='y',data=df)
     	sns.violinplot(x='x',y='y',data=df)  小提琴图
     ```

   - 分类数据可视化

     ```markdown
     1. sns.barplot(data=df) 条形图
     2. sns.pairplot(x='x',y='y',data=df) 点图
     3. sns.factorplot(x='x',y='y',data=df) 多层面板分类图
     4. sns.countplot() 数量统计图
     ```

   - 线性关系可视化

     ```markdown
     1. sns.regplot(x='x',y='y',data=df)  回归分析图
     ```

3. **结构网格**

   - 数据识别网格绘图

     ```markdown
     fg=sns.FacetGrid(df,col='x')
     fg.map(plt.scatter,'y','y')
     ```

4. ##### 热度图

   ```markdown
   df=np.random.rand(3,3)
   sns.heatmap(df)
   ```

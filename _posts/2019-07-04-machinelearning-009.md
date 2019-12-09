---
title: 【西瓜书】 009 聚类
date: 2019-07-04 17:26:00
---

### 聚类任务

聚类试图将训练集中的样本划分为若干个通常是不相交的子集，每个子集被称为一个“簇”。




### 性能度量

### 距离计算

### 原型聚类

### 高斯混合聚类

多元高斯概率密度函数：
$$P(x) = \frac{1}{(2\pi)^{\frac{1}{2}} \|\sum\|^{\frac{1}{2}}} e^{-\frac{1}{2} (x - \mu)^T \sum^{-1} (x - \mu)}$$

高斯混合分布：
$$P_M(x) = \sum_{i=1}^{k}{\alpha_i p(x\|\mu_i,\sum_i)}$$

$\alpha_i > 0$是混合系数，加和为1.
K表示k个混合成份。


样本生成过程：
$\alpha_i$ 的含义，即 为选择第 i 个混合成分的概率，或者反过来说，$\alpha_i$ 为样本属于第 i个混合 成分的概率。重新描述一下样本生成过程，根据先验分布$\alpha_1, \alpha_2, ...$ 选择其中一个高斯 混合成分（即第 i 个高斯混合成分被选到的概率为 $\alpha_i$），假设选到了第 i 个高斯混合成分，其 参数为$\mu_i, \sum_i$ ；然后根据概率密度函数$p(x|\mu_i, \sum_i)$ （即将式(9.28)中的 $\mu, \sum$ 替换为 $\mu_i, \sum_i$ ） 进行采样生成样本 x 。两个步骤的区别在于第 1 步选择高斯混合成分时是从 k 个之中选其一 （相当于概率密度函数是离散的），而第2步生成样本时是从 x 定义域中根据 $p(x|\mu_i, \sum_i)$ 选 择其中一个样本，样本 x 被选中的概率即为 $p(x|\mu_i, \sum_i)$ 。即第1步对应于离散型随机变量， 第 2 步对应于连续型随机变





### 密度聚类

### 层次聚类

### 习题
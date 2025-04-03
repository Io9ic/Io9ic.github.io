# 孟德尔随机化文献综述

## 引言

孟德尔随机化(mendelian randomlization)是一种工具变量分析形式，利用SNPS基因型形式的

遗传标记作为“暴露”的遗传代理，用于作为分析暴露和结果之间的因果分析。

### 三大IV假设

孟德尔随机化使用SNPS作为工具变量进行因果分析有三个基本假设：

1. SNP工具与暴露相关。如果关于SNP工具与暴露之间关联的第一个假设成立,但这种关联较弱,则可能导致偏差的放大
2. 暴露以及所有已测量和未测量的混杂因素条件下,SNP工具与结果之间具有独立性
4. snp工具变量独立于所有(已测量和未测量的)暴露与结果之间关系的混杂因素

### 依赖

孟德尔随机化的发展依赖于全基因组GWAS

### 目的

解决一个问题：如何判断一个变量是否是真正的因果变量，在循证医学中，或在制定干预政策时，明确因果性十分必要。可能存在的偏差：1. 反向因果关系（revese causation）2.混淆变量造成的偏倚（omitted variable bias due to confounding）,测量误差(meaurement error),双向因果关系(bidirectional causality)

在现实中，要完成随机对照实验需要很大的人力物力，有时因伦理问题无法实施。

孟德尔随机化在统计学本质是利用孟德尔第二定律，也就是自由组合规律，当具有两队或更多相对性状的亲本进行杂交，子一代产生配子时，等位基因分离的同时，非同源染色体的基因自由组合，类似于随机对照。

工具变量简单来说就是，一个与X相关，但与被忽略的混淆因素以及Y不相关的变量。在经济学研究中工具变量可以是政策改革，自然灾害等等，而在遗传学中，这个变量就是基因。

## 简单孟德尔随机化（单变量）

#### 二阶段最小二乘估计

$$
X=\mu_1+\beta Z+\theta
$$





wald系数：
$$
\frac{Cov_{y,z}}{Cov_{x,z}}
$$

### 潜在问题

4.1 遗传相关中，因果关系的方向是确定的，遗传多样性导致了不同的表型，反之则不成立

4.2 一般情况下我们所测量的环境暴露因素都或多或少与行为，社会，心理等因素相关，造成偏倚。但遗传变异则不受这些混淆因素影响。

4.3 相对来说，遗传变异与其效应的测量误差较小。

4.4 并不一定要找到因果SNP，一个与因果SNP处于LD的SNP即可满足假设条件。

4.5.目前GWAS的数据相对容易获取

### 双样本汇总数据  MR



## 存在异质性的孟德尔随机化

### 异质性在孟德尔随机化

> Del Greco FM, Minelli C, Sheehan NA, Thompson JR. Detecting  pleiotropy in Mendelian randomisation studies with summary  data and a continuous outcome. Stat Med. 2015;34(21):  2926‐2940.

计量经济学中使用相似方法，对孟德尔随机化使用
$$
 \overline{F} = \frac{1}{L} \sum_{j=1}^{L} \frac{\widehat{\gamma}j^2}{\sigma{Xj}^2}
$$

$$
w_j(\beta) = \frac{\beta^2 \sigma{Xj}^2 + \sigma_{Yj}^2}{\widehat{\gamma}_j^2}
$$

 

> Improving the accuracy of two-sample  summary-data Mendelian randomization:  moving beyond the NOME assumption  Jack Bowden,1,2* Fabiola Del Greco M,3 Cosetta Minelli,4 Qingyuan Zhao,5 Debbie A Lawlor,1,2 Nuala A Sheehan,6 John Thompson6 and George Davey Smith1,2
>

最小 Q 统计量不受弱工具变量导致的膨胀影响。通过  使用(9)中的权重得出的β优化值是一个改进的 IVW 估计,  该估计在固定效应模型下不受回归稀释偏差的影响



## MR-Egger 回归

### 改进

Lin Z, Pan I, Pan W (2022) A practical problem with Egger regression in Mendelian randomization. PLOS Genetics 18:e1010166. doi: [10.1371/journal.pgen.1010166](https://doi.org/10.1371/journal.pgen.1010166)




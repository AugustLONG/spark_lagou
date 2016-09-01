本系列专属github地址:[https://github.com/ios122/spark_lagou](https://github.com/ios122/spark_lagou)

## 前言

我觉得如果动笔,就应该努力地把要说的东西表达清楚.今后一段时间,尝试下系列博客文章.简单说,如果心里想表达想分享的,就适当规划组织下,使其相对自成体系,以便于感兴趣但可能刚好某个领域还不是很熟的人,也能很好地入手.系列文章,我会努力避免过于主观化的描述,同时吸取以往的经验,尽量给每个系列的文章都设置一个单独的 github 项目,供查阅参考.

## Spark 系列文章规划

Spark系列,因为本人并非供职于大型数据公司,也未曾在较大数据集上实践过,所以内容可能仅供初级入门者参考.目前,我处理过的较大的数据集,也仅在百万条左右,但是也不得不惊叹 Spark 做为数据分析工具的便利性,100w条数据,在3台BMR服务器结点上,复杂查询一般在十秒以内.从数据分析的工具角度,我觉得 Spark 还是有必要了解的,大多数时候,基于数据的多个维度分析出的结论,可能比某些抽象的统计数据,能有说服力.

### 数据源: 拉勾网 iOS 职位最近一个月的公开招聘信息

以拉勾网 iOS 职位最近一个月的公开招聘信息作为样本.这是一个样本,到时我会具体说一下数据获取的方法和思路,还会奉上可用的脚本.

### 数据分析工具:Spark.

Spark是主要分析工具.我前一段时间,看了那本<< Hadoop 权威指南 >>,然后开始了Spark的学习.自己感觉 Spark,可能更符合自己目前阶段的需要--小规模数据的即时分析.

### 数据分析平台: 百度BMR

我会直接基于百度BMR来分析数据.至今,我没有试过自己搭建spark开发环境,也暂无打算研究.因为我觉得,大数据的分析,硬件还是挺贵的,好在现在有云平台,即开即用,用完释放掉即可.还有一个原因是,单机版的Spark和分布式的Spark,某些函数的行为还是有差异的.我看阿里云,也有类似的大数据分析平台,应该也是可以的.

### 准备事宜

实名认证的百度开发者账号,注册请到 [https://login.bce.baidu.com](https://login.bce.baidu.com) 因为必须是实名认证的百度开发者账号,才可以创建 BMR 实例,没有账号,可能会影响到你观察文章的体验.因为这个实名认证要审核的,最好提前弄.

## 文章更新具体规划

### 使用Spark分析拉勾网招聘信息(一):准备工作

交代基本背景,动机与必要准别事宜等,为进一步文章铺垫.

### 使用Spark分析拉勾网招聘信息(二): 获取数据

使用脚本自动获取数据,会涉及数据源的分析,脚本编写思路,以及一个最终可用的脚本和实际采集的完整数据附件.

## 使用Spark分析拉勾网招聘信息(三): BMR 入门

主要讲解百度大数据平台BMR的基础操作与常用工具的使用.当然电脑性能较为强悍的童鞋,可以自己安装研究下Hadoop,Spark和Zeepline等工具.用BMR,比较省钱,按分钟计费,一小时 2块左右,我通常只是有感兴趣的数据题材时才开启.顺便插一句,以数据的视角,自由组合维度来观察某些自己关心的数据,真的看出来许多刷新自己认知的**真实**.不过,考虑到工具的可扩展性,我还是建议掌握下 BMR或者阿里的大数据平台的基础使用.

### 使用Spark分析拉勾网招聘信息(四): 几个常用的脚本与图片分析结果

这里,会结合数据结构,展示下数据分析与提取的基本思路,然后会选几个角度分析下数据.方法是根本,简单了解下,再多看看 spark 和 scala 文档,我相信大家是可以自由使用Spark来分析自己感兴趣的数据的.

---
**版权声明**: iOS122 **颜风** 署名系列文章,每日 **7:20** 首发于微信公众号 **iOS122gg**,其他平台次日10点更新.除各大博客平台的iOS122官方专栏外,其他任何用途的转载与使用,请务必注明出处!
---
layout: post
title:  "经典模型结构"
subtitle: "如何选择适合的模型？"
categories: [MachineLearning]
---

说说久经考验的机器学习经典模型。


# LR models


# GBM models


# FM models

对categorical类型进行独热编码变成数值特征（1变多）之后，特征会非常稀疏（非零值少），特征维度空间也变大。因此FM的思路是构建新的交叉特征。

FM的表达式是在线性表达式后面加入了新的交叉项特征及对应的权值。

https://www.cnblogs.com/wkang/p/9588360.html


# Deep-learning based CTR models

![]({{site.baseurl}}/images/dnnmodels.jpeg)

![]({{site.baseurl}}/images/dnnmodels-2.jpg)



## Wide and Deep learning 模型

- wide model (logistic regression with sparse features and transformations) 
wide的部分具有较强的记忆能力，协同过滤、逻辑回归等简单模型的记忆能力较强。
- deep model (feed-forward neural network with an embedding layer and several hidden layers)
deep的部分具有较强的泛化能力，

### DeepFM 模型

将LR替换为FM

### Deep&Cross DCN 模型

它和Wide&Deep的差异就是用cross网络替代wide的部分。

Cross Layer





## DIN & DIEN

在embedding层和MLP层之间加入 attention 机制



## MOE


# Deep-learning based NLP models

## Batch Negative


## Transformer

transformer layer的样子

- 美团如何使用 Transformer 搜索排序 https://tech.meituan.com/2020/04/16/transformer-in-meituan.html

- 介绍 http://jalammar.github.io/illustrated-transformer/


## Attention

https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/


## BERT 模型

BERT的全称是Bidirectional Encoder Representation from Transformers，即双向Transformer的Encoder，因为decoder是不能获要预测的信息的。模型的主要创新点都在pre-train方法上，即用了Masked LM和Next Sentence Prediction两种方法分别捕捉词语和句子级别的representation。

https://mp.weixin.qq.com/s/mFRhp9pJRa9yHwqc98FMbg


# Deep-learning based Gragh models

LeNet-5网络，AlexNet，VGG网络，GoogLeNet，残差网络





# References

wide&deep: https://arxiv.org/pdf/1606.07792.pdf

seq2seq: https://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf

PNN: https://arxiv.org/pdf/1611.00144.pdf

NCF: https://www.comp.nus.edu.sg/~xiangnan/papers/ncf.pdf

MV-DNN: https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/frp1159-songA.pdf

FNN: 利用FM的结果进行网络初始化 https://arxiv.org/pdf/1601.02376.pdf

DNN-YouTube: https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf

DCN: https://arxiv.org/pdf/1708.05123.pdf ， DCN介绍： https://zhuanlan.zhihu.com/p/43364598

GBDT+LR: http://quinonero.net/Publications/predicting-clicks-facebook.pdf

FM: https://www.csie.ntu.edu.tw/~b97053/paper/Rendle2010FM.pdf

NFM: 使用神经网络提升FM二阶部分的特征交叉能力 https://www.comp.nus.edu.sg/~xiangnan/papers/sigir17-nfm.pdf

AFM: 引入了注意力机制的FM模型 https://arxiv.org/pdf/1708.04617.pdf

deepFM: https://www.ijcai.org/proceedings/2017/0239.pdf

深度学习推荐系统 https://www.zhihu.com/people/wang-zhe-58

CTR深度模型总结 https://github.com/shenweichen/DeepCTR
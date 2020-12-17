---
title: ECG Classification
date: 2019-6-18 08:15:50
categories: 
- ECG
tags: ECG
---

---

## 1. 单独对N，S两类进行分类的实验结果
## 2. N、S、V、F、Q五分类的实验（mean;std）结果
## 3. N、S、V、F、Q五分类的实验（dropout）结果
## 4. Heading 2

---

首先值得肯定的是不管是过拟合还是欠拟合，模型在训练集上的表现是非常好的，在测试集中，N,V两类的表现也比较好，唯独S类表现极差。

1、单独对N，S两类进行分类的实验结果：
```
测试集的混淆矩阵:
[[43956   262]
 [ 1676   160]]
 Test set: loss: 0.0108, Accuracy: 44116/46054 (95.79190%)
 训练集的混淆矩阵：
 [[45750    76]
 [  144   799]]
Train set: loss: 0.001126, Accuracy: 46549/46769 (99.52960%)
```
2、N、S、V、F、Q五分类的实验（mean;std）结果：
```
测试集的混淆矩阵:
[[42243   407   602   966     0]
 [ 1412   211   212     1     0]
 [  183    42  2970    24     0]
 [  301     3    83     1     0]
 [    2     0     5     0     0]]

Test set: loss: 0.032887, Accuracy: 45425/49668 (91.45728%)

训练集的混淆矩阵:
[[45802    13     1    10     0]
 [   23   917     3     0     0]
 [    6     3  3775     4     0]
 [   10     0     5   399     0]
 [    7     0     1     0     0]]

Train set: loss: 0.000342, Accuracy: 50893/50979 (99.83130%)
```
3、N、S、V、F、Q五分类的实验（dropout）结果：
```
dropout = 0.1
测试集的混淆矩阵:
[[41448   433  1164  1173     0]
 [ 1404   161   270     1     0]
 [  159    47  2989    24     0]
 [  302     3    82     1     0]
 [    3     0     4     0     0]]
Test set: loss: 0.035579, Accuracy: 44599/49668 (89.79423%)
训练集的混淆矩阵:
[[45798    17     4     7     0]
 [   23   917     3     0     0]
 [    9     2  3770     7     0]
 [   22     0     5   387     0]
 [    6     1     1     0     0]]
Train set: loss: 0.000374, Accuracy: 50872/50979 (99.79011%)

dropout = 0.5
测试集的混淆矩阵:
[[40577   343  1775  1523     0]
 [ 1424    95   317     0     0]
 [  274    70  2855    20     0]
 [  280     3   103     2     0]
 [    2     0     5     0     0]]
Test set: loss: 0.03826, Accuracy: 43529/49668 (87.63993%)
训练集的混淆矩阵:
[[45784    30     9     3     0]
 [   39   895     9     0     0]
 [   25     3  3750    10     0]
 [   39     0    14   361     0]
 [    6     0     2     0     0]]
Train set: loss: 0.000694, Accuracy: 50790/50979 (99.62926%)

dropout = 0.9
测试集的混淆矩阵:
[[38011   189  6001    17     0]
 [ 1453    35   348     0     0]
 [  418    64  2729     8     0]
 [  130     1   257     0     0]
 [    2     0     5     0     0]]
Test set: loss: 0.037088, Accuracy: 40775/49668 (82.09511%)
训练集的混淆矩阵:
[[45424   255   144     3     0]
 [  190   672    81     0     0]
 [  147     7  3630     4     0]
 [  215     0    59   140     0]
 [    6     0     2     0     0]]
Train set: loss: 0.004964, Accuracy: 49866/50979 (97.81675%)
```
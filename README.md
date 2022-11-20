# RandomForest

随机森林算法，随机构建多棵决策树，多颗决策树对object类别进行投票，票数多者即为随机森林输出的object的类别

## 内容列表

- [1.介绍](#1.介绍)
- [2.环境](#2.环境)
- [3.使用说明](#3.使用说明)
  - [Step1](#Step1)
  - [Step2](#Step2)
  - [Step3](#Step3)
- [4.相关文章](#4.相关文章)
- 
## 1.介绍

该文档是为了帮助你快速了解该算法的操作流程

整个算法中包括三个部分：输入数据集，根据数据集随机创建多棵决策树，利用创建的决策树对输入的object类别进行判定

分别在三个.py文件中对其进行了实现

## 2.环境

python  3.10等

## 3.使用说明

#### Step1：

运行createDataSet.py生成数据集并输出为dataSet.json和labels.json

数据集的最后一列应为该对象的类别，如：好瓜，坏瓜

##### 数据集输入示例：

```python
[
        # 1
        ['青绿', '蜷缩', '浊响', '清晰', '凹陷', '硬滑', '好瓜'],
        # 2
        ['乌黑', '蜷缩', '沉闷', '清晰', '凹陷', '硬滑', '好瓜'],
        # 3
        ['乌黑', '蜷缩', '浊响', '清晰', '凹陷', '硬滑', '好瓜'],
        # 4
        ['青绿', '蜷缩', '沉闷', '清晰', '凹陷', '硬滑', '好瓜'],
        # 5
        ['浅白', '蜷缩', '浊响', '清晰', '凹陷', '硬滑', '好瓜'],
        # 6
        ['青绿', '稍蜷', '浊响', '清晰', '稍凹', '软粘', '好瓜'],
        # 7
        ['乌黑', '稍蜷', '浊响', '稍糊', '稍凹', '软粘', '好瓜'],
        # 8
        ['乌黑', '稍蜷', '浊响', '清晰', '稍凹', '硬滑', '好瓜'],
        # 9
        ['乌黑', '稍蜷', '沉闷', '稍糊', '稍凹', '硬滑', '坏瓜'],
        # 10
        ['青绿', '硬挺', '清脆', '清晰', '平坦', '软粘', '坏瓜'],
        # 11
        ['浅白', '硬挺', '清脆', '模糊', '平坦', '硬滑', '坏瓜'],
        # 12
        ['浅白', '蜷缩', '浊响', '模糊', '平坦', '软粘', '坏瓜'],
        # 13
        ['青绿', '稍蜷', '浊响', '稍糊', '凹陷', '硬滑', '坏瓜'],
        # 14
        ['浅白', '稍蜷', '沉闷', '稍糊', '凹陷', '硬滑', '坏瓜'],
        # 15
        ['乌黑', '稍蜷', '浊响', '清晰', '稍凹', '软粘', '坏瓜'],
        # 16
        ['浅白', '蜷缩', '浊响', '模糊', '平坦', '硬滑', '坏瓜'],
        # 17
        ['青绿', '蜷缩', '沉闷', '稍糊', '稍凹', '硬滑', '坏瓜']
]
```

#####label输入示例：
```python
['色泽', '根蒂', '敲击', '纹理', '脐部', '触感', 'good/bad']
```


#### Step2：

运行RandomForest.py生成随机森林，并输出为treeSet.json

此步中需要step1中生成的dataSet.json和labels.json，当然你也可以用自己生成的dataSet.json文件和labels.json文件（要注意输入格式符合范例）

#### Step3:

运行DecideByRandomForest.py，读取dataSet.json labels.json 和treeSet.json

用户在控制台输入要判断的对象

输入对象应为一个属性列表，例：

```python
['青绿', '蜷缩', '浊响', '清晰', '凹陷', '硬滑',]
```
控制台将输出随机森林对该对象的类别判断结果如：

```python
好瓜
```

## 4.相关文章
#### 决策树总结（二）如何构建决策树
https://zhuanlan.zhihu.com/p/266880465
#### 一文看懂随机森林 - Random Forest（附 4 个构造步骤+10 个优缺点）
https://zhuanlan.zhihu.com/p/266880465


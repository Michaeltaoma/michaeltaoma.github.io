---
title: What is bias?

updated: 2020-05-07 19:40
---

## What is bias?

<iframe width="560" height="315" src="https://www.youtube.com/embed/HetFihsXSys" frameborder="0" allowfullscreen></iframe>

但凡对于神经网络有过一定了解的人，就不会不知道bias。但是很多人对bias的理解也就只停留在了一个简单的阶段即bias偏差值和学习率一样，都只是神经网络的一个参数，我们训练神经网络，就是通过多次迭代，找出现有训练集下的能够最大化模型预测精准度的参数的值。在计算加权和的时候，为了确保bias能够随着权重在每一次的迭代中被调整到，神经网络都是把bias当作是一个不存在的输入\\(x_0(= 1) \\)的权重，也就是说，\\( \sum_{i=0}w_{i}\*x_{i} \\)是等价于\\(\sum_{i = 1}w_{i}*x_{i} + bias \\)，不过不知道大家也没有思考过这样明显存在的问题：为什么需要bias？这么一个值对于神经网络能取到什么样子的调整？
- 为什么需要bias？针对这个问题答案其实很简单，bias调整了函数

title: 机器学习
date: 2023-5-23 19:05
tags:
- 机器学习
- 算法
- 研究生
---

# 机器学习

## 1.机器学习的基本概念

机器学习≈构建一个映射函数

- 语音识别
- 图像识别
- 围棋 落子位置
- 对话系统

基本概念

样本，特征，标签，模型，算法

![image-20230510105923640](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510105923640.png)

`X = [x1,x2,...]` 特征向量 Feature Vector

保证每个样本是独立同分布的（例如：抛硬币

![image-20230510133423833](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510133423833.png)

![image-20230510133947884](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510133947884.png)

## 2.机器学习的三要素

### （1）模型

![image-20230510144012644](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510144012644.png)

### （2）学习准则

![image-20230510145407206](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510145407206.png)

#### 交叉熵损失函数（负对数自然函数 )

p永远<1
$$
loss = -p\log_{2}\hat{p}
$$

#### 2分类损失函数

$$
L = \max (0,1-y*\hat{y} )
$$

#### 经验风险最小化

![image-20230510152107609](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510152107609.png)

#### 过拟合

![](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510153109711.png)

### （3）优化

![image-20230510153452219](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510153452219.png)

#### 正则化

![image-20230510153624656](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510153624656.png)

![image-20230510153749689](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510153749689.png)

#### 最优化问题

![image-20230510154012561](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510154012561.png)

#### 梯度下降法

![image-20230510154031453](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510154031453.png)

![image-20230510154924411](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510154924411.png)

![image-20230510155136858](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510155136858.png)

![image-20230510155802282](https://image-yangj.oss-cn-beijing.aliyuncs.com/typora/image-20230510155802282.png)

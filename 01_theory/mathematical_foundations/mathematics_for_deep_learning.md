# 深度学习所需数学基础

本文件用于整理数学理论在机器学习、深度学习、Transformer和物理AI中的具体作用。

## 1. 线性代数与神经网络

### 核心知识

- 向量与矩阵
- 张量
- 矩阵乘法
- 内积与相似度
- 特征分解
- 奇异值分解
- 低秩近似

### 深度学习中的应用

- 神经网络线性层
- Embedding表示
- Attention中的Q、K、V计算
- 参数矩阵
- LoRA低秩适配
- PCA与特征压缩

## 2. 微积分与反向传播

### 核心知识

- 导数
- 偏导数
- 梯度
- 链式法则
- Jacobian
- Hessian

### 深度学习中的应用

- 反向传播
- 损失函数优化
- 自动微分
- 梯度消失与梯度爆炸
- 梯度裁剪
- 二阶优化方法

## 3. 概率统计与机器学习

### 核心知识

- 条件概率
- 贝叶斯公式
- 常见概率分布
- 期望与方差
- 最大似然估计
- 最大后验估计

### 深度学习中的应用

- 交叉熵损失
- Softmax
- 生成模型
- Dropout
- 贝叶斯神经网络
- 不确定性估计
- MC Dropout

## 4. 最优化与模型训练

- Batch Gradient Descent
- SGD
- Momentum
- AdaGrad
- RMSProp
- Adam与AdamW
- Weight Decay
- Learning Rate Scheduler
- Warm-up
- 梯度累积

## 5. 信息论

- 信息量
- 熵
- 交叉熵
- KL散度
- 互信息

### 应用

- 分类损失
- 知识蒸馏
- 表征学习
- 对比学习
- 多模态对齐
- 变分自编码器

## 6. Transformer数学基础

- Token Embedding
- Position Encoding
- Scaled Dot-Product Attention
- Multi-Head Attention
- Mask
- Layer Normalization
- Residual Connection
- Feed-Forward Network

核心公式：

```text
Attention(Q, K, V)
= softmax(QKᵀ / √dₖ)V

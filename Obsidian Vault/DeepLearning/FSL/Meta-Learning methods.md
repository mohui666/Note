# MAML
### 对于每一类任务划分support和query集,inner loop在support集合上训练,outer loop在query集合上进行meta更新
***变体:FOMAML:忽略二阶导数(Relu的使用导致二阶导接近为常数)***

---
# Reptile
### 不直接使用任务内梯度，而是用任务训练前后模型参数的差值来近似梯度方向

---
# Optimization as Long Short-Term Memory network cell update
### 用一个共享的 LSTM（元优化器）来学习“如何更新参数”，然后在每个任务上，把“优化过程”看成 LSTM 在时间上的展开

---
# Optimization with Markov decision process and Reinforcement Learning
### 通过把优化视为一个 MDP，训练一个 RL 策略$\pi$，让它决定每一步参数更新动作，从而学习一个通用的优化算法

---
# Memory-augmented Neural Networks
## 训练时,先给出这一步的x和上一步的label,下一步再给出这一步的label,从而学会基于记忆的预测
**具体模型:NTMs:加入controller(FFN或LSTM),读取时使用加权平均数,写入时将x和label配对在一起***
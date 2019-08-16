## 介绍

### 学习目标

- 了解强化学习问题及其与监督学习的区别

### 摘要
- 强化学习（RL）是一种基于目标的学习方式。
- 在RL中，智能体通过与环境交互获得的经验来学习。 在监督学习中，我们不能影响环境。
- 在RL奖励中，奖励通常具有延迟性
- 智能体会尝试使得长期收益最大化。 例如，智能体可能需要做出看似当下次优的决策,以达到游戏获胜的目标。
- 智能体通过状态，动作和奖励与环境交互。

### 课件 & 视频

**Required:**

- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/RLbook2018.pdf) - Chapter 1: The Reinforcement Learning Problem
- David Silver's RL Course Lecture 1 - Introduction to Reinforcement Learning ([video](https://www.youtube.com/watch?v=2pWv7GOvuf0), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/intro_RL.pdf))
- [OpenAI Gym Tutorial](https://gym.openai.com/docs)

**自选的:**

N/A


### 练习

- [前往Openai](https://gym.openai.com/docs)

### 笔者的学习笔记
RL基本组成元素：
元素|定义
---|---
智能体(Agent)|本体(與环境交互)
环境(environment)|状态集的組成
状态(state)|表示從环境交互得到的数据
动作(action)|智能体做出的动作。动作集(智能体能做出的所有动作)
奖励(reward)|智能体執行一个动作后,获得的正/負奖励信号
策略(pi)|从环境状态到动作的映射,該映射关系称为策略
目标(target)|寻找连续时间序列里最优策略，最优策略通常指最大化长期累积奖励

与监督学习的区别
模型|学习方式|训练的数据类型
---|:--:|---:
监督学习|通过特征工程对数据进行提取，放进模型中训练出数据的表达模型分为训练和预测两阶段，学习只发生在训练阶段|。多样化的标签数据
强化学习|学习过程与生物自然学习更类似，通过不断探索和试错的方式，利用基于正/负奖励的方式进行学习|带有回报的交互数据

重大突破的时间线
时间|提出人|突破算法
---|:--:|---
1956年|Bellman|动态规划算法
1977年|Werbos|自适应动态规划算法
1988年|Sutton|时间差分算法
1992年|Watkins|Q-learning算法
1994年|Rummery|Saras算法
1996年|Bersekas|解决随机过程中优化控制的神经动态规划算法
2006年|Kocsis|置信上限树算法
2009年|Kewis|反馈控制自适应动态规划算法
2014年|Silver|确定性策略梯度（Policy Gradient）算法
2015年|Google DeepMind|Deep-Q-Network

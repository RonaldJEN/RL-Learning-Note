### 概述
本文提供了多种强化学习算法的代码,下面两本为推荐的补充材料：
- [Richard Sutton 和 Andrew Barto的《强化学习：简介（第二版）》](http://incompleteideas.net/book/RLbook2018.pdf)
- [David Silver 的强化学习课程](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)

Python版本  ：python3
强化学习环境 ：[OpenAI Gym](https://gym.openai.com/)
深度学习框架 ：[Tensorflow](https://www.tensorflow.org/) 

### 目录

- [介绍强化学习 & OpenAI Gym](Introduction/)
- [马尔可夫 & 贝尔曼方程 ](MDP/)
- [动态规划: 基于模型的RL, 策略迭代 ＆ 值迭代](DP/)
- [蒙特卡罗法-Free Prediction & Control](MC/)
- [时间差分法-Free Prediction & Control](TD/)
- [Function Approximation](FA/)
- [Deep Q Learning](DQN/) (WIP)
- [Policy Gradient Methods](PolicyGradient/) (WIP)
- Learning and Planning (WIP)
- Exploration and Exploitation (WIP)

### List of Implemented Algorithms
## 动态规划
- [动态规划_策略评估](DP/Policy%20Evaluation%20Solution.ipynb)
- [动态规划_策略迭代](DP/Policy%20Iteration%20Solution.ipynb)
- [动态规划_值迭代](DP/Value%20Iteration%20Solution.ipynb)

## 蒙特卡洛法
- [蒙特卡洛预测](MC/MC%20Prediction%20Solution.ipynb)
- [贪婪策略的蒙特卡罗](MC/MC%20Control%20with%20Epsilon-Greedy%20Policies%20Solution.ipynb)
- [抽样的蒙特卡罗（Off-Policy）](MC/Off-Policy%20MC%20Control%20with%20Weighted%20Importance%20Sampling%20Solution.ipynb)

## 时间差分法
- [SARSA (On Policy TD Learning)](TD/SARSA%20Solution.ipynb)
- [Q-Learning (Off Policy TD Learning)](TD/Q-Learning%20Solution.ipynb)
- [Q-Learning 线性函数逼近](FA/Q-Learning%20with%20Value%20Function%20Approximation%20Solution.ipynb)

## DQN及其变种
- [Deep Q-Learning (雅达利游戏)](DQN/Deep%20Q%20Learning%20Solution.ipynb)
- [Double Deep-Q Learning (雅达利游戏)](DQN/Double%20DQN%20Solution.ipynb)
- [Deep Q-Learning 优先经验回放 (施工中)

## 策略梯度
- [Policy Gradient: 基础板](PolicyGradient/CliffWalk%20REINFORCE%20with%20Baseline%20Solution.ipynb)
- [Policy Gradient: Actor-Critic板](PolicyGradient/CliffWalk%20Actor%20Critic%20Solution.ipynb)
- [Policy Gradient: 连续动作空间的Actor-Critic 算法](PolicyGradient/Continuous%20MountainCar%20Actor%20Critic%20Solution.ipynb)
- [连续动作空间的确定性策略梯度 (施工中)]
- [Deep Deterministic Policy Gradients (DDPG) (施工中)]
- [异步优势 Actor-Critic 算法 (A3C)](PolicyGradient/a3c)


### 资源

参考书:

- [Reinforcement Learning: An Introduction (2nd Edition)](http://incompleteideas.net/book/RLbook2018.pdf)

课程资料:

- [David Silver's Reinforcement Learning Course (UCL, 2015)](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)
- [CS294 - Deep Reinforcement Learning (Berkeley, Fall 2015)](http://rll.berkeley.edu/deeprlcourse/)
- [CS 8803 - Reinforcement Learning (Georgia Tech)](https://www.udacity.com/course/reinforcement-learning--ud600)
- [CS885 - Reinforcement Learning (UWaterloo), Spring 2018](https://cs.uwaterloo.ca/~ppoupart/teaching/cs885-spring18/)
- [CS294-112 - Deep Reinforcement Learning (UC Berkeley)](http://rail.eecs.berkeley.edu/deeprlcourse/)

相关访谈:

- [Introduction to Reinforcement Learning (Joelle Pineau @ Deep Learning Summer School 2016)](http://videolectures.net/deeplearning2016_pineau_reinforcement_learning/)
- [Deep Reinforcement Learning (Pieter Abbeel @ Deep Learning Summer School 2016)](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/)
- [Deep Reinforcement Learning ICML 2016 Tutorial (David Silver)](http://techtalks.tv/talks/deep-reinforcement-learning/62360/)
- [Tutorial: Introduction to Reinforcement Learning with Function Approximation](https://www.youtube.com/watch?v=ggqnxyjaKe4)
- [John Schulman - Deep Reinforcement Learning (4 Lectures)](https://www.youtube.com/playlist?list=PLjKEIQlKCTZYN3CYBlj8r58SbNorobqcp)
- [Deep Reinforcement Learning Slides @ NIPS 2016](http://people.eecs.berkeley.edu/~pabbeel/nips-tutorial-policy-optimization-Schulman-Abbeel.pdf)
- [OpenAI Spinning Up](https://spinningup.openai.com/en/latest/user/introduction.html)
- [Advanced Deep Learning & Reinforcement Learning (UCL 2018, DeepMind)](https://www.youtube.com/playlist?list=PLqYmG7hTraZDNJre23vqCGIVpfZ_K2RZs)


相关Papers:

- [Human-Level Control through Deep Reinforcement Learning (2015-02)](http://www.readcube.com/articles/10.1038/nature14236)
- [Deep Reinforcement Learning with Double Q-learning (2015-09)](http://arxiv.org/abs/1509.06461)
- [Continuous control with deep reinforcement learning (2015-09)](https://arxiv.org/abs/1509.02971)
- [Prioritized Experience Replay (2015-11)](http://arxiv.org/abs/1511.05952)
- [Dueling Network Architectures for Deep Reinforcement Learning (2015-11)](http://arxiv.org/abs/1511.06581)
- [Asynchronous Methods for Deep Reinforcement Learning (2016-02)](http://arxiv.org/abs/1602.01783)
- [Deep Reinforcement Learning from Self-Play in Imperfect-Information Games (2016-03)](http://arxiv.org/abs/1603.01121)
- [Mastering the game of Go with deep neural networks and tree search](https://gogameguru.com/i/2016/03/deepmind-mastering-go.pdf)

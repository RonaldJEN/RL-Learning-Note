## 马尔可夫 & 贝尔曼方程

### 学习目标

- 了解 Agent-Environment接口
- 了解 MDP（马尔可夫决策过程）是什么以及如何解释循环图
- 了解 值函数 ,动作-值函数,策略函数 
- 了解 值函数 ,动作-值函数的贝尔曼方程 和 贝尔曼最优方程 

### 摘要

- 智能体 & 环境 交互: 在每一步 `t` 智能体会收到状态 `S_t`, 并做出动作 `A_t` and 获得奖励 `R_{t+1}`. 动作的选择是来自策略函数 `pi`.

- 累积奖励 `G_t` 是从t时刻起,所有奖励的加总 . 未来收益会以折现率`gamma^k`进行折现.
- 马尔可夫性：环境在`t+1`时的状态仅受到时间`t`时刻的状态和动作影响,与时间步`t-1`以及`t-1`步之前的时间步都沒有关连性,即无后校性. 即使一个环境不能完全满足马尔可夫性，我们仍然把它看作是它,并试图将状态表示的方式,改进成近似马尔可夫。
- 马尔可夫决策过程 (MDP): 由状态集S，动作集A和单步dynamics `p(s',r | s,a)`定义. 如果我们完全了解环境，我们就知道转移概率. 在实践中，我们通常不知道完整的MDP（但我们知道它有的部分是MDP）。`MDP = (S,A,P_{sa},R)`

- 值函数 `v(s)` 估计一个状态其值有多好. 更正式的说,假设智能体处于状态`s`,他的值将就会是这状态未来的累积回报 `G_t` . 
`v(s) = Ex[G_t | S_t = s]`. 请注意，值函数的估计策略是来自`pi`。
- 动作-值函数: q(s, a) 估计一个状态和动作对其值有多好. 与值函数类似，但他考虑了动作
- 贝尔曼方程表达相邻状态 `v(s)`和 `v(s')`之间的关系. 他可以用"backup" diagram来表示. 贝尔曼方程在值函数和动作值函数之间都成立。
.<img src="https://github.com/RonaldJEN/Reinforcement_Learning/blob/master/pic/贝尔曼方程.png" width="664" height="90" />

- 值函数定义了一个策略好坏的判断方式. 对于所有状态s,如果`v_p1(s) >= v_p2(s)` 则策略`p1` 好于策略 `p2` .对于MDPs, 存在一个或多个优于或等于其他策略的最优策略
- 最优状态值函数 `v*(s)` 是最优策略的值函数. 对于最优状态动作函数 `q*(s, a)`也是如此. 贝尔曼最优性方程定义了最优的状态值如何与下一个最优的状态值相关。 他是“最大”而不是平均值。
.<img src="https://github.com/RonaldJEN/Reinforcement_Learning/blob/master/pic/贝尔曼最优方程.png" width="613" height="263" />

### 课件与视频

**Required:**

- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/RLbook2018.pdf) - Chapter 3: Finite Markov Decision Processes
- David Silver's RL Course Lecture 2 - Markov Decision Processes ([video](https://www.youtube.com/watch?v=lfHX2hHRMVQ), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/MDP.pdf))


### 练习

本章主要是理论，所以没有练习。

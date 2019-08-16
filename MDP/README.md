## 马尔可夫 & 贝尔曼方程

### 学习目标

- 了解 Agent-Environment接口
- 了解 MDP（马尔可夫决策过程）是什么以及如何解释循环图
- 了解 值函数 ,动作-值函数,策略函数 
- 了解 值函数 ,动作-值函数的贝尔曼方程 和 贝尔曼最优方程 

### Summary

- 智能体 & 环境 交互: 在每一步 `t` 智能体会收到状态 `S_t`, 并做出动作 `A_t` and 获得奖励 `R_{t+1}`. 动作的选择是来自策略函数 `pi`.

- 累積獎勵 `G_t` 是从t时刻起,所有奖励的加总 . 未来收益会以折现率`gamma^k`进行折现.
- Markov property: The environment's response at time `t+1` depends only on the state and action representations at time `t`. The future is independent of the past given the present. Even if an environment doesn't fully satisfy the Markov property we still treat it as if it is and try to construct the state representation to be approximately Markov.

- 马尔可夫性：环境在`t+1`时的状态仅受到时间`t`时刻的状态和动作影响。 未来与当前的过去无关。 即使一个环境不能完全满足马尔可夫性，我们仍然把它看作是它,并试图将状态表示的方式,改进成近似马尔可夫。

- Markov Decision Process (MDP): Defined by a state set S, action set A and one-step dynamics `p(s',r | s,a)`. If we have complete knowledge of the environment we know the transition dynamic. In practice, we often don't know the full MDP (but we know that it's some MDP).
- The Value Function `v(s)` estimates how "good" it is for an agent to be in a particular state. More formally, it's the expected return `G_t` given that the agent is in state `s`. `v(s) = Ex[G_t | S_t = s]`. Note that the value function is specific to a given policy `pi`.
- Action Value function: q(s, a) estimates how "good" it is for an agent to be in states and take action a. Similar to the value function, but also considers the action.
- The Bellman equation expresses the relationship between the value of a state and the values of its successor states. It can be expressed using a "backup" diagram. Bellman equations exist for both the value function and the action value function.
- Value functions define an ordering over policies. A policy `p1` is better than `p2` if `v_p1(s) >= v_p2(s)` for all states s. For MDPs, there exist one or more optimal policies that are better than or equal to all other policies.
- The optimal state value function `v*(s)` is the value function for the optimal policy. Same for `q*(s, a)`. The Bellman Optimality Equation defines how the optimal value of a state is related to the optimal value of successor states. It has a "max" instead of an average.


### 课件与视频

**Required:**

- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/RLbook2018.pdf) - Chapter 3: Finite Markov Decision Processes
- David Silver's RL Course Lecture 2 - Markov Decision Processes ([video](https://www.youtube.com/watch?v=lfHX2hHRMVQ), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/MDP.pdf))


### 练习

本章主要是理论，所以没有练习。

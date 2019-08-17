## 动态规划: 基于模型的RL, 策略迭代 ＆ 值迭代

### 学习目标

 - 了解策略评估和策略改进之间的区别以及这些流程如何相互作用
 - 了解策略迭代算法
 - 理解值迭代算法
 - 理解动态规划方法的局限性

### 摘要

- 动态规划(DP) ：假设我们有一个完美的环境马尔可夫决策过程模型（MDP）。在实践中通常情况并非如此，但无论如何研究DP都很重要。
- 策略评估: 计算给定策略`pi`的状态值函数 `V(s)` . 在DP中, 他是使用"full backup"完成的. 在每一个状态, 我们展望每个可能的动作和下一步状态. 我们能这样做，是因为我们拥有完美的MDP模型。
- "full backup(反向更新)：full backup过程和贝尔曼方程很像,只不过是把贝尔曼方程转化成了赋值规则。当backup计算不再变化时，说明这个时候的状态值已经收敛到可以满足贝尔曼方程了。
- 策略改进: 基于一个确定策略的状态值函数,我们可以采用greedily法来选择动作(即在每个状态下采取最佳行动).然后当策略不再改进时,我们可以保证这个策略已经是最优的.
- 策略迭代: 循环执行策略评估和策略改进，直到达到最优策略。
- 值迭代: 我们只需要执行一个步骤并立即改进策略,而不是执行多个步骤的策略评估去找到正确的V(s)值. 在实践中,这種收敛更快。
- 广义策略迭代: 循环进行策略评估和改进的过程。我们可以为每个步骤选择不同的算法，但基本思路保持不变。
- 动态规划法bootstrap(自举法): 根据其他的估计值更新估计值 (one step ahead).
### 课件与视频

**Required:**

- David Silver's RL Course Lecture 3 - Planning by Dynamic Programming ([video](https://www.youtube.com/watch?v=Nd1-UUMVfz4), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/DP.pdf))

**Optional:**

- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/RLbook2018.pdf) - Chapter 4: Dynamic Programming


### Exercises

- 实现策略评估 in Python (Gridworld)
  - [Exercise](Policy%20Evaluation.ipynb)
  - [Solution](Policy%20Evaluation%20Solution.ipynb)

- 实现策略迭代 in Python (Gridworld)
  - [Exercise](Policy%20Iteration.ipynb)
  - [Solution](Policy%20Iteration%20Solution.ipynb)

- 实现值迭代   in Python (Gridworld)
  - [Exercise](Value%20Iteration.ipynb)
  - [Solution](Value%20Iteration%20Solution.ipynb)

- 实现赌徒问题
  - [Exercise](Gamblers%20Problem.ipynb)
  - [Solution](Gamblers%20Problem%20Solution.ipynb)

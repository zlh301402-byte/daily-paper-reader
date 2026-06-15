---
title: Wasserstein Policy Optimization
title_zh: Wasserstein策略优化
authors: "David Pfau, Ian Davies, Diana L Borsa, João Guilherme Madeira Araújo, Brendan Daniel Tracey, Hado van Hasselt"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=oAKe7MG9GM"
tags: ["query:drone-arm"]
score: 7.0
evidence: 通用的连续控制演员-评论家RL算法，适用于机器人臂控制中的强化学习
tldr: 针对连续动作空间中的强化学习，本文提出Wasserstein策略优化（WPO），一种从Wasserstein梯度流推导的演员-评论家算法。WPO兼具确定性策略梯度利用动作值函数梯度和经典策略梯度支持任意分布的优势，无需重参数化技巧。实验表明其在连续控制任务上性能优异，为机械臂控制等场景提供了强大的RL算法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1403, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1674, \"height\": 386, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1670, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1679, \"height\": 960, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1766, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1425, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1392, \"height\": 2141, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 508, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 523, \"height\": 671, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1391, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1394, \"height\": 2142, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oake7mg9gm/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1394, \"height\": 2143, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1167, \"height\": 662, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 616, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 691, \"height\": 402, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 592, \"height\": 145, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 861, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oake7mg9gm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1021, \"height\": 383, \"label\": \"Table\"}]"
motivation: 在连续动作空间中，确定性策略梯度局限于确定性策略，而经典策略梯度效率较低，需要统一两者的优势。
method: 通过近似Wasserstein梯度流推导出适用于任何分布的无重参数化演员-评论家更新规则。
result: 在标准连续控制基准上，WPO达到或超过当前最优算法，且实现简单。
conclusion: WPO提供了一种通用、高效的连续控制RL算法，易于部署到实际系统。
---

## Abstract
We introduce Wasserstein Policy Optimization (WPO), an actor-critic algorithm for reinforcement learning in continuous action spaces. WPO can be derived as an approximation to Wasserstein gradient flow over the space of all policies projected into a finite-dimensional parameter space (e.g., the weights of a neural network), leading to a simple and completely general closed-form update. The resulting algorithm combines many properties of deterministic and classic policy gradient methods. Like deterministic policy gradients, it exploits knowledge of the *gradient* of the action-value function with respect to the action. Like classic policy gradients, it can be applied to stochastic policies with arbitrary distributions over actions -- without using the reparameterization trick. We show results on the DeepMind Control Suite and a magnetic confinement fusion task which compare favorably with state-of-the-art continuous control methods.

---

## 论文详细总结（自动生成）

# Wasserstein Policy Optimization（WPO）论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：在连续动作空间的强化学习中，存在两大策略梯度方法：
  - **经典策略梯度**（如REINFORCE、PPO）：支持任意随机策略，但仅使用标量值（如Q值）作为权重，未利用Q函数对动作的梯度，效率较低。
  - **确定性策略梯度（DPG）**：利用Q函数关于动作的梯度，更新高效，但仅适用于确定性策略，不利于探索；后续扩展（如SVG(0)、SAC）需依赖重参数化技巧，限制了策略分布的选择。
  - 现有方法无法兼具两者优势：即同时利用动作值梯度、支持任意随机策略、且无需重参数化。
- **整体含义**：提出Wasserstein策略优化（WPO），从最优传输理论中的Wasserstein梯度流出发，推导出一种新的演员-评论家更新规则，它自然融合了DPG对动作梯度的利用和经典策略梯度对任意分布的适用性。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想
- 将策略优化视作在概率测度空间（策略的空间）上的Wasserstein梯度流，从而得到连续时间下的演化偏微分方程（PDE）：
  \[
  \frac{\partial \pi}{\partial t} = -\nabla_a \cdot \left( \pi \, (-\nabla_a \frac{\delta J}{\delta \pi}) \right)
  \]
  其中 \(J[\pi]\) 是期望回报，\(\frac{\delta J}{\delta \pi} = \frac{1}{1-\gamma} Q^\pi(s,a) d^\pi(s)\) 是泛函导数。
- 将该连续流投影到有限维参数空间（如神经网络权重），通过最小化KL散度近似，得到闭式更新：
  \[
  \theta_{t+1} = \theta_t + F_{\theta\theta}^{-1} \, \mathbb{E}_{a\sim\pi}[\nabla_\theta \nabla_a \log \pi(a|s) \, \nabla_a Q^\pi(s,a)]
  \]
  其中 \(F_{\theta\theta}\) 是Fisher信息矩阵。

### 2.2 关键技术细节
- **近似Fisher信息矩阵**：对于对角高斯策略，Fisher矩阵对角元为 \(1/\sigma_i^2\)（均值）和 \(2/\sigma_i^2\)（标准差）。直接使用缩放后的“修正”梯度（乘以方差）替代完整自然梯度，避免数值不稳定。
- **KL正则化**：添加KL散度惩罚项（软约束或硬约束），防止策略过早坍缩为确定性，同时使用独立的正则化权重控制均值和方差的更新步长。
- **适用于任意分布**：推导不依赖重参数化，可直接用于混合高斯等非重参数化分布。
- **与现有方法关系**：在高斯情况下，WPO更新期望等价于经典策略梯度，但方差更低；在混合高斯举例中，WPO收敛更快、更稳定。

## 3. 实验设计

### 3.1 数据集/场景与基准
- **DeepMind Control Suite**：包含多个连续控制任务（如Cartpole、Acrobot、Humanoid、Dog等），动作维度从1到56维。
- **Tokamak磁约束聚变控制任务**：模拟TCV托卡马克的等离子体形状控制（19个动作维度，93个观测）。
- **组合任务**：将多个Humanoid Stand环境复制并联（1、3、5个副本，对应21、65、105动作维度），用于测试高维动作空间下的扩展性。

### 3.2 对比方法
- **DDPG**（确定性策略梯度）
- **SAC**（软演员-评论家，使用重参数化技巧）
- **MPO**（最大后验策略优化，基于EM思路的KL约束方法）

### 3.3 实验设置
- 分布式RL框架：4个并行演员（Control Suite）/ 1000个演员（聚变任务）。
- 所有算法均使用相同网络结构（Actor: [256,256,128]；Critic: [512,512,256]）、优化器（Adam）、学习率（3e-4）、折扣因子（0.99）等公共超参数。
- WPO和MPO使用离策略采样（从重放缓冲取状态，但动作从当前策略重新采样）。
- 每个任务运行5-10个随机种子，报告平均回报及最小/最大范围。

## 4. 资源与算力
- **论文未明确说明**具体的GPU型号、数量及训练总时长。仅提到使用分布式RL系统（Acme框架），Control Suite使用4个演员，聚变任务使用1000个演员。未提供硬件配置细节。

## 5. 实验数量与充分性

### 5.1 实验数量
- **Control Suite**：在49个任务上（排除LQR），对比了WPO、DDPG、SAC、MPO；并针对MPO做了额外超参数对比（图11）。
- **组合任务**：3种不同副本数（1/3/5），每种对比4种算法，各5个种子。
- **聚变任务**：2种变体（原始任务和精炼任务），对比WPO和MPO。
- **消融实验**：测试了不同激活函数（ELU vs SiLU）、是否使用立方根压扁函数（cube-root squashing）对WPO的影响（图12）。

### 5.2 实验充分性与公平性
- **充分性**：覆盖了从低维到高维、从稀疏奖励到密集奖励、从完全观测到部分观测（Dog任务）的多种场景，实验范围较广。
- **公平性**：为每个算法独立调参（WPO和MPO经过多年调参；DDPG和SAC也做了超参搜索）。在MPO与WPO对比中，额外验证了MPO在WPO超参数设置下的表现无明显变化，排除了超参数差异的影响。
- **局限性**：WPO未在所有任务上优于所有基线，但在大部分任务上表现与MPO相当或更好，且明显优于DDPG和SAC（它们在部分任务未能学习）。

## 6. 主要结论与发现

1. **WPO是一种有效的连续控制RL算法**：在49个Control Suite任务上，WPO学习稳定，收敛性能与SOTA（MPO）相当，远好于DDPG和SAC。
2. **高维动作空间优势**：在组合Humanoid任务中，随着动作维度增加（21→105），WPO相比MPO和DDPG的早期学习速度优势更显著。
3. **聚变控制应用**：在磁约束聚变任务上，WPO取得与MPO相近的回报，且表明策略方差自然收敛到较小值（MPO维持较大方差），更适合确定性控制。
4. **理论贡献**：提供了从Wasserstein梯度流到参数化策略更新的完整推导，澄清了与经典策略梯度和DPG的关系。

## 7. 优点

- **创新性理论推导**：首次将Wasserstein梯度流框架应用于通用演员-评论家算法，导出简洁闭式更新。
- **统一性**：该更新无需重参数化，适用于任意分布（如混合高斯、指数分布等），而SVG(0)/SAC受限。
- **鲁棒性**：在广泛任务上无需精细调参即可取得良好性能，尤其在高维动作空间下学习速度快。
- **实验设计全面**：包含标准benchmark、高维扩展、实际物理控制任务，并进行了充分的消融和超参数敏感性分析。
- **开放实现**：提供了Acme框架下的开源实现（注意：实验版本非Acme版本，但效果定性一致）。

## 8. 不足与局限

- **未超越MPO基线**：在多数Control Suite任务上性能与MPO相当，未展现压倒性优势。部分任务（如Dog）收敛速度慢于MPO，可能受部分观测影响。
- **高维优势仅体现在早期学习速度**：在最终收敛性能上，各方法差异不大；仅在学习曲线早期的斜率上体现优势。
- **计算资源未报告**：缺乏算力需求细节，不利于可复现性评估（如GPU型号、训练时长等）。
- **KL正则化依赖**：WPO仍依赖KL惩罚来防止策略坍缩，而理论上更优的Wasserstein距离正则化未实现，留有改进空间。
- **超参数敏感性**：虽然WPO相对鲁棒，但方差正则化权重、动作值梯度压扁函数、激活函数等选择仍影响部分任务性能，需依赖经验调优。
- **仅验证了高斯和混合高斯策略**：虽然理论支持任意分布，但实验中仅使用对角高斯和混合高斯（一维例子），未充分展示其在非高斯分布（如指数、Beta等）上的实用性。
- **缺乏统计显著性检验**：未提供置信区间或成对比较的统计检验（如t检验），仅展示均值与极值范围。

（完）

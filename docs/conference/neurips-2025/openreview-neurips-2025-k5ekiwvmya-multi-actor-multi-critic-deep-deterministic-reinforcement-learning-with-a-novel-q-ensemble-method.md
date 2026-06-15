---
title: Multi-Actor Multi-Critic Deep Deterministic Reinforcement Learning with a Novel Q-Ensemble Method
title_zh: 基于新颖Q集成方法的多智能体多评论家深度确定性强化学习
authors: "Andy Wu, Chun-Cheng Lin, Rung-Tzuo Liaw, Yuehua Huang, Chihjung Kuo, Chia-Tong Weng"
date: 2025-05-10
pdf: "https://openreview.net/pdf?id=k5ekIwvmYA"
tags: ["query:drone-arm"]
score: 5.0
evidence: 多智能体多评论家深度确定性强化学习方法可用于机器人手臂控制
tldr: 针对强化学习中值函数高估低估问题，提出多智能体多评论家深度确定性强化学习框架。通过新颖的Q集成方法提高策略评估准确性，在连续控制任务上取得了更优的收敛性能和稳定性，为复杂控制系统提供了一种有效的学习算法。
source: NeurIPS-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5ekiwvmya/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1396, \"height\": 545, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5ekiwvmya/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1422, \"height\": 211, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-k5ekiwvmya/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1418, \"height\": 408, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5ekiwvmya/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1379, \"height\": 339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5ekiwvmya/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1215, \"height\": 629, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5ekiwvmya/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1208, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5ekiwvmya/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-k5ekiwvmya/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1386, \"height\": 177, \"label\": \"Table\"}]"
motivation: 现有方法缺乏多智能体多评论家架构的探索，且值函数估计不准确。
method: 提出多智能体多评论家架构，结合Q集成方法提高策略评估精度。
result: 在连续控制任务上取得了更优的收敛性能和稳定性。
conclusion: 多智能体多评论家架构结合Q集成能有效提升深度强化学习在控制问题中的表现。
---

## Abstract
Abstract Reinforcement learning has gathered much attention in recent years due to its rapid development and rich applications, especially on control systems and robotics. When tackling real-world applications with reinforcement learning method, the corresponded Markov decision process may have huge discrete or even continuous state/action space. Deep reinforcement learning has been studied for handling these issues through deep learning for years, and one promising branch is the actor-critic architecture. Many past studies leveraged multiple critics to enhance the accuracy of evaluation of a policy for addressing the overestimation and underestimation issues. However, few studies have considered the architecture with multiple actors together with multiple critics. This study proposes a novel multi-actor multi-critic (MAMC) deep deterministic reinforcement learning method. The proposed method has three main features, including selection of actors based on non-dominated sorting for exploration with respect to skill and creativity factors, evaluation for actors and critics using a quantile-based ensemble strategy, and exploiting actors with best skill factor. Theoretical analysis proves the learning stability and bounded estimation bias for the MAMC. The present study examines the performance on a well-known reinforcement learning benchmark MuJoCo. Experimental results show that the proposed framework outperforms state-of-the-art deep deterministic based reinforcement learning methods. Experimental analysis also indicates the proposed components are effective. Empirical analysis further investigates the validity of the proposed method, and shows its benefit on complicated problems.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：深度强化学习在连续控制任务中面临值函数估计偏差问题（高估或低估）。现有方法多采用多个评论家（critic）来提高评估精度，但对同时使用多个演员（actor）的研究很少。作者认为，多演员-多评论家架构能够更好地平衡探索与利用，提升学习稳定性和估计准确性。
- **整体含义**：提出一种新的多演员多评论家深度确定性强化学习方法（MAMC），通过新颖的Q集成方法（分位数集成）结合多演员选择策略，旨在解决值函数估计偏差，并加速在复杂连续控制环境中的收敛。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：同时维护多个actor网络和多个critic网络，通过分位数集成构建目标值，利用非支配排序（基于技能因子和创造力因子）选择最合适的actor与环境交互，从而提升探索效率和学习稳定性。
- **关键技术细节**：
  - **分位数集成目标值构建**：对于每个transition，先计算每个actor对应的多个critic目标值，取其`q`分位数作为该actor的状态值估计`ˆV_ϕ_i(s';C')`，再对所有actor的状态值取中位数作为最终的TD目标`y(s,a) = r + γ * median(ˆV_ϕ_i)`。这种两步集成降低了方差和偏差。
  - **多actor/critic训练**：每个critic独立采样mini-batch，使用上述目标值更新自身；每个actor依次由不同critic引导（轮换），采用标准actor损失函数。
  - **采样多次复用（SMR）**：每个mini-batch重复利用M次更新，增强样本效率。
  - **演员选择与利用**：
    - **技能因子**：actor在mini-batch上的平均分位数状态值（越高表示越擅长当前任务）。
    - **创造力因子**：actor在各critic上的分位数与各critic原始值的平均绝对误差（越大表示输出多样性高）。
    - 使用非支配排序（NSGA-II中的拥挤比较算子）在上述两个目标上选择前√NA个actor作为候选集，再从中随机选取一个进行环境交互。
    - 同时记录具有最高技能因子的actor作为最优策略，用于最终推理。
- **算法流程**（算法1）：初始化NA个actor、NC个critic及目标网络；循环中依次执行：critic学习（采样M次更新+软更新）、actor学习（轮换critic引导）、探索（选择actor与环境交互并存入回放缓冲区）；最终返回技能因子最高的actor。

## 3. 实验设计

- **数据集/场景**：使用MuJoCo基准中的五个连续控制环境，难度从简单到困难：
  - Hopper-v5（简单）
  - HalfCheetah-v5、Walker2d-v5（中等）
  - Ant-v5、Humanoid-v5（困难）
- **对比方法**：四种最新RL方法，均采用SMR版本以保证公平比较：
  - TD3-SMR（确定性策略，单actor双critic）
  - DARC-SMR（确定性策略，双actor双critic）
  - SAC-SMR（随机策略，单actor双critic）
  - REDQ-SMR（随机策略，单actor十critic）
- **评价指标**：平均回报随时间步的变化，以及早期（100k）、中期（200k）、晚期（300k）阶段的Wilcoxon符号秩检验。

## 4. 资源与算力

- 根据论文补充材料（Section A.2），所有实验在一台服务器上运行，配置为：
  - CPU: Intel Xeon W7-2475X (2.6 GHz, 20核40线程)
  - GPU: 2块NVIDIA RTX 4090（每块24GB显存）
  - 内存：128GB
- 未明确给出单个实验的训练时长或总计算量，但提及每个实验运行10次试验，每次试验平均20个种子（即每个环境方法组合约200次运行），结合五个环境与五种方法，总计算量较大。

## 5. 实验数量与充分性

- **实验数量**：
  - 主对比实验：5个环境 × 4个基线 × 10 trials × 20 seeds = 4000次运行（加上MAMC本身，共5种方法）。
  - 消融实验：对比单目标最优选择（SO）与多目标选择（MO）在Ant-v5上的表现（8 trials）。
  - 敏感性分析：针对分位数参数q（0.1~0.5）在HalfCheetah和Walker2d上的表现。
  - 有效性分析：定性展示最佳/最差/被选actor的回报曲线。
  - 此外还包括超参数分析（如actor/critic数目）在补充材料中。
- **充分性**：实验设计相对全面，覆盖了不同难度环境、多种基线、统计显著性检验（Wilcoxon）、组件消融和参数敏感性。但仅使用MuJoCo一个基准，未在Atari或其他连续控制任务上验证。统计检验方法合理（符号秩检验，显著性水平0.05），误差条为均值±标准差，多次重复种子设置增强了结果可靠性。

## 6. 论文的主要结论与发现

- MAMC在早期（100k步）和中期（200k步）显著优于确定性方法TD3-SMR和DARC-SMR，也优于随机策略SAC-SMR；但对REDQ-SMR优势不明显，甚至在某些环境（Hopper-v5、Humanoid-v5）晚期被反超。
- 收敛速度更快：在Walker2d、Ant、Humanoid三个较复杂环境中，MAMC回报曲线上升快于TD3-SMR、DARC-SMR和SAC-SMR。
- 多目标选择（技能+创造力）相比单目标加权（SO）在Ant-v5上回报更高，验证了其有效性。
- 分位数参数q的最佳取值与环境偏好相关：乐观环境偏好较大q（如0.4~0.5），悲观环境偏好较小q（如0.2~0.3），推荐稳健值约0.3。
- 理论分析表明MAMC的方差小于单演员或单评论家架构，估计误差介于极限情况之间，具有有界性，保证了学习稳定性。

## 7. 优点

- **方法创新**：首次系统性提出多演员-多评论家架构，并引入非支配排序选择actor，兼顾技能（高质量）与创造力（多样性），是一种新颖的探索-利用平衡机制。
- **理论贡献**：证明了目标值方差降低和估计误差有界，为方法可靠性提供了理论支撑。
- **实验设计全面**：对比四种先进方法（确定性+随机性），使用公平的SMR版本，包含统计检验、消融、敏感性分析，结果可信。
- **代码开源**：提供匿名GitHub仓库，便于复现。

## 8. 不足与局限

- **实验覆盖有限**：仅测试MuJoCo连续控制任务，未在离散动作环境（如Atari）或其他连续控制基准（如DMControl）上验证，泛化性有待确认。
- **计算开销**：使用10个actor和10个critic，训练成本远高于单actor双critic方法，文中未提供具体的计算时间对比或效率分析。
- **对确定性策略依赖**：作者指出随机策略（如REDQ）在某些环境下表现更好，MAMC作为确定性方法存在本质劣势，未来方向可结合随机策略。
- **分位数参数敏感**：最佳q值依赖环境，需要调整，缺乏自适应策略。稳健值0.3并非通用最优。
- **晚期性能提升有限**：在300k步时，MAMC与对比方法的差距缩小甚至被反超，说明长期学习潜力可能不如高效随机方法。
- **理论分析简化**：假设critic之间独立同分布等理想条件，实际中可能不满足。

（完）

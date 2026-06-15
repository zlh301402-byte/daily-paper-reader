---
title: "MENTOR: Mixture-of-Experts Network with Task-Oriented Perturbation for Visual Reinforcement Learning"
title_zh: MENTOR：用于视觉强化学习的混合专家网络与任务导向扰动
authors: "Suning Huang, Zheyu Aqa Zhang, Tianhai Liang, Yihan Xu, Zhehao Kou, Chenhao Lu, Guowei Xu, Zhengrong Xue, Huazhe Xu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=t46uezeQH8"
tags: ["query:drone-arm"]
score: 7.0
evidence: 用于机器人操控任务的视觉RL架构
tldr: "该论文针对视觉深度强化学习样本效率低的问题，提出MENTOR方法，用混合专家网络替代标准MLP，并引入任务导向扰动机制。在三个仿真基准和三个真实机器人操控任务上，MENTOR分别达到平均83%的成功率，远超基线方法的32%。该方法直接适用于机械臂控制，可迁移至空中机械臂场景。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 850, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1554, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1610, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1370, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1574, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1609, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1595, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 620, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1743, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1311, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1427, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1216, \"height\": 630, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 591, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 566, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 764, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-t46uezeqh8/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 836, \"height\": 209, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 853, \"height\": 717, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1352, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 860, \"height\": 783, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1478, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1470, \"height\": 1604, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 316, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 997, \"height\": 151, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-t46uezeqh8/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 604, \"height\": 239, \"label\": \"Table\"}]"
motivation: 现有视觉RL算法样本效率低，难以实际应用。
method: 以混合专家网络为骨干，添加任务导向扰动改进优化。
result: 在仿真和真实机器人操控任务上显著优于现有方法。
conclusion: 改进架构和优化策略能大幅提升视觉RL的样本效率和性能。
---

## Abstract
Visual deep reinforcement learning (RL) enables robots to acquire skills from visual input for unstructured tasks. However, current algorithms suffer from low sample efficiency, limiting their practical applicability. In this work, we present MENTOR, a method that improves both the *architecture* and *optimization* of RL agents. Specifically, MENTOR replaces the standard multi-layer perceptron (MLP) with a mixture-of-experts (MoE) backbone and introduces a task-oriented perturbation mechanism. MENTOR outperforms state-of-the-art methods across three simulation benchmarks and achieves an average of 83\% success rate on three challenging real-world robotic manipulation tasks, significantly surpassing the 32% success rate of the strongest existing model-free visual RL algorithm. These results underscore the importance of sample efficiency in advancing visual RL for real-world robotics. Experimental videos are available at https://suninghuang19.github.io/mentor_page/.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：视觉深度强化学习（Visual RL）在机器人操控任务中依赖高维图像输入，但现有算法样本效率极低，导致难以直接在真实世界从头训练，往往需要先模拟再迁移，面临Sim-to-Real差距。
- **重要性**：提升样本效率是使视觉RL在真实机器人场景中实用化的关键。
- **本文贡献**：提出MENTOR，通过**改进网络架构**（用混合专家网络MoE替代标准MLP）和**优化方法**（任务导向扰动机制）显著提升样本效率，在仿真和真实世界任务上均达到SOTA。

## 2. 论文提出的方法论
### 核心思想
- **架构层面**：将策略网络中的MLP替换为MoE层，通过稀疏路由动态激活不同专家，缓解梯度冲突（gradient conflict）。
- **优化层面**：引入任务导向扰动（Task-Oriented Perturbation），从历史高性能agent的权重分布中采样扰动候选，替代纯随机噪声，提供更有效的探索方向。

### 关键技术细节
- **MoE架构**：
  - 输入通过CNN提取特征后，由路由器计算专家选择概率，激活top-k专家，加权组合输出。
  - 辅助负载均衡损失（防止专家退化）：负熵损失最小化专家使用不均。
- **任务导向扰动**：
  - 维护一个固定大小的候选集`S_top`，存储历史最优agent的权重和奖励。
  - 扰动分布`Φ_oriented = N(μ_top, σ_top)`，其中均值和标准差由`S_top`计算得到。
  - 扰动公式：`θ_t = α θ_{t-1} + (1-α) ϕ`，其中`α`由休眠比率（dormant ratio）动态调整，`ϕ`从`Φ_oriented`采样。
- **休眠比率机制**：沿用DrM中的定义，根据神经元活跃程度调整扰动强度。

## 3. 实验设计
### 仿真场景（Benchmark）
- **DeepMind Control Suite (DMC)**：Dog Stand, Dog Walk, Manipulator Bring Ball, Acrobot Swingup (Sparse)
- **Meta-World (MW)**：Assembly, Disassemble, Pick Place, Coffee Push (Sparse), Soccer (Sparse), Hammer (Sparse)
- **Adroit**：Door, Hammer
- **评价指标**：DMC用episode reward，MW和Adroit用success rate。

### 真实世界任务
- **Peg Insertion（三形状插入）**：Star, Triangle, Arrow三种peg。
- **Cable Routing（线缆路由）**：将线缆依次放入两个非平行槽中。
- **Tabletop Golf（桌面高尔夫）**：击球入洞并避开障碍。

### 对比方法
- DrM（2023）、DrQ-v2（2021）、ALIX（2022）、TACO（2023），均为model-free视觉RL方法。

## 4. 资源与算力
- **GPU型号**：Nvidia RTX 3090（文中明确提及）。
- **训练时长**：未明确每个任务的具体训练步数或小时数，但附录表6显示了每个真实任务训练时对应的FPS（0.4~0.6 FPS），且附录图14给出了DrM达到MENTOR同等性能所需的训练时间对比（平均37%更多时间）。仿真任务FPS在附录表5中给出（Hopper Hop任务：MENTOR 37 FPS vs DrM 55 FPS）。未说明GPU数量或分布式训练情况。

## 5. 实验数量与充分性
- **仿真实验**：共12个任务，每个任务用4个随机种子，曲线显示均值与方差/范围。覆盖多个环境（DMC、MW、Adroit），包含稀疏奖励和长视距任务。
- **消融实验**：
  - 分别移除MoE或任务扰动（附录C图9），在4个任务上比较。
  - 多任务实验（附录G）在Meta-World多任务组合上验证MoE优势。
  - 真实世界消融（表1）：对比MENTOR、MENTOR w/o MoE、DrM、预训练编码器等。
- **鲁棒性测试**：仿真中加入随机扰动（附录I图16），真实世界人为干扰（图7）。
- **充分性评估**：实验设置合理，对比基线最新，消融完备，统计量（多个随机种子）使用恰当。但真实世界任务仅执行少量rollout（表1：Peg Insertion每子任务10次，其他20次），统计量偏弱。

## 6. 主要结论与发现
- MENTOR在所有12个仿真任务上优于所有基线，尤其在稀疏奖励和高维动作空间（Dog任务）提升显著。
- 真实世界任务：MENTOR平均83%成功率，显著优于最强基线DrM的32%。
- MoE有效缓解梯度冲突（通过余弦相似度实验验证）。
- 任务导向扰动比随机扰动更有效，扰动候选的奖励随时间提升，甚至超越当前agent。

## 7. 优点
- **方法新颖性**：首次将MoE引入model-free视觉RL，并设计任务导向扰动，两者互补。
- **架构优势**：MoE动态路由自动分解任务阶段，减少共享参数负担。
- **实验全面**：涵盖仿真和真实世界，包括多任务、稀疏奖励、接触丰富任务。
- **真实世界验证**：三个挑战性任务直接从头训练，无需演示或模拟，体现算法实用性。
- **消融深入**：量化梯度冲突、专家使用模式、扰动候选质量等。

## 8. 不足与局限
- **时间效率**：MoE导致推理速度下降（附录表5：MENTOR在Hopper Hop上FPS为37，低于DrM的55），限制了实时应用。
- **实验覆盖**：
  - 仿真任务有限，未在Atari或其他视觉RL经典环境上测试。
  - 真实世界任务仅各一个机器人，单种机械臂（Franka Panda），未验证多机器人或多物体泛化。
  - 扰动候选集大小固定为10，未探讨敏感性。
- **计算资源**：未报告总训练时长或GPU数量，难以复现成本。
- **理论分析**：对于MoE为何在单任务中缓解梯度冲突，论证较直观，缺少严格理论证明。
- **潜在偏差**：真实世界任务奖励设计依赖手工分类器或位置估计，可能引入偏见；初始位置随机化但未公开所有随机种子的成功率分布。

（完）

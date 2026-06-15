---
title: A Forget-and-Grow Strategy for Deep Reinforcement Learning Scaling in Continuous Control
title_zh: 面向深度强化学习连续控制扩展的遗忘与增长策略
authors: "Zilin Kang, Chenyuan Hu, Yu Luo, Zhecheng Yuan, Ruijie Zheng, Huazhe Xu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=VhmTXbsdtx"
tags: ["query:drone-arm"]
score: 6.0
evidence: 解决RL连续控制中初始偏见的遗忘增长策略，可应用于机械臂控制
tldr: 深度强化学习在连续控制中常因初始经验过拟合而受限。受人类婴儿遗忘启发，提出遗忘与增长策略，在训练中周期性重置并增长网络，有效缓解初始偏见。在多个连续控制任务上，该方法显著提高了样本效率和泛化能力。该策略可广泛适用于机器人控制等连续动作空间问题。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 853, \"height\": 1644, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 851, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1736, \"height\": 1096, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 850, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 807, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 855, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1720, \"height\": 1456, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1746, \"height\": 365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 866, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 862, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 853, \"height\": 306, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 886, \"height\": 808, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1403, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1776, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1776, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1780, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1780, \"height\": 797, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1784, \"height\": 1192, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1783, \"height\": 1495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 888, \"height\": 386, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhmtxbsdtx/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 896, \"height\": 826, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 985, \"height\": 896, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1172, \"height\": 422, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1504, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1432, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1376, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1155, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhmtxbsdtx/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1509, \"height\": 702, \"label\": \"Table\"}]"
motivation: 深度RL中初始偏见导致样本效率低，而现有重置方法效果有限。
method: 提出遗忘与增长机制，在训练过程中周期性重置部分网络参数并添加新神经元，模仿人类遗忘。
result: 在MuJoCo连续控制任务上，相比基线方法显著提升了性能。
conclusion: 遗忘与增长策略是一种简单有效的缓解初始偏见的方法，可扩展至各类连续控制任务。
---

## Abstract
Deep reinforcement learning for continuous control has recently achieved impressive progress. However, existing methods often suffer from primacy bias—a tendency to overfit early experiences stored in the replay buffer—which limits an RL agent’s sample efficiency and generalizability. A common existing approach to mitigate this issue is periodically resetting the agent during training. Yet, even after multiple resets, RL agents could still be impacted by early experiences. In contrast, humans are less susceptible to such bias, partly due to *infantile amnesia*, where the formation of new neurons disrupts early memory traces, leading to the forgetting of initial experiences. Inspired by this dual processes of forgetting and growing in neuroscience, in this paper, we propose *Forget and Grow* (**FoG**), a new deep RL algorithm with two mechanisms introduced. First, *Experience Replay Decay (ER Decay)*—"forgetting early experience''—which balances memory by gradually reducing the influence of early experiences. Second, *Network Expansion*—"growing neural capacity''—which enhances agents' capability to exploit the patterns of existing data by dynamically adding new parameters during training. Empirical results on four major continuous control benchmarks with more than 40 tasks demonstrate the superior performance of **FoG** against SoTA existing deep RL algorithms, including BRO, SimBa and TD-MPC2.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：深度强化学习（DRL）在连续控制任务中取得了显著进展，但现有方法普遍存在 **“首因偏差”（primacy bias）**——即智能体过度拟合回放缓冲区中的早期经验，导致样本效率和泛化能力受限。早期的“网络重置”方法（如周期性重置部分参数）虽能部分缓解，但无法彻底消除该问题，因为旧样本仍会被更频繁地采样，造成不平衡。
- **生物学启发**：人类婴儿的“婴儿期遗忘”现象——海马体在幼年时期产生大量新神经元，破坏原有记忆痕迹，导致早期记忆被遗忘——为缓解首因偏差提供了灵感。论文借鉴了这种“遗忘+生长”的双重过程。
- **整体含义**：提出了一种名为 **Forget and Grow (FoG)** 的深度强化学习算法，通过引入经验回放衰减（模拟遗忘）和网络扩展（模拟生长）两种机制，有效缓解首因偏差，提升模型在连续控制任务中的表现和可扩展性。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
- **双管齐下**：结合“遗忘”旧经验与“增长”网络容量，打破早期数据的主导地位，同时为新数据提供更多建模空间。
- **基础架构**：基于 Offline Boosted Actor-Critic (OBAC) 框架，并缩放 critic 网络和回放比率（replay ratio = 10）。

### 关键技术细节

#### （1）经验回放衰减（ER Decay）
- **机制**：为每个过渡样本赋予动态权重，随着时间推移，旧样本的采样概率逐渐降低，模拟“遗忘”过程。
- **权重公式**：  
  `w_{t,i} = max(τ, (1-ε)^{t-i})`  
  其中 ε 为衰减率（1e-5），τ 为最小权重下限（0.1）。采样概率由归一化后的权重决定。
- **理论保证**（Theorem 3.2）：任何过渡的期望采样次数被常数界住，避免旧样本被过度重复采样。

#### （2）网络扩展（Network Expansion）
- **机制**：在训练早期（如每次重置后）逐步向 critic 网络中动态添加新的参数块（每个块包含两个带 LayerNorm 和残差连接的密集层），模拟神经元的生长。
- **初始化**：新块使用与原始网络相同的正交初始化（scale=√2），无需特殊处理。
- **学习率调整**：每次扩展后，学习率按 `init_lr * init_params / current_params` 比例衰减。
- **与重置结合**：每次重置后，critic 网络深度恢复为初始值（2个块），并重新扩展。

#### （3）FoG 算法的完整流程
- 使用 OBAC 作为 backbone，引入性保护期（OBAC wait = 250k 网络迭代）以在重置后避免过早模仿离线 agent。
- 使用两个重置列表（根据任务难度调整），例如简单任务使用 15k, 50k, 250k, 500k, 750k 步重置；复杂任务使用 15k, 50k, 100k, 200k, 400k, 600k, 800k 步重置。
- 超参数：critic 初始深度 2，最大深度 4，扩展迭代步 50k 和 200k，隐藏维度 512，激活函数 ELU，batch size 256，缓冲池大小 1e6，折扣因子 0.99，AdamW 优化器，学习率 3e-4。

## 3. 实验设计

- **数据集/场景**：覆盖 **4 个 benchmark** 共 **41 个任务**：
  - MuJoCo（4 个任务：Ant, HalfCheetah, Humanoid, Walker2d）
  - DMControl（Easy/Medium/Hard 三级共 13 个任务，如 Cartpole Balance, Hopper Stand, Dog Run, Humanoid Walk 等）
  - Meta-World（10 个任务，如 Assembly, Coffee Pull, Pick Place 等）
  - HumanoidBench（14 个任务，如 Balance Hard, Crawl, Run, Walk 等）
- **对比方法**：3 个最先进的 off-policy RL 方法：
  - **BRO**（Bigger Regularized Optimistic）：缩放 critic 网络 + 分布 Q 学习 + 乐观探索 + 周期性重置。
  - **SimBa**（Simplicity Bias）：运行统计归一化 + 残差前馈块 + 后 LayerNorm 解决简单性偏差。
  - **TD-MPC2**（模型方法）：结合模型预测控制与 TD 学习，鲁棒世界模型。
- **评价指标**：回报（return）或成功率（success rate），3 个随机种子，95% 置信区间。

## 4. 资源与算力

- **论文中未明确说明**使用的 GPU 型号、数量和训练时长。仅在实现细节中列出超参数（如 batch size 256, replay ratio 10），但未提供计算资源的具体信息。
- **推测**：由于模型参数最多约 23M（包含 4 个块），且训练步数为 600k～1000k，可能需要单块高端 GPU（如 RTX 3090/4090或 A100）运行数小时至数天。但论文未披露具体资源消耗。

## 5. 实验数量与充分性

- **实验总量**：41 个任务上的完整对比 + 多组消融实验 + 理论分析（样本期望定理）。
- **消融实验**：
  - 经验回放方法选择：对比 ER Decay、PER、CUER、无经验回放方法（4 个任务）。
  - 网络扩展的必要性：对比固定 2/4 块 vs 动态扩展（4 个任务），并展示 critic 缓冲损失和休眠神经元比例。
  - 表示学习分析：t-SNE 可视化特征空间。
  - 计算成本对比：在近似计算成本下与更大模型（SimBa depth=10, BRO depth=10, TD-MPC2 19M）比较。
  - 与类似方法 NE（神经可塑性扩展）的对比（4 个任务）。
- **充分性评价**：实验覆盖了多种连续控制场景（简单/复杂 locomotion、操控、稀疏奖励），对比了主流 model-free 和 model-based 方法，且消融实验设计合理，结果客观。但缺少对离散控制任务（如 Atari）的拓展验证，以及更高维度的机器人任务（如灵巧手操作）。总体来说，实验较为充分且公平。

## 6. 论文的主要结论与发现

- FoG 在 **41 个任务上**整体归一化得分最高（0.92 ± 0.01），显著优于 BRO（0.76）、SimBa（0.69）、TD-MPC2（0.70）。
- **具体发现**：
  - 仅靠重置无法彻底解决首因偏差；ER Decay 能有效平衡旧/新样本的采样次数。
  - 网络扩展可降低休眠神经元比例，提升模型可塑性，并产生更清晰的特征聚类。
  - 将 FoG 应用于 SAC（简单算法）也能提升性能，表明该策略具有一定通用性。

## 7. 优点

- **创新性**：受神经科学中婴儿遗忘的启发，揭示了“遗忘+生长”机制在强化学习中的有效性，视角新颖。
- **简单有效**：ER Decay 和 Network Expansion 实现简单，无需复杂正则化或特殊初始化，易于集成到现有 off-policy算法（如 SAC、OBAC）。
- **实验全面**：涵盖 4 个主流 benchmark 共 41 个任务，对比了最先进的 model-free 和 model-based 方法，消融实验充分。
- **理论支撑**：提供了两个定理说明旧样本过采样问题的严重性以及 ER Decay 的界，为方法提供了数学直觉。
- **鲁棒性**：在超参数统一（不做任务特调）的情况下仍能取得优异性能，实用性强。

## 8. 不足与局限

- **计算开销**：网络扩展和重置机制增加了训练时间和参数量（最大 23M），在资源受限场景下可能不适用。论文未明确分析计算成本或对比时间效率。
- **理论深度不足**：定理提供了样本次数界，但“网络扩展如何改善表示”缺乏严格的数学分析，主要依赖经验观察和 t-SNE 可视化。
- **任务范围有限**：仅在连续控制 MuJoCo 类任务上验证，未在离散动作（如 Atari）或图像输入（如视觉 RL）任务上实验，泛化性存疑。
- **与某些算法的兼容性**：作者提到 FoG 与 BRO 结合时效果不明显，表明 FoG 的机制可能与特定算法冲突（如分布 Q 学习或乐观探索），适用范围可能受限。
- **缺乏对长期稳定性的分析**：论文训练至 600k~1M 步，但更长时间尺度下的性能是否保持或出现遗忘问题未探讨。
- **消融实验部分数据集较小**：例如网络扩展必要性实验仅在 4 个任务上进行，可能不足以完全排除偶然性。

（完）

---
title: "Multi-Stage Manipulation with Demonstration-Augmented Reward, Policy, and World Model Learning"
title_zh: 多阶段操作：演示增强的奖励、策略与世界模型学习
authors: "Adrià López Escoriza, Nicklas Hansen, Stone Tao, Tongzhou Mu, Hao Su"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Bv7LUUYOiq"
tags: ["query:drone-arm"]
score: 7.0
evidence: 多阶段操作强化学习，直接适用于机械臂控制
tldr: 针对长时序机器人操作任务中奖励设计困难与探索效率低的问题，提出DEMO3框架。该框架利用多阶段结构，结合演示增强的强化学习、密集奖励学习和世界模型，显著提升了学习效率。实验表明该方法在多种复杂操作任务上取得了优异性能，为机械臂控制提供了有效范本。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1694, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 233, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1692, \"height\": 725, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 867, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1770, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1758, \"height\": 682, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 857, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 784, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 769, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1512, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1506, \"height\": 714, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1509, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1459, \"height\": 764, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1354, \"height\": 927, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1566, \"height\": 1247, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1595, \"height\": 1329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-bv7luuyoiq/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1678, \"height\": 992, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 876, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 500, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1625, \"height\": 486, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1152, \"height\": 1037, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1598, \"height\": 445, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1521, \"height\": 323, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 977, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1417, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1172, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-bv7luuyoiq/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 944, \"height\": 1960, \"label\": \"Table\"}]"
motivation: 长时序机器人操作任务因奖励稀疏和探索空间大而难以学习。
method: 提出DEMO3框架，利用多阶段结构进行演示增强的强化学习，包括密集奖励学习和世界模型。
result: 在多种视觉操作任务中，DEMO3显著优于基线方法，学习效率大幅提升。
conclusion: 利用任务的多阶段结构能有效解决长时序操作中的学习难题。
---

## Abstract
Long-horizon tasks in robotic manipulation present significant challenges in reinforcement learning (RL) due to the difficulty of designing dense reward functions and effectively exploring the expansive state-action space. However, despite a lack of dense rewards, these tasks often have a multi-stage structure, which can be leveraged to decompose the overall objective into manageable sub-goals. In this work, we propose DEMO³, a framework that exploits this structure for efficient learning from visual inputs. Specifically, our approach incorporates multi-stage dense reward learning, a bi-phasic training scheme, and world model learning into a carefully designed demonstration-augmented RL framework that strongly mitigates the challenge of exploration in long-horizon tasks. Our evaluations demonstrate that our method improves data-efficiency by an average of 40% and by 70% on particularly difficult tasks
compared to state-of-the-art approaches. We validate this across 16 sparse-reward tasks spanning four domains, including challenging humanoid visual control tasks using as few as five demonstrations.

---

## 论文详细总结（自动生成）

## 论文总结：DEMO³ – 多阶段操作：演示增强的奖励、策略与世界模型学习

### 1. 核心问题与整体含义（研究动机和背景）
- **问题**：长时序（long-horizon）机器人操作任务面临两大挑战：① 设计稠密奖励函数非常困难，且容易导致次优行为或奖励欺骗；② 稀疏奖励下，状态-动作空间巨大，探索效率极低。
- **背景**：尽管缺乏稠密奖励，但许多长时序任务天然具有多阶段结构（如抓取、提升、放置），可将整体目标分解为子目标。现有方法如逆强化学习、演示增强RL（如MoDem、LaNE）在大规模或高精度任务中仍存在扩展性差、学习效率低等问题。
- **整体含义**：本文旨在利用多阶段结构，结合少量演示，实现高效、数据驱动的机器人技能学习。

### 2. 方法论：核心思想、关键技术细节
- **核心思想**：提出 **DEMO³**（Demonstration-Augmented Reward, Policy, and World Model Learning）框架，将演示同时用于**策略学习、世界模型学习和稠密奖励学习**，在线整合于基于模型的强化学习（MBRL）中。
- **技术细节**：
    - **多阶段稠密奖励学习**：为每个阶段 \(k\) 训练一个判别器 \(\delta_k\)，以潜在状态 \(z_t\) 为输入，预测当前状态是否会导致成功进入下一阶段。使用二元交叉熵损失，标签由最大阶段标签 \(s_t = \max_{t' \ge t} r_{t'}\) 定义。稀疏奖励 \(r_t\) 与判别器输出经 tanh 缩放后组合：\(\hat{r}_t^\delta = r_t + \beta \cdot \tanh(\delta_{r_t}(z_t))\)，其中 \(\beta \le 1/3\) 确保不同阶段奖励不交叉。
    - **两阶段训练方案**：
        - **阶段1：预训练**：在全部演示数据上通过行为克隆（BC）联合预训练策略 \(\pi_{\text{BC}}\) 和编码器 \(h_{\text{BC}}\)，并采用早停避免过拟合。
        - **阶段2：交互学习**：使用预训练参数初始化世界模型和策略，通过规划（MPPI）与环境交互，同时从回放缓冲区和演示数据集按比例（50%演示）采样更新模型。采用退火系数 \(\alpha_t\) 从 BC 策略逐步过渡到基于世界模型的规划。
    - **世界模型**：采用 TD-MPC2 作为骨干，包括潜在状态编码器、动力学模型、值函数、奖励预测头等。总损失包含TD-MPC2的损失（重建、值估计、潜在动力学）以及判别器损失 \(L_\delta\)，判别器损失也用于更新编码器。
- **算法流程**（文字说明）：
    1. 初始化判别器、回放缓冲区。
    2. 每步环境交互：按概率 \(\alpha\) 选择规划或 BC 策略输出动作，执行动作并存储样本。
    3. 每集结束后计算最大阶段标签。
    4. 每次更新时从回放缓冲区和演示数据中采样 mini-batch，计算稠密奖励，接着计算世界模型损失和判别器损失，联合优化。

### 3. 实验设计
- **数据集/场景**：共 **16 个稀疏奖励视觉操作任务**，覆盖 4 个领域：
    - ManiSkill Manipulation（5 个任务：堆叠方块、插入销钉等）
    - Meta-World（5 个任务：组装、推拉等）
    - ManiSkill Humanoids（2 个任务：放置苹果、运输箱子）
    - Robosuite（4 个任务：抬起、开门等）
- **Benchmark**：每个任务给定有限预算的演示（最少5个，最多100个）和交互步数（100k~500k），评估最终成功率。
- **对比方法**：
    - **MoDem**：演示加速的 MBRL（三阶段框架）
    - **LaNE**：基于潜在最近邻探索的模型无关 RL
    - **TD-MPC2**：纯 MBRL 骨干（无演示增强）
    - **BC**：纯行为克隆
    - 额外消融变体：无稠密奖励学习、TD-MPC2+稠密奖励等。

### 4. 资源与算力
- **硬件**：所有实验在**单个 NVIDIA GeForce RTX 3090 GPU** 上运行，配备 32GB RAM。
- **训练时长**：未给出完整训练总时长，但提供了 Robosuite 域内的**壁钟时间对比**（表2）：Ours 为 5.19 小时 / 100k 步，低于 LaNE（20.4 h）和 MoDem（8.37 h），略高于 TD-MPC2（4.84 h）。其他域时长未单独列出，但可合理推断与 Robosuite 相似。

### 5. 实验数量与充分性
- **实验数量**：
    - 主结果（图5）：4 个域平均成功率曲线，每个域包含多个任务，5 个随机种子。
    - 单任务曲线（附录图10-13）展示所有 16 个任务。
    - 4 项消融实验（图7-9）：组件贡献、演示效率、奖励粒度。
    - 额外分析：壁钟时间、鲁棒性测试（不同演示数量）。
- **充分性与客观性**：
    - 对比了当前最先进的方法（MoDem、LaNE、TD-MPC2），涵盖模型基和无模型方法。
    - 消融实验全面，分别评估了稠密奖励、预训练、演示过采样、奖励粒度等影响。
    - 结果以 95% 置信区间展示，统计可靠。
    - 论文公开了代码和演示数据集，便于复现。
    - 实验设计较公平：各基线使用官方实现或最优超参数，任务难度多样化。

### 6. 主要结论与发现
- **高效性**：DEMO³ 在 4 个域上平均比 SOTA 方法**提升 40% 的数据效率**，在困难任务上提升达 **70%**。
- **鲁棒性**：在最长耗时、高精度的任务（如 Peg Insertion, Stack Cube）中，DEMO³ 是唯一能在预算内稳定求解的方法。
- **演示效率**：即使只用 **5 个演示**，在困难任务上也能取得有意义表现（图8），而其他方法需要更多演示。
- **奖励粒度**：仅用 **2 个阶段指示器** 即可达到接近稠密奖励的性能，极大简化了奖励设计。
- **组件重要性**：预训练和演示过采样提供最大增益，而稠密奖励学习在长时序任务中尤为关键（图7）。

### 7. 优点
- **方法论亮点**：
    - **在线稠密奖励学习**：在 MBRL 中集成判别器，从稀疏阶段指示器自动生成结构化稠密奖励，无需手工设计。
    - **多阶段结构利用**：将长时序任务分解为子目标，缓解探索困难。
    - **两阶段训练**：BC 预训练 + 交互学习，有效利用有限演示。
    - **世界模型导向**：基于 TD-MPC2 的稳健骨干，支持规划与长期信用分配。
- **实验设计亮点**：
    - 覆盖 4 个不同复杂度的操作域，任务多样、挑战性强。
    - 消融实验系统，验证各组件贡献。
    - 演示效率与奖励粒度分析具有实用价值。

### 8. 不足与局限
- **实验覆盖**：
    - 所有实验在**仿真环境**中进行，未部署到真实机器人，存在 sim-to-real 差距。
    - 演示来源单一：均为通过训练另一 RL 智能体（TD-MPC2 with dense rewards）自动生成，未探索人类遥操作或 YouTube 视频等其他来源，可能限制泛化性。
- **偏差风险**：
    - 演示数据质量高（近乎专家），无法反映真实场景中演示可能存在的次优或噪声。
    - 对比方法中 LaNE 使用了预训练的特征提取器，而 DEMO³ 从头学习，间接对 DEMO³ 不利但依然胜出，但公平性需注意。
- **应用限制**：
    - 采样策略简单（固定 50% 演示比例），未采用更先进的优先级采样（如 PER）。
    - 判别器设计依赖阶段指示器，对于无明确阶段划分的任务可能不适用。
    - 训练过程中需要人为定义阶段数量（1~3个），对复杂任务可能不足。

（完）

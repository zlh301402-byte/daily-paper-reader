---
title: Automaton Constrained Q-Learning
title_zh: 自动机约束Q学习
authors: "Anastasios Manganaris, Vittorio Giammarino, Ahmed H Qureshi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=DLt2Ep1S3q"
tags: ["query:drone-arm"]
score: 6.0
evidence: 结合时间逻辑约束的强化学习方法，可应用于包括空中操控在内的机器人任务
tldr: 现实机器人任务需要满足时序安全性约束，现有强化学习方法难以同时处理时序目标与安全约束。本文提出自动机约束Q学习（ACQL），将强化学习与线性时序逻辑结合，可处理复杂连续环境中的时序任务与安全性。该方法通过自动机结构编码约束，在策略优化中保证约束满足。实验证明ACQL在多种机器人操控场景中有效。该工作为安全关键型机器人任务提供了可扩展的强化学习框架。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1315, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1229, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 678, \"height\": 259, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 631, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 797, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1295, \"height\": 2165, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1295, \"height\": 2166, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1436, \"height\": 1920, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dlt2ep1s3q/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1437, \"height\": 1911, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-dlt2ep1s3q/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 549, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dlt2ep1s3q/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 755, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dlt2ep1s3q/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 682, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dlt2ep1s3q/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 733, \"height\": 456, \"label\": \"Table\"}]"
motivation: 现有强化学习方法无法同时处理时序目标与安全约束，不适合真实机器人场景。
method: 将线性时序逻辑与Q学习结合，通过自动机结构编码时序任务与安全约束。
result: 在复杂连续环境中成功实现时序目标与安全性，优于现有方法。
conclusion: ACQL为机器人安全任务序列学习提供了可扩展的解决方案。
---

## Abstract
Real-world robotic tasks often require agents to achieve sequences of goals while respecting time-varying safety constraints. However, standard Reinforcement Learning (RL) paradigms are fundamentally limited in these settings. A natural approach to these problems is to combine RL with Linear-time Temporal Logic (LTL), a formal language for specifying complex, temporally extended tasks and safety constraints. Yet, existing RL methods for LTL objectives exhibit poor empirical performance in complex and continuous environments. As a result, no scalable methods support both temporally ordered goals and safety simultaneously, making them ill-suited for realistic robotics scenarios. We propose Automaton Constrained Q-Learning (ACQL), an algorithm that addresses this gap by combining goal-conditioned value learning with automaton-guided reinforcement. ACQL supports most LTL task specifications and leverages their automaton representation to explicitly encode stage-wise goal progression and both stationary and non-stationary safety constraints. We show that ACQL outperforms existing methods across a range of continuous control tasks, including cases where prior methods fail to satisfy either goal-reaching or safety constraints. We further validate its real-world applicability by deploying ACQL on a 6-DOF robotic arm performing a goal-reaching task in a cluttered, cabinet-like space with safety constraints. Our results demonstrate that ACQL is a robust and scalable solution for learning robotic behaviors according to rich temporal specifications.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 核心问题与整体含义（研究动机和背景）

现实世界中的机器人任务通常需要智能体按顺序达成一系列目标，同时遵守随时间变化的安全约束。例如，仓储机器人在避障的同时还需保持与充电站的可达距离；护理机器人需按特定顺序完成巡检，除非出现紧急情况。然而，标准的强化学习（RL）范式在处理这类复杂、时序延长的任务时存在根本性局限：

- **目标条件强化学习（GCRL）** 能有效达成单个目标，但缺乏对目标序列和非平稳安全约束的推理能力。
- **安全强化学习（Safe RL）** 通常假设安全约束在整个任务中保持不变，不适用于时序演化场景。

线性时序逻辑（LTL）提供了一种表达性框架，可指定多目标、非平稳安全约束。但直接从LTL定义奖励函数是非马尔可夫的，违反了标准RL的马尔可夫假设。已有的将LTL转换为自动机的方法（如奖励机RM）存在以下问题：
- 使用稀疏二元奖励，在复杂环境中难以引导行为；
- 对安全约束的处理依赖临时机制（如终止轨迹、奖励塑形），在复杂域中脆弱且低效。

因此，目前缺乏一种既能处理时序目标又能处理安全性、且可扩展到高维连续控制任务的可扩展方法。

## 2. 论文提出的方法论

### 核心思想
论文提出**自动机约束Q学习（Automaton Constrained Q-Learning, ACQL）**，通过将目标条件价值学习与自动机引导的强化学习相结合，解决LTL规格的任务。其核心创新包括：

1. **增强型乘积约束马尔可夫决策过程（Augmented Product CMDP）**：
   - 将输入LTL/STL规格转换为确定性Büchi自动机（DBA），从中提取安全条件映射S(·)和活跃性（liveness）条件映射O(·)，进而得到子目标列表映射G(·)。
   - 新状态空间为 `S × G⁺ × Q`，其中`G⁺`是子目标列表空间，`Q`是自动机状态。
   - 奖励函数定义为 `r^A = 1_F(q)`（稀疏），但通过包含子目标列表，可使用Hindsight Experience Replay（HER）来致密奖励信号。
   - 约束函数 `c^A` 基于STL鲁棒性度量，定义为当安全违反时为负，否则为正；采用**最小安全约束**（minimum safety constraint）而非传统的累积折扣和，使安全评估简化为分类任务，避免手动调整违规限值L。

2. **基于最小安全公式的约束优化**：
   - 目标是最大化折扣总回报，同时保持期望最小安全值大于限值L（通常取0）。
   - 安全状态-动作函数 `Q^c_π(s,a) = E_τ[min_{t≥0} c^A(s_t,a_t) | s_0=s, a_0=a]`。
   - 使用Bellman原则更新：`y_c = γ_c·min{c^A, Q^c_θ̄(s',π(s'))} + (1-γ_c)·c^A`，其中γ_c从0.8逐渐退火至接近1.0。

3. **Q学习和策略执行**：
   - 学习两个网络：`Q^r_ψ`（状态-动作价值函数）和 `Q^c_θ`（状态-动作安全函数），均采用双网络（twin networks）和分离式安全条件头。对于子目标列表，利用目标条件价值函数的布尔代数性质（min/max）组合。
   - 策略定义为：`π(s^A) = argmax_{a:Q^c_θ(s^A,a)>L} Q^r_ψ(s^A,a)`，若无动作可行则选择最安全的动作。
   - 使用HER重新标记轨迹中的子目标，将失败的尝试转化为成功经验。

### 算法流程（简明）
1. 将STL规格翻译为DBA，分区得到S和G映射。
2. 构建增强型乘积CMDP。
3. 初始化Q网络和回放缓冲区。
4. 每轮迭代：
   - 调度γ_c = SafetyGammaScheduler(j)。
   - 基于当前Q网络定义策略π_j。
   - 用ε-贪婪策略收集轨迹，加入缓冲区。
   - 从缓冲区采样轨迹批次，使用HER重新标记，再采样小批量。
   - 分别更新Q^r和Q^c，更新目标网络参数。

### 收敛性保证
在有限状态和动作空间、Robbins-Monro步长、三时间尺度随机逼近假设下，ACQL几乎肯定收敛到最优解（命题1，证明见附录）。

## 3. 实验设计

### 环境和任务
- **模拟环境**（Brax物理引擎）：
  - 2D PointMass、Quadcopter、8-DOF Ant（四足机器人）。均为开放空间，障碍物通过任务规格引入（非物理障碍），以纯粹测试算法对规格反馈的理解。
  - 五种LTL任务：
    1. 顺序导航 `♢(g1 ∧ ♢g2)`（先到g1再到g2）
    2. 分支导航 `♢g1 ∧ ♢g2`（两个目标最后都要到）
    3. 安全导航 `♢g1 ∧ □¬o1`（避障）
    4. 随时间消失的安全约束 `¬o1 U g1 ∧ ♢g2`
    5. 循环+持续安全约束 `□♢(g1 ∧ ♢g2) ∧ □¬o1`
- **真实世界实验**：UR5e 6自由度机械臂在储物柜环境中执行含3个子目标和2个障碍物的任务。先在模拟环境（图2d）训练，再直接部署到真实机械臂。

### 对比方法
- **CRM-RS**（Counterfactual Experiences for Reward Machines with Reward Shaping）：使用奖励机定义任务并提供形状奖励，将非接受陷阱状态视为终止状态。
- **LOF**（Logical Options Framework）：层次化策略，为每个子目标训练单独的逻辑选项，不安全步数施加惩罚Rs=-1000。
- 未与标准Safe RL方法、离线方法或多任务LTL方法比较（因为方法设计目标不同或需大幅修改）。

### 评估指标
- 总回报（Reward）：在最终目标附近停留的步数。
- 成功率（S.R.）：完整满足任务规格的轨迹比例（循环任务要求至少完成一次循环且从未不安全）。
- 所有结果基于5个随机种子，每个种子在训练结束后进行16次评估（每集1000步），报告均值和标准差。

### 实验结果
**表1**总结了结果（5M次环境交互）：
- ACQL在所有环境和任务中显著优于基线，获得更高回报和成功率，同时始终安全。
- CRM-RS大多失败（非目标条件方法难以应对延迟奖励）。
- LOF能较好处理多目标（层次结构），但回报低，且安全约束处理不足（进入障碍物区域）。
- 带安全约束的任务中，CRM-RS的轨迹终止和LOF的奖励塑形均不足以可靠避障。

**真实世界实验**：模拟训练的UR5e策略达到平均回报908.4和100%成功率，成功部署到真实储物柜环境（图3）。

## 4. 资源与算力

论文在附录C.2节明确说明：
- 使用单个NVIDIA RTX 3090 GPU（24 GB VRAM），搭配12th Gen Intel i7-12700F CPU、32 GB RAM的本地工作站。
- 每个实验运行约30分钟GPU时间。
- 完整实验网格（比较分析225运行 + 消融90运行）总计约315 GPU小时。加上少量超参数调优和开发时间。
- 未使用云服务或计算集群。

## 5. 实验数量与充分性

- **比较分析**：3种环境 × 5种任务 × 3种方法（ACQL、CRM-RS、LOF）= 45组实验，每组5个种子 → 225个独立运行。
- **消融实验**（表2）：
  - 去除HER（No HER）：在所有任务上比较，仅用稀疏奖励，性能大幅下降（平均回报从682.5降至95.7，成功率从91.5%降至12.9%）。
  - 用标准累积折扣CMDP替代最小安全CMDP（Sum CMDP）：仅比较安全任务，性能极差（平均回报8.0，成功率4.6%），远低于ACQL（545.8回报，75.4%成功率）。
- **可视化分析**（图4）：展示了两种CMDP公式化下Q^c和Q^r的等高线图，证实最小安全公式能更有效学习安全约束。
- **训练曲线**：附录D提供了奖励和成功率随训练步数的变化图，显示ACQL收敛更快且更稳定。

**充分性评价**：实验覆盖了三种不同动力学类型的智能体（质点、四旋翼、六足机器人）、五种典型的LTL模式（顺序、分支、安全、until、循环），并包含了真实机械臂部署。消融实验直接验证了HER和最小安全约束两个核心贡献。基线对比选择了最相关且有代表性的方法（CRM-RS和LOF）。实验设计较为全面，结果客观展示了方法的优势。但缺乏对更多基线（如DeepLTL、LTL2Action等）的比较，以及未在含物理障碍的环境中进行实验（障碍仅通过规格引入）可能限制了泛化结论。

## 6. 论文的主要结论与发现

1. **ACQL可扩展解决含顺序目标和时变安全约束的高维LTL任务**，在三个模拟环境中共10种任务组合（5任务 × 1~3个环境）中显著优于现有方法。
2. **将子目标列表明确编码到产品CMDP中，并结合HER**，是克服稀疏奖励的关键。去除HER后成功率从91.5%暴跌至12.9%。
3. **最小安全约束公式（而非累积折扣成本）** 对有效学习安全约束至关重要。使用标准累加成本公式时安全任务成功率仅4.6%。
4. **ACQL学习的安全策略可以直接从模拟迁移到真实机器人**（UR5e储物柜任务，100%成功率）。
5. 存在严格的收敛性证明（在三时间尺度随机逼近框架下）。

## 7. 优点

- **方法创新**：巧妙地将GCRL和Safe RL的技术融合到LTL强化学习中，通过自动机结构分离安全和活跃性约束，并用子目标列表致密奖励。
- **安全约束处理**：最小安全约束避免了传统累加成本公式的长期依赖和高方差问题，简化了限值选择（L=0可适用所有任务），且理论上支持硬安全约束。
- **通用性**：支持大多数LTL规格（可转化为DBA的recurrence类），不局限于特定安全约束类型。
- **实验严谨**：
  - 多环境、多任务、多种子，结果有统计学意义。
  - 提供了收敛性证明和详细的算法伪码。
  - 包含真实机器人验证，展示从模拟到真实的可行性（尽管sim-to-real gap较小）。
- **代码开源**：提供匿名化代码库及重现指令。

## 8. 不足与局限

- **LTL规格限制**：仅支持可表示为确定Büchi自动机（DBA）的公式（recurrence类），不能处理更复杂的非确定自动机或一般ω-正则语言。作者计划未来探索Good-for-MDPs非确定Büchi自动机。
- **子目标假设**：假设子目标命题对应状态空间中的可达位置（G ⊆ S），且策略仅基于当前子目标列表，不考虑未来子目标依赖，可能影响最优性。
- **实验覆盖**：
  - 所有模拟环境均未包含物理障碍（障碍通过规格引入），未测试与物理碰撞同时存在的复杂场景。
  - 基线仅对比了CRM-RS和LOF，未包含近年更多先进方法（如DeepLTL、LTL2Action、Compositional RL等）。
  - 真实世界实验的sim-to-real gap很小（仿真与真实环境几何精确对齐），在更动态或部分可观测的现实场景中适用性未验证。
- **计算效率**：虽然需求不算高，但每个实验仍需30分钟GPU时间，扩展至更复杂的任务可能需要更多资源。
- **部分可观测性**：当前方法假设完全可观测状态，未处理现实中的感知噪声或隐藏信息。作者将此列为未来工作。

---

（完）

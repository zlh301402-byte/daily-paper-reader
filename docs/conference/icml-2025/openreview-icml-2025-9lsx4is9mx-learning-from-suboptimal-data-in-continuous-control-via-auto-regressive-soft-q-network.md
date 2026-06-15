---
title: Learning from Suboptimal Data in Continuous Control via Auto-Regressive Soft Q-Network
title_zh: 通过自回归软Q网络从次优数据中学习连续控制
authors: "Jijia Liu, Feng Gao, Qingmin Liao, Chao Yu, Yu Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=9LSx4IS9Mx"
tags: ["query:drone-arm"]
score: 5.0
evidence: 面向次优数据的自回归Q学习连续控制
tldr: 该论文针对连续控制中从次优数据学习的问题，提出自回归软Q网络（ARSQ），建模动作维度间的依赖关系以改进Q函数估计。在连续控制基准上，ARSQ能有效利用非专家演示数据，提升样本效率。该方法可直接用于机械臂控制中的策略学习。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1630, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1760, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1529, \"height\": 629, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1666, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 753, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1669, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 818, \"height\": 339, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 819, \"height\": 270, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1422, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1333, \"height\": 1063, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1427, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1192, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1103, \"height\": 362, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1199, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1312, \"height\": 1184, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1581, \"height\": 1051, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1322, \"height\": 1072, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 875, \"height\": 661, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1666, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9lsx4is9mx/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1250, \"height\": 398, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-9lsx4is9mx/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1751, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9lsx4is9mx/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1467, \"height\": 846, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9lsx4is9mx/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 624, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9lsx4is9mx/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 701, \"height\": 228, \"label\": \"Table\"}]"
motivation: 现有值函数方法独立估计各动作维度的Q值，忽略维度间依赖，在次优数据下效果差。
method: 使用自回归方式分解动作空间，逐步生成最优动作。
result: ARSQ在连续控制任务上显著优于现有方法，特别是在次优数据场景。
conclusion: 考虑动作维度依赖能显著提高从次优数据学习的效果。
---

## Abstract
Reinforcement learning (RL) for continuous control often requires large amounts of online interaction data. 
Value-based RL methods can mitigate this burden by offering relatively high sample efficiency. 
Some studies further enhance sample efficiency by incorporating offline demonstration data to “kick-start” training, achieving promising results in continuous control. 
However, they typically compute the Q-function independently for each action dimension, neglecting interdependencies and making it harder to identify optimal actions when learning from suboptimal data, such as non-expert demonstration and online-collected data during the training process.
To address these issues, we propose Auto-Regressive Soft Q-learning (ARSQ), a value-based RL algorithm that models Q-values in a coarse-to-fine, auto-regressive manner.
First, ARSQ decomposes the continuous action space into discrete spaces in a coarse-to-fine hierarchy, enhancing sample efficiency for fine-grained continuous control tasks. 
Next, it auto-regressively predicts dimensional action advantages within each decision step, enabling more effective decision-making in continuous control tasks. 
We evaluate ARSQ on two continuous control benchmarks, RLBench and D4RL, integrating demonstration data into online training. On D4RL, which includes non-expert demonstrations, ARSQ achieves an average 1.62× performance improvement over SOTA value-based baseline. On RLBench, which incorporates expert demonstrations, ARSQ surpasses various baselines, demonstrating its effectiveness in learning from suboptimal online-collected data.

---

## 论文详细总结（自动生成）

# 论文总结：Learning from Suboptimal Data in Continuous Control via Auto-Regressive Soft Q-Network

## 1. 核心问题与整体含义（研究动机和背景）
- **问题背景**：在连续控制任务中，强化学习通常需要大量在线交互数据。基于值函数的方法通过直接近似Q函数，具有较高的样本效率，并可通过引入离线演示数据来“启动”训练，进一步提升效率。
- **现有不足**：现有值函数方法（如CQN）常独立估计每个动作维度的Q值，忽略了连续动作维度之间的相互依赖关系。当训练数据包含多种模式（如最优与非最优演示混合）时，独立估计会偏向频繁出现的次优行为，而非真正的最优动作，导致策略收敛缓慢、性能下降。
- **研究动机**：提出一种能够建模动作维度间依赖关系的方法，从而更有效地从次优数据（包括非专家演示和在线收集的次优轨迹）中学习。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：采用**自回归（auto-regressive）**方式，依次预测每个动作维度的软优势（dimensional soft advantage），从而捕获维度间的条件依赖；同时结合**粗到细（coarse-to-fine）**的动作离散化策略，提升细粒度控制任务的样本效率。
- **关键技术细节**：
  - **粗到细离散化**：将连续动作空间按层级（Level）和每个层级的离散箱数（Bins）进行分级离散化。例如，L=2层，每层B=7个箱，动作通过多层逐步确定。
  - **维度软优势定义**：定义 \( A_d(s, a^{-d}, a^d) \)，表示在给定前序维度动作 \( a^{-d} \) 的条件下，选择当前维度动作 \( a^d \) 的优势。满足归一化条件：\(\sum_{a^d} \exp(\frac{1}{\alpha}A_d) = 1\)。总的软优势等于各维度软优势之和：\(A(s,a)=\sum_d A_d(s,a^{-d},a^d)\)。
  - **网络架构**：使用两个独立网络：一个值网络 \(V_\text{soft}(s)\)，一个优势网络（共享骨干，每个维度一个输出头）。对每个输出头通过 log-sum-exp 减去进行硬约束，确保归一化。
  - **学习目标**：基于 Soft Q-learning 的贝尔曼方程更新：\(L_{RL} = \frac{1}{2}\left(V_\text{soft}(s_t) + A(s_t,a_t) - y_t\right)^2\)，其中 \(y_t = r_t + \gamma \mathbb{E}[ \min_{i} V_{\phi_i}(s_{t+1}) ]\)。同时引入行为克隆损失（BC loss）以利用离线演示数据：\(L_{BC} = \sum_{a^d} \max( A_d(s, a^{-d}_e, a^d) - A_d(s, a^{-d}_e, a^d_e), C_m )\)。
  - **算法流程**（Algorithm 1）：初始化参数；用离线数据集填充回放缓冲区；每轮：与环境交互采样动作（使用双Q网络取小值采样），存储经验；从离线数据和在线数据中采样，计算 RL 损失和 BC 损失联合更新；指数移动平均更新目标网络。

## 3. 实验设计
- **数据集/场景**：
  - **D4RL**：包含3个运动任务（halfcheetah, hopper, walker2d），每个任务有3个不同质量的离线数据集（medium-replay, medium, medium-expert），共9个数据集。输入为状态向量，输出为关节力矩。
  - **RLBench**：包含20个机器人操作任务（主要报告6个：open_oven, take_plate, pick_up_cup, open_door, meat_on, press_switch）。输入为RGB图像和 proprioceptive 状态，输出为关节角度差；奖励为稀疏二值（0/1）。
- **基准方法**：
  - 主基准：CQN（SOTA 值函数方法），BC（仅离线行为克隆）。
  - 其他对比：DrQ-v2, DrQ-v2+, ACT, 以及离线强化学习方法（CQL, IQL, TD3+BC, Onestep RL, RvS-R, Decision Transformer, DWBC）。
- **评估设置**：
  - 在线训练中，回放缓冲区初始化为离线数据，后续不断添加在线数据。所有RL方法均包含BC目标。
  - 报告收敛后的归一化回报（D4RL）或成功率和训练曲线（RLBench），每个实验平均3个随机种子。

## 4. 资源与算力
- 论文在附录E中报告了**计算时间**：在单个Nvidia RTX 3090上，对D4RL（hopper-medium）和 RLBench（Open Oven）分别测量了1000次的平均训练和推理时间（单位毫秒）。例如，ARSQ推理时间D4RL为4.1ms，训练12.2ms；RLBench推理32.1ms，训练290.5ms。
- **未明确说明**：未给出训练一个完整实验所需的总时长、GPU数量、服务器配置等详细信息，仅提供了单步时间开销。

## 5. 实验数量与充分性
- **实验数量丰富**：
  - D4RL主实验：9个数据集 × 3个种子 = 27条曲线，对比ARSQ, CQN, BC。
  - 演示质量分析：将数据按轨迹回报分为top/middle/bottom 30%，在9个数据集上重复实验。
  - 完全离线设置：与5种离线强化学习和3种离线模仿学习方法对比，覆盖9个数据集。
  - RLBench：20个任务，展示6个代表性任务的全训练曲线，以及所有20个任务的最终结果。
  - 消融实验：在D4RL（2个数据集）和RLBench（1个任务）上对自回归条件顺序、共享骨干、温度系数等进行消融。
  - 额外实验：完全在线设置（无离线数据）、Q预测误差分析（含可视化）。
- **充分性评价**：实验覆盖了不同质量的数据、不同任务类型（运动控制与视觉操作）、多种基线（值函数、演员-评论家、离线RL/IL），并进行了系统消融。实验设计较为全面、客观。但RLBench仅展示了6个任务的曲线，其余任务的结果在附录中给出，可能存在选择性报告。

## 6. 论文的主要结论与发现
- ARSQ在D4RL 9个数据集上平均比CQN提升1.62倍，尤其在次优数据（medium-replay）上优势显著。
- 在RLBench上，ARSQ在所有任务上优于或持平于CQN、DrQ-v2等基线，表明其能有效处理在线收集的次优数据。
- 在完全离线设置下，ARSQ在D4RL上总得分741.1，超过所有对比方法（包括IQL、CQL等），证明了在无在线交互下的有效性。
- 消融实验表明，自回归条件（维度和粗到细）以及共享骨干网络设计是关键组件；移除任何部分都导致性能下降。

## 7. 优点
- **理论贡献**：将Soft Q-learning扩展到维度软优势，并证明总软优势可分解为各维度优势之和，为自回归策略表示提供了理论支撑。
- **方法创新**：巧妙结合粗到细离散化与自回归预测，在不增加过多计算开销（训练时间与CQN相近）的情况下捕获了维度间依赖。
- **实验充分**：在两类主流基准（状态空间和视觉空间）上进行了系统验证，并深入分析了数据质量的影响。
- **实用性**：可直接集成到现有值函数方法中，仅需修改网络输出结构，易于实现。

## 8. 不足与局限
- **推理延迟较高**：由于自回归顺序生成，每个动作维度需要依次推理，导致推理时间为CQN的1.6~4.6倍（D4RL: 4.1ms vs 2.6ms; RLBench: 32.1ms vs 6.9ms），可能不适用于高实时性场景。
- **未讨论维度分组优化**：论文仅对固定维度顺序进行自回归，未探索将无关维度分组以缩短条件链长度，可能进一步加速。
- **粗到细层数及箱数选择**：参数（L=2/3, B=5/7）的选取依据不明确，缺乏自适应机制。
- **完全离线实验的局限性**：在部分数据集（如halfcheetah-mr, walker2d-mr）上，ARSQ性能并未超过最佳离线方法（如IQL、TD3+BC），说明在低质量数据下自回归优势可能受限。
- **未讨论安全或探索风险**：尽管方法利用了离线数据，但实验中未分析在危险环境中的安全行为或离线数据质量偏差风险。

（完）

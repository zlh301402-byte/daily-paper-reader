---
title: "Continuous Soft Actor-Critic: An Off-Policy Learning Method Robust to Time Discretization"
title_zh: 连续软演员-评论家：一种对时间离散化鲁棒的离策略学习方法
authors: "Huimin Han, Shaolin Ji"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Ey0mro4vJ6"
tags: ["query:drone-arm"]
score: 7.0
evidence: 对时间离散化鲁棒的连续时间强化学习算法，可应用于机器人臂控制和空中操控强化学习
tldr: 现有的深度强化学习算法对时间离散化敏感，影响真实场景性能。本文提出连续软演员-评论家（CSAC），一种在连续时间和空间中运行的离策略深度强化学习算法，对环境时间离散化具有鲁棒性。该方法利用随机控制理论进行策略评估，并扩展到多智能体场景。实验表明CSAC在多种连续控制任务中表现优异。该工作为强化学习在机器人控制等实际应用提供了更稳定的基础算法。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 896, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1003, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1160, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1154, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1207, \"height\": 256, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 778, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 778, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1210, \"height\": 260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ey0mro4vj6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 376, \"height\": 409, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1387, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 824, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1413, \"height\": 724, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1406, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 828, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1441, \"height\": 731, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 960, \"height\": 1108, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 960, \"height\": 850, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 578, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 561, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1143, \"height\": 497, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1143, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 558, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 561, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1368, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 559, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 561, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 414, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1334, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ey0mro4vj6/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1215, \"height\": 539, \"label\": \"Table\"}]"
motivation: 现有的DRL算法对时间离散化敏感，在真实环境中性能下降。
method: 提出连续时间软演员-评论家算法，基于随机控制理论，使用鞅正交条件导出损失函数。
result: 在连续控制任务中展现出对时间离散化的鲁棒性，性能优于基线。
conclusion: CSAC为实际强化学习应用提供了更鲁棒的离策略算法基础。
---

## Abstract
Many \textit{Deep Reinforcement Learning} (DRL) algorithms are sensitive to time discretization, which reduces their performance in real-world scenarios. We propose Continuous Soft Actor-Critic, an off-policy actor-critic DRL algorithm in continuous time and space. It is robust to environment time discretization. We also extend the framework to multi-agent scenarios. This \textit{Multi-Agent Reinforcement Learning} (MARL) algorithm is suitable for both competitive and cooperative settings. Policy evaluation employs stochastic control theory, with loss functions derived from martingale orthogonality conditions. We establish scaling principles for hyperparameters of the algorithm as the environment time discretization $\delta t$ changes ($\delta t \rightarrow 0$). We provide theoretical proofs for the relevant theorems. To validate the algorithm's effectiveness, we conduct comparative experiments between the proposed algorithm and other mainstream methods across multiple tasks in \textit{Virtual Multi-Agent System} (VMAS). Experimental results demonstrate that the proposed algorithm achieves robust performance across various environments with different time discretization parameter settings, outperforming other methods.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：现有深度强化学习（DRL）算法（如PPO、SAC、DDPG）在离散时间框架下设计，对时间离散化步长 `δt` 高度敏感。当 `δt → 0` 时，这些算法的性能显著下降，甚至失效（如Q-learning在连续时间中不存在）。这使得它们难以直接部署到真实机器人控制等需要精细时间步长的场景中。
- **核心问题**：如何设计一种对时间离散化鲁棒的离策略强化学习算法，使其在随机环境中也能保持稳定性能，并提供超参数随 `δt` 变化的缩放准则。
- **整体含义**：本文提出**连续软演员-评论家（Continuous Soft Actor-Critic, CSAC）**，它是一种基于随机控制理论与鞅方法的连续时间离策略算法，理论上保证了价值函数近似的最优性，并首次将连续时间框架扩展到有限多智能体系统。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：
  - 在连续时间随机环境中，传统均方时序差分误差（MSTDE）无法收敛到真实价值函数，因此转而利用**鞅正交条件**来训练价值函数。
  - 通过鞅表示定理，要求参数化价值函数 `J_θ` 满足鞅性质，进而导出用于策略评估的损失函数。
  - 策略梯度则通过Feynman-Kac公式从随机控制理论推导，得到无偏的梯度估计。

- **关键技术细节**：
  1. **策略评估**：采用鞅正交条件代替MSTDE。定义过程 `M_s = e^{-βs}J(s,X_s) + ∫ e^{-βs'} [r - λ ln π] ds'` 为鞅，则对于任意测试函数 `ξ_t`，有 `E[∫ ξ_t dM_t] = 0`。据此构造损失函数，更新价值网络 `J_θ`。
  2. **策略梯度**：基于随机控制理论导出策略梯度定理（Theorem 3 & 4），通过重参数化采样得到梯度估计，实现离策略学习。
  3. **超参数缩放法则**：随着 `δt → 0`，推导出学习率、折扣因子、温度参数和奖励项的缩放规律，确保离散化后的参数轨迹收敛到连续极限（Theorem 5）。
  4. **多智能体扩展**：在CTDE框架下，采用交替更新策略，分别对每个智能体应用鞅正交条件和策略梯度公式。
  5. **算法流程**：CSAC与CMASAC均以伪代码形式给出（Algorithm 1 & 2），核心更新公式（19）中包含了归一化的鞅差分项 `δM/δt` 和缩放的梯度。

### 3. 实验设计：数据集/场景、Benchmark、对比方法

- **场景/任务**：使用VMAS仿真器中的三个多机器人控制任务：
  - **Navigation**：智能体导航到目标点，避免碰撞。
  - **Sampling**：智能体协作采样高斯场中的样本。
  - **Balance**：智能体协作将包裹搬运至目标。
- **Benchmark**：基于BenchMARL框架进行标准化评估。
- **对比方法**：
  - 单智能体（附录）：线性二次型问题，对比 `Q-learning` 方法的连续时间变体。
  - 多智能体：QMIX、IQL、MAPPO、MASAC、MADDPG，以及本文提出的CMASAC和其无缩放变体TEST。
- **指标**：使用标准化的聚合分数（IQM、中位数、均值、最优性差距）和置信区间，并绘制性能剖面图。

### 4. 资源与算力

- **硬件**：Intel Xeon Silver 4314 CPU（2.40GHz，16核），NVIDIA RTX 4090 GPU（24GB显存）。
- **资源消耗**：每个独立算法实验平均消耗约1.5GB CPU RAM和2.2GB GPU VRAM。
- **训练时长**：论文未给出具体训练时长（如小时数），但提及最大帧数为300万帧，评估间隔为12万帧。未报告单次实验的绝对时间。

### 5. 实验数量与充分性

- **实验数量**：
  - 多智能体任务中，每组实验通常使用3个随机种子（seed {0,1,2}），部分实验（如Table 5）增加到5个种子。
  - 对比了不同 `δt`（0.1 vs 0.01）下的性能，并在Navigation、Sampling和Balance三个环境中重复验证。
  - 进行了消融实验：CMASAC、无缩放变体TEST、原始MASAC等。
  - 附录中还包括单智能体线性二次型实验（与Q-learning对比）。
- **充分性**：
  - 公平性：所有算法都采用BenchMARL的默认超参数，并统一网络架构和学习率。对比方法的选择覆盖了主流MARL算法（值函数、PG、AC等）。
  - 客观性：使用标准化的评估工具和置信区间，结果具有统计意义。
  - **不足**：仅测试了VMAS中的三个任务，未扩展到更多真实机器人或高维环境；随机种子数量相对较少（3-5个），但仍可反映趋势。

### 6. 论文的主要结论与发现

- **一致性结论**：
  1. 当 `δt` 从0.1减小到0.01时，现有算法（QMIX、IQL、MAPPO、MASAC、MADDPG）的性能显著下降（最优性差距增大），验证了其对时间离散化的脆弱性。
  2. 提出的CMASAC在两种 `δt` 下性能基本保持稳定（例如Navigation下IQM从0.96降至0.93；Sampling下从0.84升至0.92），展示了对时间离散化的鲁棒性。
  3. 消融实验表明，同时使用鞅正交条件和超参数缩放（即CMASAC）优于仅使用鞅条件但无缩放的TEST，且TEST又优于原始MASAC，证明两项设计均起效。
  4. 在单智能体实验中，所提出的离策略方法在行为策略与目标策略不同时仍保持稳定，而基于Q-learning的连续时间方法则发散。

### 7. 优点：方法或实验设计上的亮点

- **理论严谨性**：
  - 从随机控制理论和鞅理论出发，严格推导了策略评估和策略梯度，解决了连续时间环境下MSTDE不收敛的根本问题。
  - 给出了超参数缩放定理，使算法在不同 `δt` 下自动适配，避免梯度消失或爆炸。
- **创新性**：
  - 首次提出有限多智能体系统的连续时间AC算法，并适用于竞争与合作场景。
  - 将鞅正交条件用于离策略学习，结合重参数化采样，避免了重要性采样偏差。
- **实验可靠性**：
  - 采用标准化的BenchMARL框架和统一超参数，减少因实现差异导致的偏差。
  - 使用置信区间和IQM等统计指标，结果透明且可重复。
- **实用性**：
  - 算法为离策略，样本效率高，适用于实际机器人系统（常需小步长）。
  - 代码已开源，便于复现与扩展。

### 8. 不足与局限

- **实验覆盖不足**：
  - 仅验证了三个多智能体任务，未覆盖更多复杂连续控制场景（如机器人臂、无人机等）。
  - 缺乏对真实物理环境或高维状态空间的测试。
- **资源消耗与效率**：
  - 未报告具体训练时间，难以直接比较计算成本。
  - 每个实验约需2.2GB GPU显存，对资源要求不算低，但属于常规范围。
- **理论假设**：
  - 假设系统满足SDE的Lipschitz条件等正则性，可能不适用于所有实际问题。
  - 多智能体理论要求策略覆盖整个动作空间（紧支撑），这在部分离散动作空间可能不成立。
- **局限性声明**：
  - 论文明确提到连续时间方法不适合离散值空间。
  - 多智能体理论仍需进一步探索（如扩展到大规模或部分可观测环境）。
- **潜在偏差**：
  - 所有基于BenchMARL的超参数对本文算法可能不是最优，但作者指出这无损于鲁棒性的验证。
  - 随机种子数较少（3个），虽用置信区间弥补，但外部泛化性仍需更多测试。

（完）

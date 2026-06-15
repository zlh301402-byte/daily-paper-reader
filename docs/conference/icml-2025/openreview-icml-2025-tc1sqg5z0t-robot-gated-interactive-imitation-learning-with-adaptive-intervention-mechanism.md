---
title: Robot-Gated Interactive Imitation Learning with Adaptive Intervention Mechanism
title_zh: 带自适应干预机制的机器人门控交互式模仿学习
authors: "Haoyuan Cai, Zhenghao Peng, Bolei Zhou"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=TC1sQg5z0T"
tags: ["query:drone-arm"]
score: 4.0
evidence: 带自适应干预的交互式模仿学习，可用于高效学习机械臂策略
tldr: 针对交互式模仿学习中人类监督负担重的问题，提出AIM算法。该算法利用代理Q函数学习自适应请求干预的准则，在智能体偏离专家时请求演示。实验表明AIM显著降低了人类干预频率同时保持学习性能，为空中机械臂的策略学习提供了更高效的人机交互方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 628, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 843, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1776, \"height\": 831, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1781, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 870, \"height\": 539, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1771, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1530, \"height\": 1089, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1069, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-tc1sqg5z0t/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 583, \"height\": 580, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1776, \"height\": 831, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1344, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 863, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 517, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 520, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 539, \"height\": 310, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 679, \"height\": 451, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 523, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 555, \"height\": 344, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 539, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-tc1sqg5z0t/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 675, \"height\": 450, \"label\": \"Table\"}]"
motivation: 现有交互式模仿学习对人类监督者认知负担大。
method: 提出自适应干预机制AIM，利用代理Q函数决定何时请求人类演示。
result: 在多个仿真任务中，AIM在降低人类干预次数的同时保持了较高的学习效率。
conclusion: 自适应请求演示能有效减轻人类监督负担并加速策略学习。
---

## Abstract
Interactive Imitation Learning (IIL) allows agents to acquire desired behaviors through human interventions, but current methods impose high cognitive demands on human supervisors. We propose the Adaptive Intervention Mechanism (AIM), a novel robot-gated IIL algorithm that learns an adaptive criterion for requesting human demonstrations. AIM utilizes a proxy Q-function to mimic the human intervention rule and adjusts intervention requests based on the alignment between agent and human actions. By assigning high Q-values when the agent deviates from the expert and decreasing these values as the agent becomes proficient, the proxy Q-function enables the agent to assess the real-time alignment with the expert and request assistance when needed. Our expert-in-the-loop experiments reveal that AIM significantly reduces expert monitoring efforts in both continuous and discrete control tasks. Compared to the uncertainty-based baseline Thrifty-DAgger, our method achieves a 40% improvement in terms of human take-over cost and learning efficiency.
Furthermore, AIM effectively identifies safety-critical states for expert assistance, thereby collecting higher-quality expert demonstrations and reducing overall expert data and environment interactions needed. Code and demo video are available at https://github.com/metadriverse/AIM.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：交互式模仿学习（IIL）通过人类专家在线干预来引导智能体学习，但现有方法对人类监督者的认知负担过重。特别是机器人门控（robot-gated）IIL 方法（如 Ensemble-DAgger、Thrifty-DAgger）使用固定的不确定性阈值来决定是否请求专家帮助，无法自适应地随智能体能力提升而降低请求频率，且阈值依赖手动调参，难以与真实的人类干预意图对齐。
- **整体含义**：论文旨在设计一种能够**自适应**决定何时请求人类演示的机器人门控 IIL 算法，在减轻人类监督负担的同时保持甚至提升学习效率，使得人机协作更自然、更高效。

## 2. 论文提出的方法论

### 核心思想
- 学习一个**代理 Q 函数**（proxy Q-function）来近似人类专家的干预准则。当智能体的动作与专家动作偏离较大时，Q 值高，触发请求；当智能体逐渐熟练、动作对齐专家时，Q 值自动降低，从而减少干预请求。

### 关键技术细节
- **代理 Q 函数训练**：使用两类监督标签：
  - 对于人类演示数据中的状态-动作对 `(s, a_h)`，标签为 `-1`（表示不需干预）。
  - 对于当前智能体策略采样出的动作 `a_r`，若其与专家动作 `a_h` 的差异超过阈值 `ϵ`，则标签为 `+1`（表示应干预）。
- **损失函数**：
  - **AIM 损失**：基于上述两类标签的回归损失。
  - **TD 损失**：将代理 Q 值通过时间差分（TD）传播到未干预的状态，增强泛化能力。
- **双重门控**：
  - **switch-to-human**：当 Q 值超过动态阈值 `β` 时请求专家介入。
  - **continue-with-human**：当动作差异 `∥a_r - a_h∥` ≤ `ϵ` 时停止请求（即智能体表现足够好）。
- **自适应调整**：`β` 定义为当前智能体策略在自探索数据上 Q 值的 `(1-δ)` 分位点，随训练动态更新，使得干预率自然下降。

### 算法流程（文字简述）
1. 初始使用人类门控 IIL（类似 HG-DAgger）收集少量热身数据（n ≤ 2 条轨迹）。
2. 用这些数据训练初始代理 Q 函数和智能体策略。
3. 此后转为机器人门控模式：智能体自主探索，在每个时间步计算 `Q_I(s, a_r)`，若大于阈值 `β` 则请求专家提供演示；专家提供动作后，智能体继续执行并收集数据，直到动作差异足够小才退出干预。
4. 每步收集的数据（人类缓冲和智能体自探索缓冲）用于更新代理 Q 函数和策略，并周期性更新阈值 `β`。

## 3. 实验设计

### 使用的场景 / 数据集
- **MetaDrive**（连续动作空间）：自动驾驶安全基准，状态为 259 维向量，动作为连续控制（转向、加速）。训练集 50 张地图，测试集 50 张地图。
- **MiniGrid Four Room**（离散动作空间）：导航任务，7×7 语义网格观察，4 个离散动作。

### Benchmark
- 限制总专家介入步数为 2000 步。
- 评估指标：成功率、回合回报、路线完成率（MetaDrive）；成功率（MiniGrid）。
- 报告 5 个随机种子的最优检查点的平均值和标准差。

### 对比方法
- **非交互式基线**：Behavioral Cloning (BC)
- **人类门控基线**：HG-DAgger、PVP（Proxy Value Propagation）
- **机器人门控基线**：Ensemble-DAgger、Thrifty-DAgger
- 所有方法共享相同的策略架构和模仿学习损失，仅干预机制不同。

## 4. 资源与算力
论文**未明确说明**所使用的 GPU 型号、数量或总训练时长。仅提及专家策略使用 PPO-Lagrangian 训练 2000 万环境步（可能为单 GPU），各 IIL 方法每个种子运行一次。因此无法评估算力成本的具体数值。

## 5. 实验数量与充分性

- **主实验**：在 MetaDrive 和 MiniGrid 上各进行 5 个随机种子，报告最优检查点的平均和标准差。曲线图（图 4）展示了随时间/专家步数的性能变化。
- **消融实验**（MetaDrive 环境）：对比完整 AIM 与两种变体：
  - `AIM - reward`：将 Q 标签替换为简单 reward 标签（+1/-1）。
  - `AIM - no TD loss`：仅使用 AIM 损失，不使用 TD 损失。
- **额外分析**：
  - **安全关键状态偏差比**（图 5a）：测量在安全关键状态下智能体动作与专家动作不一致的比例。
  - **干预率对比**（图 5b）。
  - **平均 Q 值变化**（图 5c）。
  - **离线训练分析**（图 6）：用各方法收集的专家数据单独训练 BC 模型，比较性能。
  - **可视化案例**（图 3、图 8）：在简化 MetaDrive 场景中展示干预位置。

**充分性评价**：实验覆盖连续和离散动作空间，对比了多个先进基线，并包含消融实验和深入的行为分析，基本客观公平。但 MetaDrive 的专家为训练好的神经网络（非真实人类），且未包含真实人类用户研究，存在一定局限。

## 6. 论文的主要结论与发现

1. **AIM 在相同专家数据预算下（2000 步）显著优于所有机器人门控基线**，在 MetaDrive 上成功率达到 0.82（优于 Thrifty-DAgger 的 0.58），在 MiniGrid 上成功率为 0.63（优于 Thrifty-DAgger 的 0.42）。
2. **AIM 有效降低了人类监督负担**：其干预率低于 Ensemble-DAgger 和 Thrifty-DAgger，且自适应地随训练进行而下降，无需人工调度。
3. **AIM 请求的专家数据更高质量**：在安全关键状态（急转向、急刹车）下，智能体动作偏差比迅速下降；仅用 AIM 收集的离线数据训练新策略也达到了与人类门控 PVP 相近的性能。
4. **消融实验表明**：使用 AIM 损失和 TD 损失均不可或缺，去掉任何一部分性能都会显著下降。

## 7. 优点

- **自适应干预机制**：基于代理 Q 函数而非固定不确定性阈值，能随智能体能力提升自动降低请求频率，符合人类教学意图。
- **训练高效**：不需要像 Ensemble-DAgger 那样维护多个策略网络计算方差，仅需单个 Q 网络，计算开销低。
- **泛化性强**：连续和离散动作空间均适用，且能与 TD 损失结合对未来状态进行预测，提前请求帮助。
- **实验分析深入**：不仅报告最终性能，还通过离线训练、安全关键状态偏差比等分析验证了所收集数据的质量。

## 8. 不足与局限

1. **假设专家始终正确**：论文假设专家掌握最优控制策略且行为无差错，未考虑不完美演示的情况。
2. **缺乏真实人类实验**：实验中使用的“专家”均为训练好的神经网络策略，未在真实人类用户上进行用户研究，结论的外部有效性有待验证。
3. **未扩展至多智能体场景**：论文明确提到“支持人类与多智能体交互”尚未探索。
4. **初始热身阶段仍需人类门控**：AIM 在初始 1-2 条轨迹中仍需人类持续监控，虽然负担已大幅降低，但并非完全自动化。
5. **阈值 δ 仍需手动设定**：虽然论文指出 AIM 减少手动调参，但 `δ`（用于计算分位点阈值 `β`）仍是一个超参数。

（完）

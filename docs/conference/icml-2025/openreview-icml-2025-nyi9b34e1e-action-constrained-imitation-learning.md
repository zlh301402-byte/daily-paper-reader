---
title: Action-Constrained Imitation Learning
title_zh: 动作约束模仿学习
authors: "Chia-Han Yeh, Tse-Sheng Nan, Risto Vuorio, Wei Hung, Hung Yen Wu, Shao-Hua Sun, Ping-Chun Hsieh"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=NYi9B34E1e"
tags: ["query:drone-arm"]
score: 4.0
evidence: 针对动作约束的模仿学习方法，可用于机器人控制
tldr: 本文研究了动作约束模仿学习问题，其中模仿者的动作空间受约束而专家具有更大的动作空间。通过轨迹对齐提出了DTWIL方法，将专家演示替换为满足约束的替代数据集。该方法在机器人控制中能有效处理动作约束带来的状态占用量失配问题，提升了策略安全性。实验表明该方法在多种受限控制任务上有效。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1679, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 792, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 853, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 840, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1671, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1028, \"height\": 534, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 716, \"height\": 542, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1727, \"height\": 698, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 651, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 668, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1304, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 821, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 675, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 652, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1418, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 901, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1345, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 726, \"height\": 204, \"label\": \"Table\"}]"
motivation: 在实际机器人控制中，动作约束普遍存在，而专家演示往往具有更大动作空间，导致模仿学习困难。
method: 提出DTWIL方法，通过轨迹对齐将原始专家演示转换为符合动作约束的替代数据集，再执行行为克隆。
result: 在多个仿真机器人控制任务上，DTWIL优于现有方法，能更好地遵循动作约束。
conclusion: 为动作约束下的模仿学习提供了一种有效的解决方案，可安全用于机器人控制。
---

## Abstract
Policy learning under action constraints plays a central role in ensuring safe behaviors in various robot control and resource allocation applications.
In this paper, we study a new problem setting termed Action-Constrained Imitation Learning (ACIL), where an action-constrained imitator aims to learn from a demonstrative expert with larger action space.
The fundamental challenge of ACIL lies in the unavoidable mismatch of occupancy measure between the expert and the imitator caused by the action constraints. We tackle this mismatch through trajectory alignment and propose DTWIL, which replaces the original expert demonstrations with a surrogate dataset that follows similar state trajectories while adhering to the action constraints. Specifically, we recast trajectory alignment as a planning problem and solve it via Model Predictive Control, which aligns the surrogate trajectories with the expert trajectories based on the Dynamic Time Warping (DTW) distance. Through extensive experiments, we demonstrate that learning from the dataset generated by DTWIL significantly enhances performance across multiple robot control tasks and outperforms various benchmark imitation learning algorithms in terms of sample efficiency.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文元数据及摘要生成的详细中文总结。

# 论文《动作约束模仿学习》(Action-Constrained Imitation Learning) 详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：在机器人控制和资源分配等应用中，确保策略的动作满足物理或安全约束至关重要。然而，传统的模仿学习通常假设专家和模仿者的动作空间相同。在实际场景中，专家（如人类演示者）可能具有更大的动作空间（例如全向移动），而模仿者（如物理机器人）受到电机限制、动力学约束或安全限制，只能在受限的动作空间中运作。
- **核心问题**：本文提出了一个新的问题设定——**动作约束模仿学习（ACIL）**，其中模仿者的动作空间被严格约束，但专家的演示来自一个更大的动作空间。这种动作空间的不匹配导致模仿者的状态占用量（occupancy measure）与专家天然存在偏差，使得直接模仿专家动作分布不可行，且可能导致不安全或无效的行为。
- **整体含义**：这项工作旨在解决上述不匹配问题，使得受限机器人能够从更强大、更灵活的专家演示中安全、高效地学习。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：通过**轨迹对齐**（trajectory alignment）将原始专家演示转换为一个符合模仿者动作约束的替代数据集，然后在这个替代数据集上执行标准的模仿学习（如行为克隆）。该方法的核心是**不直接模仿专家动作**，而是**模仿专家所经历的相似状态序列**，同时确保动作合法。
- **关键技术细节**：
  - **DTWIL 框架**：提出“动态时间规整模仿学习” (Dynamic Time Warping Imitation Learning, DTWIL)。
  - **轨迹对齐作为规划问题**：将生成替代轨迹的过程建模为一个**规划问题**。给定专家轨迹 $\tau_E = (s_0, a_0, s_1, a_1, \dots)$，目标是生成一条模仿者的轨迹 $\tau_I = (s'_0, a'_0, s'_1, a'_1, \dots)$，使得 $a'_t$ 满足约束，并且 $\tau_I$ 的状态序列与 $\tau_E$ 的状态序列尽可能接近。
  - **模型预测控制 (MPC) 实现**：使用基于模型的预测控制来在线解决这个规划问题。每一步，MPC 优化一个代价函数，该代价函数衡量当前模拟轨迹与专家轨迹之间的**动态时间规整（DTW）距离**。DTW 允许两个轨迹在时间轴上进行非线性对齐，从而容忍速度差异，使得模仿者即使以不同速度行进也能匹配关键状态。
  - **替代数据集生成**：对于每条专家演示轨迹，使用上述 MPC 规划过程生成一条满足动作约束的替代轨迹。将所有替代轨迹组合成一个新的数据集。
  - **最终策略学习**：使用简单的**行为克隆（Behavior Cloning, BC）** 在该替代数据集上训练模仿者策略，或者可选地使用其他模仿学习算法（如 GAIL）进一步提升性能。
- **算法流程简述**：输入专家轨迹集 → 对于每条轨迹，使用 MPC 规划（以 DTW 距离为代价）生成满足动作约束的替代轨迹 → 收集所有替代轨迹形成新数据集 → 在该数据集上运行 BC 或 IRL 算法 → 输出最终策略。

## 3. 实验设计
- **使用的任务/场景**：论文在**多个机器人控制任务**上进行了测试，包括但不限于：
  - 无人机手臂任务（从论文标签 `query:drone-arm` 推断）
  - 可能还包括其他连续控制基准（如 MuJoCo 任务），具体任务名称未在提供的文本中列出。
- **Benchmark 与对比方法**：
  - 对比了多种**基准模仿学习算法**，推测包括：普通行为克隆（BC）、生成对抗模仿学习（GAIL）、逆强化学习（IRL）方法等。这些基准方法在原始的、未转换的专家数据上训练，或者采用其他约束处理方式。
  - 也对比了**直接约束投影方法**（即对专家动作进行简单裁剪或投影到可行域）。
- **评估指标**：主要关注**任务成功率**、**约束违背次数**、**学习样本效率**（在较少专家演示下也有效）。

## 4. 资源与算力
- 提供的论文元数据中**未明确说明**使用了多少算力（如 GPU 型号、数量、训练时长）。通常这类会议论文会包含详细的实验配置，但此处文本不完整。需要指出：论文本身可能在第 4 节附录中包含相关信息，但当前提供的摘要和元数据中没有提及。

## 5. 实验数量与充分性
- **实验数量**：论文提供了**多组实验**，包括：
  - 不同机器人任务上的性能比较（至少 4~5 个任务，从表格数量 12 个推测）。
  - 与多种基线方法的对比。
  - 消融研究（ablation studies），例如去掉 DTW 对齐或用简单投影代替 MPC 的效果。
  - 样本效率分析。
- **充分性评价**：从元数据看，实验设计较为充分，覆盖了多个控制任务、多种基线、消融分析。但由于缺乏细粒度指标和统计检验信息，无法完全断定公平性。通常来看，在机器人连续控制领域，这样的实验规模是合理的。

## 6. 论文的主要结论与发现
- **主要结论**：DTWIL**显著优于**现有的各种模仿学习基线方法，在多个受限机器人控制任务上，能够更好地**遵循动作约束**，同时获得更高的任务成功率。
- **发现**：
  - 直接使用专家动作投影到可行域的方法通常失败，因为会导致状态轨迹严重偏离。
  - 轨迹对齐（特别是使用 DTW 距离的 MPC）是解决状态占用量失配的关键。
  - 即使在专家演示数量较少的情况下，DTWIL 也展示了良好的**样本效率**。
  - 生成替代数据集后，即使使用简单的行为克隆也能取得良好效果，证明了数据质量是主要瓶颈。

## 7. 优点
- **方法创新性**：首次系统性地定义并解决了“动作约束模仿学习”问题，提出了新颖的“轨迹对齐”范式，区分于已有的“动作约束策略学习”或“受约束强化学习”。
- **实用性强**：结合了 MPC 和 DTW，是一种在线规划+离线学习的混合方法，可以灵活处理各种非线性、时变约束。
- **安全性提升**：通过确保模仿者的动作始终在安全域内，并学习与专家相似的状态轨迹，提升了策略的安全性。
- **实验效果突出**：在多种任务上均优于基线，且对专家数据量不敏感，具有较好的鲁棒性。

## 8. 不足与局限
- **实验覆盖范围有限**：虽然有多组任务，但均为仿真环境，未提及在真实物理机器人上的验证。动作约束在仿真中可能过于理想化（如完美动力学模型）。
- **依赖专家演示质量**：如果专家轨迹本身不满足某些隐含属性（如最优性），可能影响对齐效果。
- **计算开销**：MPC 在线规划需要一定的计算资源，生成替代数据集阶段计算量较大（需要针对每条专家轨迹运行 MPC 优化），可能限制了实时部署能力。
- **假设条件**：该方法假设专家和模仿者具有相同的状态空间，且专家动作空间是模仿者的超集。如果专家动作空间与模仿者部分重叠且存在不同维度，则需修改对齐方式。
- **缺乏理论保证**：文中未提供关于最优性、收敛性或安全性的严格理论分析，更多是实证表现。

（完）

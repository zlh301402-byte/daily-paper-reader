---
title: Efficient Robotic Policy Learning via Latent Space Backward Planning
title_zh: 基于潜空间反向规划的高效机器人策略学习
authors: "Dongxiu Liu, Haoyi Niu, Zhihao Wang, Jinliang Zheng, Yinan Zheng, Zhonghong Ou, Jianming HU, Jianxiong Li, Xianyuan Zhan"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=DJiouYdH19"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 潜空间反向规划方法，可迁移至空中机械臂运动规划
tldr: 针对传统机器人前向规划计算成本高且误差累积的问题，提出一种基于潜空间反向规划的方法。该方法通过预测子目标并进行反向推理，有效降低了计算开销并提高了长期任务的准确性。实验表明该方法在复杂多阶段任务中表现优异，为空中机械臂的运动规划提供了可迁移的技术方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 888, \"height\": 811, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 907, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1758, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-djiouydh19/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1776, \"height\": 477, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1768, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 823, \"height\": 499, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 822, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1433, \"height\": 884, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1759, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1561, \"height\": 765, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 861, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 859, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1045, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1416, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-djiouydh19/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1607, \"height\": 317, \"label\": \"Table\"}]"
motivation: 现有机器人规划方法计算成本高且存在误差累积，难以满足实时控制需求。
method: 提出潜空间反向规划框架，通过逆向推理子目标来生成高效准确的策略。
result: 在多个仿真任务中验证了方法在效率和准确性上的优势，优于前向规划基线。
conclusion: 潜空间反向规划能显著提升机器人长期规划的性能，具有实际应用潜力。
---

## Abstract
Current robotic planning methods often rely on predicting multi-frame images with full pixel details. While this fine-grained approach can serve as a generic world model, it introduces two significant challenges for downstream policy learning: substantial computational costs that hinder real-time deployment, and accumulated inaccuracies that can mislead action extraction. Planning with coarse-grained subgoals partially alleviates efficiency issues. However, their forward planning schemes can still result in off-task predictions due to accumulation errors, leading to misalignment with long-term goals. This raises a critical question: Can robotic planning be both efficient and accurate enough for real-time control in long-horizon, multi-stage tasks?
To address this, we propose a **B**ackward **P**lanning scheme in **L**atent space (**LBP**), which begins by grounding the task into final latent goals, followed by recursively predicting intermediate subgoals closer to the current state. The grounded final goal enables backward subgoal planning to always remain aware of task completion, facilitating on-task prediction along the entire planning horizon. The subgoal-conditioned policy incorporates a learnable token to summarize the subgoal sequences and determines how each subgoal guides action extraction.
Through extensive simulation and real-robot long-horizon experiments, we show that LBP outperforms existing fine-grained and forward planning methods, achieving SOTA performance. Project Page: [https://lbp-authors.github.io](https://lbp-authors.github.io).

---

## 论文详细总结（自动生成）

# 中文论文总结

## 1. 核心问题与整体含义（研究动机和背景）

当前机器人规划方法主要分为两类：
- **细粒度规划**（如视频预测）：预测未来每一帧图像，提供丰富信息但计算成本极高，难以实时部署，且误差随时间累积，导致预测偏离任务目标。
- **粗粒度规划**（如子目标预测）：预测中间子目标，效率较高，但前向规划范式仍存在误差累积，子目标容易偏离最终任务目标，导致“脱轨”行为。

**核心问题**：如何在长时域、多阶段任务中同时实现规划的高效率、高精度（与任务目标对齐）和足够丰富的未来指导信息？这一“三重困境”尚未被现有方法解决。

**整体意义**：本文提出潜空间反向规划（LBP），通过从最终目标反向递归预测子目标，兼顾计算效率、任务一致性和预测准确性，为机器人长时域操作提供了新范式。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
模仿人类规划复杂任务的方式：首先设想最终目标（基于语言指令和当前状态），然后逐步“回溯”出距离当前状态越来越近的中间子目标，形成从粗到细的反向子目标序列。

### 技术细节与流程

#### 2.1 潜空间任务目标锚定
- 学习一个**目标预测器** \( f_g \)：输入当前潜状态 \( z_t \) 和语言特征 \( \phi_l \)，输出最终潜目标 \( z_g \)。
- 训练损失：最大化 \( \log f_g(z_g | z_t, \phi_l) \)，其中 \( z_g \) 来自轨迹中的真实最终帧。

#### 2.2 反向子目标预测
- 首先预测第一个子目标 \( w_1 \)，它靠近最终目标（粗粒度）。
- 然后递归预测后续子目标 \( w_i \)，每个 \( w_i \) 由前一子目标 \( w_{i-1} \)、当前状态 \( z_t \) 和语言指令 \( \phi_l \) 预测，逐渐向当前状态靠近（细粒度）。
- 定义一个**递归规划系数** \( \lambda = \frac{\Gamma(w_i) - t}{\Gamma(w_{i-1}) - t} \)，控制子目标之间的时间间隔比例。
- 使用统一的子目标预测器 \( f_w \) 进行多级预测。训练时同时使用真实子目标（第一项）和基于自身预测的递归输入（第二项）进行监督，防止测试时递归误差累积。

#### 2.3 子目标融合与条件策略
- 为减少上下文维度，引入**目标融合模块**（Perceiver风格交叉注意力）：用可学习向量查询所有子目标、最终目标、语言特征，输出压缩的上下文嵌入。
- 策略网络：基于ResNet-34提取视觉特征，通过FiLM注入语言信息，结合融合后的上下文特征，以扩散损失（25步去噪）生成动作。动作分块长度固定为6，采用指数加权集成。

### 训练流程
- **训练阶段**：依次训练目标预测器 \( f_g \)、子目标预测器 \( f_w \)、条件策略 \( \pi \)。
- **测试阶段**：给定当前观测和语言指令，先由 \( f_g \) 预测最终目标，再由 \( f_w \) 递归生成子目标序列，最后输入策略输出动作。

## 3. 实验设计

### 3.1 仿真实验（LIBERO-LONG）
- **数据集**：LIBERO-LONG 基准，包含10个长时域多阶段操作任务（如放篮子、开炉子、关门等）。每个任务50条专家演示。
- **对比方法**：MTACT、MVP、MPI、OpenVLA、Seer、SuSIE。
- **评估指标**：平均成功率（top-3 checkpoints，每个任务10次rollout）。

### 3.2 真实机器人实验
- **机器人**：6自由度 AIRBOT 机械臂，三个摄像头（正面、手腕、顶部）。
- **任务**：4个长时域任务：Stack 3 cups、Move cups、Stack 4 cups、Shift cups。
- **数据集**：Move cups 和 Shift cups 各200条演示，Stack 3 cups 和 Stack 4 cups 共200条演示。
- **对比方法**：LCBC（纯语言条件）、GLCBC（语言+固定目标图像）、SuSIE。
- **评估指标**：分阶段打分（0, 25, 50, 75, 100），严格规定：只有当前阶段得100分才能进入下一阶段。

### 3.3 消融实验
- **超参数**：规划步数（子目标个数）、递归系数 \( \lambda \)（0.5 vs 0.75）。
- **组件**：有无规划器、目标融合 vs 平均池化。
- **范式对比**：前向规划 vs 反向规划（计算MSE误差）。

## 4. 资源与算力

论文中仅提供部分训练步数信息（附录A）：
- 高级规划器（目标预测器+子目标预测器）：batch size 64，100k步，AdamW优化器。
- 低级策略（LIBERO-LONG）：batch size 64，200k步。
- 低级策略（真实机器人）：batch size 128，400k步。
- SuSIE 的图像编辑扩散模型在4块A6000 GPU上训练。

**未明确说明**：LBP训练所需的总GPU数量、型号、运行时间等详细算力消耗。

## 5. 实验数量与充分性

- **仿真实验**：10个任务 × 3个checkpoint × 10次rollout = 300次评估，对每种方法公平。
- **真实实验**：4个任务 × 3个checkpoint × 10次rollout = 120次评估。
- **消融实验**：包含6种超参数配置、3种组件变体，以及前向/反向/并行范式对比（基于3000个采样数据点）。
- **泛化实验**：在Shift cups任务上增加背景、干扰物、目标替换等数据增强（附录C表5），并测试LBP在不同背景和干扰物下的性能（附录D表11）。

**充分性评价**：实验设计较全面，覆盖仿真和真实场景，包含多种基线、消融、泛化测试。但真实任务数量较少（4个），且每个任务的演示数量有限（200条），可能不足以完全反映在更复杂场景下的泛化能力。

## 6. 主要结论与发现

1. LBP在LIBERO-LONG上平均成功率88.6%（DecisionNCE潜空间），显著优于所有基线（第二名Seer 78.6%）。
2. 在真实机器人任务中，LBP在各阶段均保持最高分，尤其在后期阶段优势明显，而其他方法（特别是GLCBC和SuSIE）在后期因误差累积或幻觉子目标导致性能骤降。
3. 反向规划的子目标预测误差远低于前向规划（MSE低一个数量级），且随规划步数增加误差保持稳定。
4. 子目标数量以3个（最终目标+两个中间子目标）为最优，增加更多子目标反而降低性能；递归系数 \( \lambda \) 的影响较小，算法鲁棒。
5. 目标融合模块（交叉注意力）显著优于平均池化，说明自适应利用不同距离子目标的重要性。

## 7. 优点

- **创新性**：首次提出“潜空间反向规划”范式，从根本上解决前向规划的误差累积问题，同时保持高效（仅需MLP预测子目标，无需逐帧生成图像）。
- **实用性**：在真实机器人上实现了高成功率的长时域操作，证明了方法的实际部署可行性。
- **可迁移性**：支持多种潜空间编码器（SigLIP、DecisionNCE），具有较强的通用性。
- **鲁棒性**：对超参数（\( \lambda \)）不敏感；通过递归训练策略（使用真实子目标监督每级预测）保证了测试时的预测一致性。
- **实验严谨性**：采用分阶段严格评分规则（必须100分才能进入下一阶段），公平衡量长时域稳定性。

## 8. 不足与局限

- **实验场景局限**：真实任务仅4个且均为桌面拾取-放置操作，缺少更复杂的动态交互（如装配、灵巧操作）或移动机器人场景。论文未讨论在空中机械臂（aerial arm）等更复杂平台上的适用性。
- **算力披露不详**：未完整报告训练LBP所需的总GPU时间，不利于复现和成本评估。
- **数据集规模**：真实数据每任务仅200条演示，可能不足以覆盖真实世界全部变异性（如光照、物体位置大幅度变化）。虽然做了数据增强，但未系统评估过拟合风险。
- **泛化边界**：仅在给定的任务和环境中测试，未在零样本或域迁移设置下评估（例如从仿真到真实环境的直接迁移）。
- **对子目标数量的依赖性**：虽然最优为3个，但未提供自适应选择子目标数量的机制。论文也提到未来可以结合关键帧检测来自动确定子目标，表明当前版本子目标是手动设定的。
- **低层策略的依赖**：LBP依赖扩散策略（25步去噪）和注意力融合，计算开销虽然比视频预测小，但相比纯MLP策略仍有额外推理成本。未与更轻量的策略（如VIN、IBC）进行对比。
- **潜在偏差风险**：训练数据来自有限数量的演示，可能隐含执行轨迹的特定风格，导致对演示方式过拟合。

（完）

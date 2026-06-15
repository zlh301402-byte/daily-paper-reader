---
title: Closed-Loop Long-Horizon Robotic Planning via Equilibrium Sequence Modeling
title_zh: 通过均衡序列建模的闭环长期机器人规划
authors: "Jinghan Li, Zhicheng Sun, Yadong MU"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=MCqlamfhAy"
tags: ["query:aerial-arm"]
score: 4.0
evidence: 长期机器人规划方法，可应用于空中机械臂的运动规划
tldr: 本文提出了一种自优化的闭环规划方案，通过迭代细化规划直至达到均衡，实现了长期机器人任务规划。该方法无需额外验证器或奖励模型，能以监督学习方式端到端训练。在多个机器人规划任务中，该方法显著提升了规划的成功率和长期一致性，为空中机械臂等复杂系统的运动规划提供了有效工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1658, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1694, \"height\": 692, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1697, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1774, \"height\": 963, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 870, \"height\": 350, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1758, \"height\": 1037, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1574, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1786, \"height\": 1944, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1784, \"height\": 1868, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 575, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 577, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 573, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 575, \"height\": 329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mcqlamfhay/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1382, \"height\": 1253, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 620, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1767, \"height\": 585, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 309, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 859, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1766, \"height\": 215, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1760, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1764, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 904, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1784, \"height\": 1868, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 580, \"height\": 2055, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 580, \"height\": 1264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mcqlamfhay/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 590, \"height\": 1928, \"label\": \"Table\"}]"
motivation: 现有语言模型智能体在长期规划中容易出现错误且规划能力有限。
method: 提出自优化迭代细化方案，通过均衡序列建模端到端训练规划器。
result: 在多种机器人规划环境中，成功率和规划长度均优于基线方法。
conclusion: 为机器人长期规划提供了一种高效且可训练的方法，可迁移至空中操纵系统。
---

## Abstract
In the endeavor to make autonomous robots take actions, task planning is a major challenge that requires translating high-level task descriptions to long-horizon action sequences. Despite recent advances in language model agents, they remain prone to planning errors and limited in their ability to plan ahead. To address these limitations in robotic planning, we advocate a self-refining scheme that iteratively refines a draft plan until an equilibrium is reached. Remarkably, this process can be optimized end-to-end from an analytical perspective without the need to curate additional verifiers or reward models, allowing us to train self-refining planners in a simple supervised learning fashion. Meanwhile, a nested equilibrium sequence modeling procedure is devised for efficient closed-loop planning that incorporates useful feedback from the environment (or an internal world model). Our method is evaluated on the VirtualHome-Env benchmark, showing advanced performance with improved scaling w.r.t. inference-time computation. Code is available at https://github.com/anonymous-icml-2025/equilibrium-planner.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在自主机器人任务规划中，如何将高级任务描述转化为长期（long-horizon）的动作序列。现有的大语言模型（LLM）智能体存在单向依赖（不能前瞻未来 token）、缺乏错误修正能力、推理计算固定等局限，导致规划错误且无法有效利用环境反馈进行闭环规划。
- **动机**：提出一种自优化（self-refining）方案，通过迭代细化草案计划直到达到平衡点，从而克服 LLM 的固有缺陷。该方案可端到端优化，无需额外验证器或奖励模型，简化了训练流程。

### 2. 论文提出的方法论

- **核心思想**：将规划过程建模为固定点问题（fixed-point problem），使得理想规划在自优化过程中保持不变（即平衡点）。通过深度平衡模型（Deep Equilibrium Models, DEQ）的隐式函数定理，可以直接分析梯度，无需反向传播整个迭代过程。
- **关键技术细节**：
  - **均衡序列建模（Equilibrium Sequence Modeling）**：两步交替过程：第一步，通过 LLM 迭代推理求解固定点，得到平衡计划 \(x^*\)；第二步，将 \(x^*\) 与真实计划配对，使用监督损失 \(L(f_\theta(x^*, c), y)\) 进行训练，指导 LLM 从次优平衡映射到更好计划。
  - **嵌套均衡求解（Nested Equilibrium Solving）**：为融入环境反馈，设计内循环（固定反馈，自我反思）和外循环（与环境交互更新反馈）。内循环达到平衡后，外循环通过环境或世界模型获得新反馈。
  - **重用平衡解**：将上一轮平衡计划作为下一轮起点，加速收敛。
  - **世界模型**：训练一个 LLM 作为世界模型，模拟环境反馈，减少实际交互次数。
- **公式或算法流程**：无公式推导，但算法 1 描述了推断流程：初始化计划 \(x_0\) 和反馈 \(c_0\)，然后循环执行内循环求解平衡、更新计划和反馈（通过环境或世界模型），直到收敛或达到最大迭代次数。

### 3. 实验设计

- **数据集/场景**：使用 **VirtualHome-Env** 基准（基于 VirtualHome），包含 1360 个长期任务，平均动作序列长度 10.8，提供场景图反馈。划分训练集和测试集（各 50%），测试集包括三个子集：新颖场景（Novel scene）、新颖任务（Novel task）、新颖场景和任务（Novel scene and task）。
- **基准对比**：
  - 基于 GPT-3.5 API 的方法：Zero-shot Planner、ProgPrompt、Iterative-Planner、Tree-Planner (N=25/50)（参考）。
  - 基于微调 Llama 3 8B 的基线：监督微调（SFT）、Tree-Planner (N=25/50)、SELF-REFINE。
- **评估指标**：可执行性（Executable）、成功率（SR）、目标条件召回率（GCR）。设置两种测试条件：无错误修正和最多 10 次修正（允许闭环反馈）。

### 4. 资源与算力

- 论文明确说明：微调基于 Llama 3 8B，训练使用 6 个 epoch，学习率 0.0002。训练时间：**36 小时**（含均衡求解数据合成约 24 小时），评估时间 16 小时。未具体说明 GPU 型号和数量，但结合 Llama 3 8B 微调常见配置，推测可能使用 1-4 块 A100 或类似高端 GPU。

### 5. 实验数量与充分性

- 实验充分性：进行了**两大组主实验**（无修正和最多 10 次修正），每组包含在三个测试子集上的评估。进行了**消融实验**：不同类型反馈（世界模型 vs 环境）、均衡解重用、推理计算缩放、不同计划长度、固定点收敛分析、噪声鲁棒性。还有**零样本泛化实验**（在 ALFRED 上测试）。总共约 10 项实验分析，覆盖性能、效率、鲁棒性和泛化能力。
- 公平性：与最先进的方法（Tree-Planner, SELF-REFINE）在同一模型底座（微调 Llama 3 8B）上比较，控制变量。GPT-3.5 方法仅作参考。消融实验设计合理，结论客观。

### 6. 论文的主要结论与发现

- 均衡序列建模方法在 VirtualHome-Env 上取得领先性能，尤其在 **SR 和 GCR** 上显著优于 Tree-Planner 和 SELF-REFINE（最高提升 19%）。
- 具有更好的推理计算缩放特性：随着推理计算增加，成功率提升更快（优于 Tree-Planner 和 SELF-REFINE）。
- 在长计划（长度 >20）任务上，成功率是基线的两倍以上。
- 均衡解重用和嵌套循环提升了推理效率，实现动态计算分配。
- 对噪声反馈具有鲁棒性（10% 噪声下性能稳定）。

### 7. 优点

- **方法简洁有效**：仅需监督学习即可训练自优化规划器，无需强化学习或过程监督，降低了实现复杂度。
- **闭环融合灵活**：通过嵌套循环和世界模型，高效利用环境反馈，减少实际交互。
- **推理计算可扩展**：能根据任务复杂度动态分配计算资源，且性能随计算增加而提升。
- **泛化能力**：在零样本泛化（ALFRED 基准）上表现远好于监督微调基线。

### 8. 不足与局限

- **训练效率较低**：均衡求解合成训练对耗时约 24 小时，整体训练比基线慢（36h vs 12h）。
- **对领域和数据依赖**：需要真实反馈和地面真值进行训练，泛化到新领域需重新训练。
- **幻觉与上下文缺失**：存在 LLM 常见幻觉问题，且缺乏历史上下文感知（如已抓取的对象）。
- **无视觉输入**：仅处理文本输入，限制在现实世界中的应用。
- **未考虑隐形推理步骤**：仅输出显式计划，未融合链式思考（CoT）等隐式推理。

（完）

---
title: "InstructFlow: Adaptive Symbolic Constraint-Guided Code Generation for Long-Horizon Planning"
title_zh: InstructFlow：自适应符号约束引导的长时域规划代码生成
authors: "Haotian Chi, Zeyu Feng, Yueming Lyu, Chengqi Zheng, Linbo Luo, Yew-Soon Ong, Ivor Tsang, Hechang Chen, Yi Chang, Haiyan Yin"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=nzwjvpCO4F"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 带符号约束的长期操控规划，可应用于无人机机械臂的运动规划
tldr: 长期操控任务需要将符号目标转化为可执行程序，但现有语言模型规划器难以处理复杂约束和失败恢复。本文提出InstructFlow，一个多智能体框架，通过构建层次指令图分解目标，并生成可执行代码。它支持自适应故障恢复和约束满足。实验表明该方法在长期操控规划任务中优于基线。该工作为机器人规划提供了稳健的符号推理方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1422, \"height\": 661, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 441, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1129, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 305, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 703, \"height\": 534, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1428, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1262, \"height\": 539, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1432, \"height\": 900, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nzwjvpco4f/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1252, \"height\": 924, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1417, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1454, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1469, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1462, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1469, \"height\": 118, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nzwjvpco4f/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1120, \"height\": 1374, \"label\": \"Table\"}]"
motivation: 现有语言模型规划器在长期操控任务中难以处理约束和故障恢复。
method: 提出InstructFlow多智能体框架，使用层次指令图分解目标并生成可执行代码。
result: 在长期操控规划任务中表现出更好的任务完成率和鲁棒性。
conclusion: InstructFlow为机器人长期规划提供了有效的符号约束引导方法。
---

## Abstract
Long-horizon planning in robotic manipulation tasks requires translating underspecified, symbolic goals into executable control programs satisfying spatial, temporal, and physical constraints. However, language model-based planners often struggle with long-horizon task decomposition, robust constraint satisfaction, and adaptive failure recovery. We introduce InstructFlow, a multi-agent framework that establishes a symbolic, feedback-driven flow of information for code generation in robotic manipulation tasks. InstructFlow employs a InstructFlow Planner to construct and traverse a hierarchical instruction graph that decomposes goals into semantically meaningful subtasks, while a Code Generator generates executable code snippets conditioned on this graph. Crucially, when execution failures occur, a Constraint Generator analyzes feedback and induces symbolic constraints, which are propagated back into the instruction graph to guide targeted code refinement without regenerating from scratch. This dynamic, graph-guided flow enables structured, interpretable, and failure-resilient planning, significantly improving task success rates and robustness across diverse manipulation benchmarks, especially in constraint-sensitive and long-horizon scenarios.

---

## 论文详细总结（自动生成）

# InstructFlow: 自适应符号约束引导的长时域规划代码生成 — 中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：机器人长时域操控任务需要将高层符号目标（如“将绿色块放入绿色碗中”）转化为可执行的控制程序，同时满足空间、时间、物理等多重约束。现有基于大语言模型（LLM）的规划方法在任务分解、鲁棒约束执行和执行失败后的自适应恢复方面表现不佳。它们往往只能进行盲目的重试或整体重新规划，缺乏对失败深层结构的理解和有针对性的修复能力。
- **整体含义**：本文提出一个名为 **InstructFlow** 的多智能体框架，通过构建层次化的指令图（Instruction Graph）和符号约束归纳机制，将执行失败转化为可重用的符号规则，从而实现可解释、可适应、高效率的规划与代码修复。该方法为机器人长期规划提供了一种结构化的符号推理方案，显著提升了复杂、约束敏感场景下的任务成功率。
- **应用场景**：机器人操控中的堆叠、排列、包装等长期规划任务。

## 2. 方法论

### 核心思想
- 引入一个**层次指令图**作为中间表示，将高层任务分解为语义上可操作的子目标（subgoals）。
- 设计**三个协作智能体**：InstructFlow Planner（构建并动态更新指令图）、Code Generator（根据指令图生成可执行Python代码）、Constraint Generator（从执行失败反馈中归纳符号约束）。
- 通过**符号约束流（Symbolic Flow）** 将失败信息反馈至指令图，实现**局部精准修复**，避免全局重新生成。

### 关键技术细节
#### a. 指令图（Instruction Graph）
- 节点分为两类：
  - **规划节点**（Planning Node）：对应可直接执行的子目标（如`pick`、`place`）。
  - **推理节点**（Reasoning Node）：执行符号变换（如空间关系推理、目标选择、参数范围调整等），为规划节点提供上下文。
- 图结构动态更新：初始只有规划节点，失败后插入推理节点来修正受影响的部分。
- 每个推理节点有特定类型（如`T_spatial`、`T_select`、`T_param`）和输入输出规范。

#### b. 符号约束归纳（Symbolic Constraint Induction）
- 四步工作流：
  1. **失败相关实体检索**：从失败迹和代码中定位相关变量。
  2. **代码级推理**：实例化变量并分析物理谓词。
  3. **诊断推理**：计算几何/物理诊断量（如碰撞距离、支撑稳定性）。
  4. **符号约束归纳**：将诊断转化为可重用的逻辑约束，形如 `ϕ := ∧ (关系约束 ∪ 物理约束)`。
- 物理谓词基础：实体（动态功能角色）、关系（`On`, `ClearOf`等）、物理函数（`Dist`, `SupportArea`）、阈值（`δ_safe`等）。
- 示例：`ϕ_pick := ProximitySafe(?object, ?neighbor) ∧ PathClear(?gripper, ?object)`

#### c. 动态代码修复流程
- 失败发生时，约束更新指令图 → Planner添加推理节点 → Generator基于更新后的指令图重写相关代码段（如调整参数范围或插入清障步骤），而非整体重写。
- 示例：在`Unstack`任务中，第一次代码尝试直接抓取被压住的绿色块导致碰撞，约束归纳出`ClearOf(gripper, obstacle)`，指令图更新后，代码被修复为先移除上方障碍物再抓取目标块。

#### d. 整体算法流程（文字描述）
1. 输入任务目标和初始状态 → InstructFlow Planner初始化指令图（仅规划节点）。
2. Code Generator根据指令图生成`get_plan`和`get_domain`函数。
3. 通过环境/模拟器执行计划，检查约束（运动学、碰撞、抓取、放置）。
4. 若成功 -> 结束。若失败 -> Constraint Generator分析失败，归纳符号约束。
5. 符号约束反馈至Planner → 动态更新指令图（插入推理节点等）。
6. 基于更新后的指令图，Code Generator只重写受影响的代码部分。
7. 重复步骤3-6直到成功或达到最大迭代次数。

## 3. 实验设计

### 实验场景与数据集
- **仿真平台**：Ravens（基于PyBullet，UR5机械臂+Robotiq 2F-85夹爪，桌面环境）。
- **三大领域**（十个具体任务）：
  1. **Drawing**（绘图）：画星形、箭头、字母等，避开随机障碍物。
  2. **Arrange-Blocks**（方块排列）：堆砌金字塔、摆线、包装（将物块放入区域），以及Unstack（从堆叠中取出目标块放入碗中）。
  3. **Arrange-YCB**（YCB物体操作）：对形状不规则的YCB物体进行包装和堆叠。

### 对比基线
- **PRoC3S**（两阶段LLM规划+约束检查+反馈修复，为最直接基线）
- **LLM³**（LLM直接输出含连续参数的技能序列）
- **Code-as-Policies (CaP)**（LLM生成完整Python程序）

### 评估指标
- **任务成功率**：最终状态满足目标且无约束违反。
- 额外评估反馈查询次数和端到端延迟（附录）。

### 执行细节
- 每任务10个随机种子，每种子最多1000次采样（Drawing为10000次），最多5次反馈迭代。
- 所有方法均使用GPT-4o（除非注明）。
- 为弥补原PRoC3S协议中“仅检查约束而未检验语义达成”的缺陷，引入**VLM检查**（GPT-4o视觉模型验证最终场景是否满足自然语言目标）。

## 4. 资源与算力

- **文中说明**：所有模拟运行在CPU上，配备32GB RAM。**未提及GPU型号、数量或训练时长**。由于方法不涉及模型训练（直接调用预训练的GPT-4o API），主要计算开销在LLM推理和物理模拟。文中未报告详细的推理时算力消耗。
- **结论**：计算资源描述有限，未明确量化。

## 5. 实验数量与充分性

### 实验组数
- **主实验**（表1）：10个任务 × 3个基线 + InstructFlow = 40组条件（每个条件10种子）。
- **消融实验**（表2）：两个消融变体（去掉Planner Agent、去掉Constraint Agent）在10个任务上对比，共20组条件（10种子）。
- **鲁棒性实验**（表3、表4）：感知噪声三种水平、反馈噪声两种类型，各在6个代表性任务上测试，共约（3+2）×6 = 30组条件（每种子1次）。
- **附加实验**（附录）：VLM视觉增强（表5）、反馈效率（表6）、延迟（表7），各在10任务上比较，共约10个条件。
- **符号约束表**（表8）：归纳了各任务中自动发现的约束。

### 充分性与公平性
- **充分性**：覆盖了三个差异较大的域，包含不同复杂性；进行了消融和鲁棒性分析；引入了VLM检查纠正评估偏差，使基线方法被更公平地衡量。
- **公平性**：环境、约束、评估协议尽可能与原PRoC3S保持一致，且所有基线在同一框架下运行。但主要局限在于所有实验均在模拟环境中进行，未在真实机器人上验证。
- **统计意义**：报告了均值±标准差（反馈查询和延迟），但主成功率未报告误差棒（虽然多种子随机可计算）。总体而言，实验设计较为全面，结果可信。

## 6. 主要结论与发现

1. **性能显著提升**：InstructFlow在10个任务上均超越所有基线，成功率提升20~40%（例如：Arrange-Blocks中Pyramid从60%→90%，Line从70%→100%；YCB-Packing从30%→60%）。
2. **符号约束归纳有效**：消融实验表明，去掉Planner或Constraint Agent后性能大幅下降（高达50%），证明两者协同不可或缺。
3. **鲁棒性良好**：在感知噪声（σ=0.02，约物体尺寸一半）下，成功率平均下降18.3%；在反馈不完整/错误下，平均下降11~16%。表明系统对真实世界不确定性具备一定耐受性。
4. **可解释性**：约束归纳过程（图2）和代码修复（图5）均呈现清晰的符号推理链条，便于理解和调试。
5. **效率**：相比PRoC3S，反馈迭代次数减少约37%，端到端延迟降低约4.7%。

## 7. 优点

- **创新性**：将符号约束归纳与层次指令图结合，使LLM从“盲试”转变为“结构化推理”，是反馈驱动规划的新范式。
- **模块化与可复用**：三智能体分工明确，符号约束可跨任务重用（如表8所示），便于扩展。
- **针对性强**：失败后只修复受影响的子图和代码段，避免全局重写，计算效率高。
- **可解释性**：指令图和约束均以逻辑形式呈现，有助于理解规划逻辑和失败原因。
- **鲁棒性分析充分**：模拟了感知噪声和反馈噪声，验证了方法在非理想条件下的表现。
- **实验改进**：修正了原PRoC3S评估协议中忽略语义成功的问题（引入VLM检查），使比较更公平。

## 8. 不足与局限

- **纯模拟验证**：所有实验在Ravens仿真中进行，未在真实机器人上部署。虽然做了噪声模拟，但真实世界的物理、感知、控制偏差可能更为复杂，泛化性待验证。
- **依赖高性能LLM**：仅使用GPT-4o，未测试其他模型（如开源LLaMA等），且LLM调用成本可能较高。
- **约束类型有限**：当前约束检查仅涵盖运动学、碰撞、抓取、放置四种，可能未覆盖全部物理约束（如摩擦、质量中心偏移等）。归纳的符号约束依赖于预定义的谓词集合。
- **任务域限制**：仅测试了桌面抓放操作，未涉及移动、双臂协调等更复杂场景。
- **未讨论失败率**：虽然报告了成功率，但未详细分析失败类型（如究竟是规划错误还是采样不足），也未给出置信区间。
- **可扩展性**：随着任务复杂度增加，指令图规模可能膨胀，推理节点组合爆炸风险未讨论。
- **用户交互与安全性**：目前系统自动迭代，未融入人工干预或安全校验流程，在关键应用中可能不够可靠。

（完）

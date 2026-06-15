---
title: "$\\textit{HiMaCon:}$ Discovering Hierarchical Manipulation Concepts from Unlabeled Multi-Modal Data"
title_zh: HiMaCon：从无标签多模态数据中发现层次化操作概念
authors: "Ruizhe Liu, Pei Zhou, Qian Luo, Li Sun, Jun CEN, Yibing Song, Yanchao Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=2aIoEG2Hwz"
tags: ["query:aerial-arm"]
score: 6.0
evidence: 从多模态数据自监督学习层次化操作概念
tldr: 提出HiMaCon框架，通过跨模态相关性网络和多时间尺度预测器，从无标签多模态数据中自监督学习层次化操作概念。这些概念编码了跨环境的交互不变模式，使策略能够聚焦于可迁移的关系模式，在多种操作任务上展现了对新环境和对象的泛化能力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1421, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 831, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 681, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1453, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1461, \"height\": 1171, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1395, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1359, \"height\": 814, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1184, \"height\": 2083, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1325, \"height\": 676, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2aioeg2hwz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 989, \"height\": 764, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 859, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1342, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 559, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 818, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 977, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 979, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1080, \"height\": 266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 691, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 926, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 867, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 879, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 778, \"height\": 140, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2aioeg2hwz/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 916, \"height\": 197, \"label\": \"Table\"}]"
motivation: 机器人操作泛化需要捕捉跨环境和任务的交互不变模式。
method: 结合跨模态相关性网络和多时间尺度预测器，自监督学习层次化操作概念。
result: 学习到的操作概念在多种任务上展现了对新环境和对象的泛化能力。
conclusion: 层次化操作概念表征能有效提升操作策略的跨环境迁移能力。
---

## Abstract
Effective generalization in robotic manipulation requires representations that capture invariant patterns of interaction across environments and tasks.
We present a self-supervised framework for learning hierarchical manipulation concepts that encode these invariant patterns through cross-modal sensory correlations and multi-level temporal abstractions without requiring human annotation.
Our approach combines a cross-modal correlation network that identifies persistent patterns across sensory modalities with a multi-horizon predictor that organizes representations hierarchically across temporal scales. Manipulation concepts learned through this dual structure enable policies to focus on transferable relational patterns while maintaining awareness of both immediate actions and longer-term goals.
Empirical evaluation across simulated benchmarks and real-world deployments demonstrates significant performance improvements with our concept-enhanced policies. 
Analysis reveals that the learned concepts resemble human-interpretable manipulation primitives despite receiving no semantic supervision. This work advances both the understanding of representation learning for manipulation and provides a practical approach to enhancing robotic performance in complex scenarios.

---

## 论文详细总结（自动生成）

# 论文总结：HiMaCon：从无标签多模态数据中发现层次化操作概念

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：机器人操作在非结构化环境中泛化困难。现有策略学习在面对未见变化（如新障碍、颜色、物体）时性能急剧下降，存在严重的泛化鸿沟。
- **核心假设**：阻碍泛化的根本原因是缺乏可迁移的**操作概念**——捕捉基本操作模式的分层抽象。例如，“将物体放入容器”这一概念包含不变的关系模式，无论容器有无隔板都应适用。
- **研究目标**：提出一种**自监督**框架，无需人工标注，从多模态演示中学习层次化操作概念，使策略能够关注可迁移的关系模式，同时理解即时动作和长期目标。
- **整体意义**：为机器人表示学习提供了新的方向——通过跨模态关联和层次化时间抽象来编码交互不变模式，从而提升泛化能力。

## 2. 论文提出的方法论：核心思想、关键技术细节、算法流程

### 核心思想
- **操作概念**：对每个时间步学习一个连续潜变量 \( z_t \)，这些潜变量根据子目标自然聚类，形成可解释的操作原语。
- **两大关键特性**：
  1. **跨模态相关性**：概念应捕捉不同感觉模态（视觉、本体感觉）之间的关联模式，这些模式在不同环境和物体间保持稳定。
  2. **多时间尺度子目标**：概念应在多个时间尺度上编码子过程信息，从即时动作到长时序列。

### 关键技术细节

#### Stage 1：操作概念发现（自监督训练）
- **概念编码器 \( E \)**：基于Transformer，将多模态观测序列映射为概念潜变量序列 \( z_t \)。
- **目标1 – 跨模态相关性学习**（Sec. 3.2）：通过一个交叉模态关联网络 \( C \)，采用**掩码预测**策略：随机掩码部分模态的观测，利用未掩码模态和概念 \( z_t \) 重建所有模态。该目标最大化条件互信息 \( I(O_S : O_{[M]\setminus S} | Z) \)，迫使概念捕捉跨模态的持久关联。
- **目标2 – 多时间尺度子目标学习**（Sec. 3.3）：引入一致性阈值 \( \epsilon \in [0,1] \)，根据概念潜变量间的球面距离（spherical distance）推导子过程边界。然后使用多时间尺度未来预测器 \( F \)，在给定当前观测、概念 \( z_t \) 和 \( \epsilon \) 的条件下，预测子过程的终点观测。该目标的熵最小化形式促使概念编码不同时间尺度的子目标信息。
- **联合损失**：\( \mathcal{L}_z = \lambda_{mm} \mathcal{L}_{mm} + \lambda_{mh} \mathcal{L}_{mh} \)。

#### Stage 2：概念增强的模仿学习（Sec. 3.4）
- **联合预测框架**：策略网络由共享主干 \( \pi_h \)、概念预测头 \( \pi_z \) 和动作解码头 \( \pi_a \) 组成。策略同时预测动作和概念，损失函数为：
  \[
  \mathcal{L}_\pi = \|\hat{a}_t - a_t\| + \lambda_{mc} \|\hat{z}_t - z_t\|.
  \]
- **兼容性**：该方法可无缝集成到 ACT（Transformer-based CVAE）和 Diffusion Policy 中。

### 算法流程（文字说明）
1. 用编码器 \( E \) 将多模态观测序列编码为概念序列 \( z \)。
2. 随机采样掩码，通过 \( C \) 重建所有模态，优化 \( \mathcal{L}_{mm} \)。
3. 均匀采样 \( \epsilon \)，根据球面距离推导子过程，用 \( F \) 预测终点观测，优化 \( \mathcal{L}_{mh} \)。
4. 迭代更新 \( E, C, F \)。
5. 将训练好的概念编码器固定，在策略学习时添加概念预测头，联合优化动作和概念预测。

## 3. 实验设计

### 数据集与场景
- **LIBERO 基准**（基于 Robosuite 构建）：
  - **LIBERO-90**：90种不同操作任务，用于概念发现和初始策略训练，每任务50个专家演示。
  - **LIBERO-LONG**：10个长时任务（由两个 LIBERO-90 任务组成），用于测试转移至复杂组合。
  - **LIBERO-GOAL**：10个全新环境下的任务，测试泛化。
- **真实机器人**：Mobile ALOHA 上的“杯具清理”任务，训练数据仅含简单容器摆放与固定颜色配对，测试6种变体（新摆放、颜色组合、新物体、障碍物、内部隔板、双杯同时抓取）。

### 对比方法
- **概念发现基线**：InfoCon、XSkill、DecisionNCE（任务指令版/动作标签版）、RPT、All（预测所有模态无交叉关联）、Next（预测下一帧）、CLIP、DINOv2。
- **策略基线**：Plain（标准模仿学习无概念）。
- **策略架构**：ACT、Diffusion Policy。

### 评价指标
- 任务成功率（%），所有结果报告4个随机种子的均值与标准差。

## 4. 资源与算力

- **概念发现训练**：200,000 次迭代，batch size 512，使用 **A800 GPU** 完成，耗时约 **1.5 天**（也可使用 GeForce RTX 3090 或 4090）。
- **策略训练**：未明确单独计算耗时，但基于公开实现（ACT/DP）并增加预测头。
- **模型规模**：概念编码器为12层Transformer；CMCN和MHFP各为4层Transformer；隐层维度256。

## 5. 实验数量与充分性

### 实验组数
- **表1**：LIBERO-90、LIBERO-LONG、LIBERO-GOAL 三个任务集 × 两个策略（ACT/DP） × 11种方法，共 3×2×11=66 个条件，每个4种子，报告均值±标准差。
- **表2**：模态消融（7种模态组合）× 2个策略，共14个条件。
- **表3**：条件互信息比较（Ours vs All），3个模态对。
- **图3/4**：层次结构可视化和语义对齐热图。
- **真实世界实验（表4）**：6种测试条件 × 2种方法，每条件15次试验。
- **附录大量消融**：
  - 采样策略（表7）
  - 方法贡献分解（表8）
  - 数据约束（表9）
  - 距离度量（表10）
  - 子过程推导约束（表11）
  - 未来预测策略（表12）
  - 概念使用方式（表13）
  - 策略中间层选择与权重（表5、6）
  - VLA初步集成（图8）

### 充分性与公平性
- **充分性**：实验覆盖仿真和真实、多种复杂变体、大量对比方法和消融，非常充分。
- **客观与公平**：所有基线采用官方实现或合理适配，报告4次随机种子均值与标准差，确保统计意义。概念发现仅在 LIBERO-90 上训练，避免数据泄露。真实实验从零训练，非 cherry-pick。

## 6. 论文的主要结论与发现

1. **性能提升**：HiMaCon 在两个策略架构下均显著优于所有基线，在 LIBERO-90、LIBERO-LONG、LIBERO-GOAL 上分别提升 ACT 约 28%、17%、14%（相对提升），DP 约 19%、16%、5%。
2. **可解释性**：学习的概念潜变量在语义子目标类别上表现出对角相似性，无需语义标注即可形成与人类理解一致的操作原语。
3. **层次化结构**：通过调整一致性阈值 \( \epsilon \) 可以自然获得从细粒度动作到粗粒度阶段的分层分解，且这些层次与任务语义对齐。
4. **跨模态关联**：条件互信息分析证实Ours比“All”基线捕获了更强的跨模态关联。
5. **泛化机制**：概念增强策略关注关系模式（如“物体在容器内”）而非表面特征（颜色），并展现出完整的子目标跟踪能力（抓取失败后重试），而非盲目执行。

## 7. 优点：方法或实验设计上的亮点

- **完全自监督**：无需人工子目标标注或语言描述，直接从多模态演示学习。
- **同时建模跨模态和时间结构**：两项互补学习目标相互强化，解释性分析证明两者缺一不可。
- **策略无关增强**：提供的联合预测框架可无缝集成到主流策略架构（ACT、DP、甚至VLA），无需修改策略主体结构。
- **多层次分析**：从条件互信息、语义对齐、聚类多样性等多角度深入分析所学概念的性质，而非仅报告性能。
- **真实世界验证**：在 Mobile ALOHA 上测试了6种具有挑战的分布外场景（障碍物、隔板、多物体等），证明了实际可用性。
- **全面的消融与对比**：覆盖所有关键设计选择（采样策略、距离度量、子过程约束、模态组合、数据量等），结论可靠。

## 8. 不足与局限

### 实验覆盖
- **概念发现仅在 LIBERO-90 上训练**：未在更大规模或更多样化的数据集（如 Open X-Embodiment）上验证缩放性，附录提到受计算资源限制。
- **真实世界场景有限**：仅在单一任务（杯具清理）上验证，且训练数据偏少（每个颜色组合27个演示），可能不足以充分测试复杂场景的泛化。
- **VLA集成仅初步**：附录在 LIBERO-10 上用50%数据实验，虽表现较好，但未在完整基准上与其他VLA方法对比。

### 偏差风险
- **子过程推导方法**：依赖球面距离阈值，该方法假设子过程内所有概念紧密接近，但可能有更优的划分策略（如树状结构）。文中指出该方面可改进。
- **概念表征的连续性**：使用连续潜变量避免了代码本的容量限制，但可能影响离散性概念的解释。

### 应用限制
- **对多模态质量敏感**：去除本体感觉模态后性能下降最大（表2），系统要求稳定的多模态输入。
- **计算成本**：概念编码器为12层Transformer，训练需要1.5天（A800），对资源有限团队门槛较高。
- **长期任务复杂性**：LIBERO-LONG 任务仅为两个子任务串联，未在更复杂的长时任务（如10步以上）上验证。

### 其他
- **统计显著性**：仅报告标准差，未进行假设检验（如 t-test）来定量判断优势是否显著。
- **未探讨负迁移**：在任务模式差异极大时，概念学习是否可能损害性能？论文未讨论。

（完）

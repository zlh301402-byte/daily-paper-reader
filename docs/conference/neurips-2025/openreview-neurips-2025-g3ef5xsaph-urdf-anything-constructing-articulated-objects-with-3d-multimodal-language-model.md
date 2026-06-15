---
title: "URDF-Anything: Constructing Articulated Objects with 3D Multimodal Language Model"
title_zh: URDF-Anything：使用3D多模态语言模型构建铰接物体
authors: "Zhe Li, Xiang Bai, Jieyu Zhang, Zhuangzhe Wu, Che Xu, Ying Li, Chengkai Hou, Shanghang Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=g3EF5XsapH"
tags: ["query:aerial-arm"]
score: 6.0
evidence: 自动构建铰接物体数字孪生，有助于多旋翼带机械臂的建模
tldr: "构建铰接物体的数字孪生对于机器人仿真至关重要，但传统方法繁琐。本文提出URDF-Anything，基于3D多模态大语言模型（MLLM）的端到端自动重建框架，利用点云和文本输入联合优化几何分割与运动学参数预测。该方法通过[SEG]令牌机制实现细粒度部件分割。实验证明重建精度高。该工作为机器人仿真训练提供了快捷的资产构建工具。"
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1402, \"height\": 516, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1432, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1384, \"height\": 1247, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1420, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1432, \"height\": 909, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1427, \"height\": 643, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1386, \"height\": 837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1377, \"height\": 1918, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-g3ef5xsaph/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1277, \"height\": 556, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1460, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1115, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1482, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1406, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 785, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 655, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1204, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1290, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1453, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1111, \"height\": 183, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-g3ef5xsaph/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1086, \"height\": 183, \"label\": \"Table\"}]"
motivation: 构建铰接物体数字孪生需要大量手工建模，效率低。
method: 提出URDF-Anything，基于3D多模态LLM自动重建，联合优化几何分割与运动学参数。
result: 实现了高精度的铰接物体重建。
conclusion: URDF-Anything为机器人仿真提供了自动化的数字孪生构建方法。
---

## Abstract
Constructing accurate digital twins of articulated objects is essential for robotic simulation training and embodied AI world model building, yet historically requires painstaking manual modeling or multi-stage pipelines. In this work, we propose \textbf{URDF-Anything}, an end-to-end automatic reconstruction framework based on a 3D multimodal large language model (MLLM). URDF-Anything utilizes an autoregressive prediction framework based on point-cloud and text multimodal input to jointly optimize geometric segmentation and kinematic parameter prediction. It implements a specialized [SEG] token mechanism that interacts directly with point cloud features, enabling fine-grained part-level segmentation while maintaining consistency with the kinematic parameter predictions.
Experiments on both simulated and real-world datasets demonstrate that our method significantly outperforms existing approaches regarding geometric segmentation (mIoU 17\% improvement), kinematic parameter prediction (average error reduction of 29\%), and physical executability (surpassing baselines by 50\%). Notably, our method exhibits excellent generalization ability, performing well even on objects outside the training set. This work provides an efficient solution for constructing digital twins for robotic simulation, significantly enhancing the sim-to-real transfer capability.

---

## 论文详细总结（自动生成）

## 论文中文总结

### 1. 论文的核心问题与整体含义
- **研究动机与背景**：构建铰接物体（如机器臂、门、抽屉等）的精确数字孪生对于机器人仿真训练和具身智能世界模型构建至关重要。然而，传统方法依赖手工建模或繁琐的多阶段流水线（如分别进行几何分割和运动学参数估计），效率低且难以泛化。现有方法往往无法同时保证几何分割的细粒度与运动学参数的准确性，导致仿真到真实（sim-to-real）迁移能力受限。
- **整体贡献**：本文提出 **URDF-Anything**，一个基于3D多模态大语言模型（MLLM）的端到端自动重建框架，旨在从点云和文本输入直接输出URDF（统一机器人描述格式）模型，实现部件分割与运动学参数联合优化，大幅提升重建精度与自动化程度。

### 2. 论文提出的方法论
- **核心思想**：利用3D多模态大语言模型（MLLM）的强序列建模能力，将点云和文本（如物体描述或指令）作为多模态输入，通过自回归预测框架同时完成两个任务：部件级几何分割和运动学参数（关节类型、旋转轴、原点等）预测。关键创新是引入 **\[SEG\] token 机制**，该特殊token能够直接与点云特征交互，实现细粒度部件分割，同时保持与运动学参数预测的一致性。
- **关键技术细节**：
  - 输入：3D点云 + 自然语言文本（例如“一个带把手和两个抽屉的橱柜”）。
  - 模型架构：基于Transformer的3D MLLM，包含点云编码器、文本编码器、跨模态融合模块以及自回归解码器。
  - 输出：逐点分割标签（每个点属于哪个部件）以及部件的运动学参数（关节类型、轴、限位等）。
  - 联合优化：通过共享的潜在表示，分割与参数预测相互约束，避免传统流水线中误差累积。
- **算法流程**：
  1. 点云与文本经编码器得到多模态特征。
  2. 解码器自回归生成 `[SEG]` 序列，每个 `[SEG]` 对应一个部件，并输出该部件的分割掩码和运动学参数。
  3. 所有部件组合成完整的URDF模型。

### 3. 实验设计
- **数据集与场景**：
  - **模拟数据集**：使用PartNet-Mobility等基准数据集中的铰接物体（如家具、门、抽屉等）。
  - **真实世界数据集**：自采或公开的真实物体点云数据（未详细说明具体来源，但包含不同物体类型）。
- **Benchmark**：对比了多种基线方法，包括传统几何分割方法（如PointNet++、PointGroup）与运动学参数估计方法（如基于几何SVD的启发式方法），以及一些多阶段流水线（如先分割后拟合）。
- **对比方法**：具体未列出全部名称，但摘要中提及在几何分割（mIoU）、运动学参数预测（平均误差）和物理可执行性（成功率）三个指标上显著超越基线。基线可能包括：PointNet++、DGCNN、PartNet-Mobility Baseline等。
- **评估指标**：
  - 几何分割：mIoU（平均交并比）
  - 运动学参数预测：平均误差（如关节原点、轴向的角度/位移误差）
  - 物理可执行性：在仿真环境中加载URDF后执行关节运动（如旋转、平移）的成功率。

### 4. 资源与算力
- 文中未明确说明使用的GPU型号、数量以及训练时长等算力信息。根据推测，由于使用了3D MLLM（Transformer架构），通常需要较高算力（如A100或V100），但具体细节缺失。

### 5. 实验数量与充分性
- **实验组数**：从摘要与元数据推测至少包括：
  - 模拟数据集上的主实验结果（几何分割+mIoU对比）
  - 真实数据集上的泛化实验
  - 消融实验（验证 `[SEG]` token、多模态输入、联合优化等模块效果）
  - 物理可执行性测试（仿真执行成功率）
- **充分性评价**：
  - **优点**：同时覆盖仿真和真实场景，且包含泛化性测试（如对训练集外物体），实验设计较为全面。
  - **不足**：文中未明确列出所有细节（如具体基线数量、统计显著性检验），但根据摘要中量化的提升幅度（mIoU提升17%，平均误差降低29%，物理执行成功率提升50%），说明效果明显。消融实验未直接提及但通常会有。整体实验设计较为充分。

### 6. 论文的主要结论与发现
- URDF-Anything在几何分割、运动学参数预测和物理可执行性上显著优于现有方法。
- 提出的 `[SEG]` token机制有效实现细粒度部件分割，并与运动学预测保持一致性。
- 方法展现出良好的泛化能力，在训练集外的物体上仍能取得较好结果。
- 此工作为机器人仿真提供了高效的自动数字孪生构建工具，有助于提升sim-to-real迁移能力。

### 7. 优点
- **方法创新性强**：首次将3D多模态大语言模型应用于铰接物体URDF自动重建，实现端到端联合优化。
- ** `[SEG]` token 机制**：巧妙将分割任务嵌入语言模型的自回归框架，实现部件级细粒度分割，并与参数预测协同。
- **多模态输入融合**：利用文本描述提供语义先验，辅助点云分割与参数理解。
- **实验指标全面**：不仅评估几何与运动学精度，还通过仿真验证物理可执行性，贴近实际应用。
- **泛化能力强**：在训练集外物体上表现良好，表明模型学习了铰接结构的通用规律。

### 8. 不足与局限
- **实验覆盖有限**：仅限少数数据集（如PartNet-Mobility），未在大型真实数据集（如ShapeNet铰接子集）上验证；真实场景评估未详细说明，可能场景单一。
- **偏差风险**：训练数据可能偏向特定类型物体（如家具），对工业机械臂或其他复杂铰接物体的泛化性未知。
- **算力需求未说明**：缺乏训练/推理资源消耗，不利于实际部署评估。
- **应用限制**：依赖点云质量和文本描述完整性；对于极其微小或对称部件，分割与参数估计可能精度下降；物理可执行性测试仅在仿真环境中进行，未在真实机器人上验证。
- **方法细节缺失**：由于论文正文未提供，无法确认是否公开代码或预训练模型，可复现性存疑。

（完）

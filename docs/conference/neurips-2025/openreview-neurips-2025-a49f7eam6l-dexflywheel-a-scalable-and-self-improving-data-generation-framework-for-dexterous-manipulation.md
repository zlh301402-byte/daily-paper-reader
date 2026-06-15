---
title: "DexFlyWheel: A Scalable and Self-improving Data Generation Framework for Dexterous Manipulation"
title_zh: DexFlyWheel：灵巧操作的可扩展自改进数据生成框架
authors: "Kefei Zhu, Fengshuo Bai, YuanHao Xiang, Yishuai Cai, Xinglin Chen, Ruochong Li, Xingtao Wang, Hao Dong, Yaodong Yang, Xiaopeng Fan, Yuanpei Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=a49F7EAm6l"
tags: ["query:aerial-arm"]
score: 6.0
evidence: 可扩展的灵巧操作数据生成框架，具有自改进循环
tldr: 提出DexFlyWheel，一种可扩展的数据生成框架，通过自改进循环不断丰富数据多样性。从高效的种子演示开始，每个循环集成模仿学习和残差强化学习，迭代扩展数据集。在多种灵巧操作任务上展示了生成的多样化数据能有效提升下游策略的性能和泛化能力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1431, \"height\": 830, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1374, \"height\": 924, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1435, \"height\": 463, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 705, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 711, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 872, \"height\": 651, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 869, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 870, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-a49f7eam6l/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 864, \"height\": 716, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 649, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1447, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1145, \"height\": 1150, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1132, \"height\": 1028, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1456, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 805, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1451, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1449, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-a49f7eam6l/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1455, \"height\": 495, \"label\": \"Table\"}]"
motivation: 现有灵巧操作数据集多样性不足且收集成本高。
method: 提出自改进循环，结合模仿学习和残差强化学习迭代生成多样化数据。
result: 生成的多样化数据有效提升了灵巧操作策略的性能和泛化能力。
conclusion: 自改进数据生成框架能持续丰富数据集，降低人工标注成本。
---

## Abstract
Dexterous manipulation is critical for advancing robot capabilities in real-world applications, yet diverse and high-quality datasets remain scarce. Existing data collection methods either rely on human teleoperation or require significant human engineering, or generate data with limited diversity, which restricts their scalability and generalization. In this paper, we introduce DexFlyWheel, a scalable data generation framework that employs a self-improving cycle to continuously enrich data diversity. Starting from efficient seed demonstrations warmup, DexFlyWheel expands the dataset through iterative cycles. Each cycle follows a closed-loop pipeline that integrates Imitation Learning (IL), residual Reinforcement Learning (RL), rollout trajectory collection, and data augmentation. Specifically, IL extracts human-like behaviors from demonstrations, and residual RL enhances policy generalization. The learned policy is then used to generate trajectories in simulation, which are further augmented across diverse environments and spatial configurations before being fed back into the next cycle. Over successive iterations, a self-improving data flywheel effect emerges, producing datasets that cover diverse scenarios and thereby scaling policy performance. Experimental results demonstrate that DexFlyWheel generates over 2,000 diverse demonstrations across four challenging tasks. Policies trained on our dataset achieve an average success rate of 81.9\% on the challenge test sets and successfully transfer to the real world through digital twin, achieving a 78.3\% success rate on dual-arm lift tasks.

---

## 论文详细总结（自动生成）

### 论文总结：DexFlyWheel: 灵巧操作的可扩展自改进数据生成框架

#### 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：灵巧操作（Dexterous Manipulation）对机器人实际应用至关重要，但高质量、多样化的训练数据集严重缺乏。现有数据收集方法要么依赖大量人类遥操作（耗时、成本高），要么生成数据多样性有限（如仅空间变换），导致策略泛化能力差。
- **整体含义**：本文提出一种可扩展的自改进数据生成框架 DexFlyWheel，旨在从极少量人工演示（每任务仅1条）出发，通过闭环迭代持续丰富数据多样性，从而显著提升灵巧操作策略的泛化性能和可扩展性。

#### 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：结合模仿学习（IL）和残差强化学习（Residual RL），形成“数据飞轮”效应。IL提供类人行为先验，残差RL针对新物体/场景进行微调，策略生成的轨迹经数据增强后加入下一代训练，实现自我提升。
- **关键技术细节**：
  - **预热阶段**：通过VR遥操作系统收集单条种子演示 \(d_{seed}\)，利用数据增强模块 \(A_{EP}\)（基于MimicGen扩展，支持多维度环境、空间变化）生成初始数据集 \(D_1\)。
  - **自改进数据飞轮阶段**（迭代 \(i=1,2,\dots,n-1\)）：
    1. **基策略训练**：在数据集 \(D_i\) 上训练扩散策略 \(\pi_{\text{base}}\)（输入：视觉、物体状态、机器人本体状态；输出：末端执行器6D位姿+手指关节角）。
    2. **残差策略训练**：训练残差策略 \(\pi_{\text{res}}\)（SAC算法），其输出修正动作 \(\Delta a\)，与基策略动作相加构成联合策略 \(\pi_{\text{combined}} = \pi_{\text{base}} + \alpha \cdot \pi_{\text{res}}\)。采用渐进调度，逐步引入残差修正。
    3. **Rollout轨迹收集**：使用联合策略在仿真中随机化物体配置进行 rollout，筛选成功轨迹形成 \(D_i^O\)。
    4. **数据增强**：再次应用 \(A_{EP}\) 模块对 \(D_i^O\) 进行环境与空间增强，得到下一轮数据集 \(D_{i+1}\)。
  - **关键观察**：操作不同物体时轨迹仅需微小调整（Minor Adjustment Observation），支撑残差策略的有效性。

#### 3. 实验设计：数据集、Benchmark、对比方法
- **任务与场景**：四个灵巧操作任务——单臂 Grasp（抓取）、Pour（倒水）；双臂 Lift（抬升）、Handover（交接）。仿真环境采用 OmniGibson，包含80个不同物体、12种环境变化（光照、桌面纹理）。
- **Benchmark**：
  - **数据多样性**：记录每轮迭代中物体数 \(O\)、环境数 \(E\)、位姿数 \(P\) 及总场景配置数。
  - **策略泛化性能**：多因子泛化测试集 \(T_{OEP}\)（40个未见过的物体-环境-位姿组合）；物体泛化测试集 \(T_O(i)\)（固定场景下不同物体）。
- **对比方法**：
  - Human Demo（Default/Enhanced）：20条人类演示（固定/多样化场景）。
  - DexMimicGen（Default/Enhanced）：基于重放和编辑的数据生成方法（Default用1条演示；Enhanced用10条演示）。
  - 消融变体：w/o Res（去除残差策略）、w/o AEP（去除增强模块）、w/o Res + w/o AEP（仅基策略）。
- **评价指标**：成功率（Success Rate, SR），均为5次独立运行的平均值±标准差。

#### 4. 资源与算力
- **基策略训练**：使用8块 NVIDIA A100 GPU。
- **残差策略训练**：使用单块 NVIDIA RTX 4090 GPU。
- **总训练时间**：约30小时（3次迭代：首次仅IL，后两次各含IL+RL）。
- **数据生成时间**：每轨迹15秒，500条成功轨迹约2.4小时（对比人类遥操作12.5小时，DexMimicGen 4.4小时）。

#### 5. 实验数量与充分性
- **实验数量**：
  - 4个任务各进行3次迭代，生成从20到500条轨迹的递增数据集。
  - 与4个基线对比（含2个Human Demo和2个DexMimicGen变体）。
  - 消融实验包括3个变体，覆盖各模块贡献。
  - 真实世界部署：双臂Lift和Handover任务各20条轨迹，3次重复试验。
- **充分性与公平性**：
  - 所有方法使用相同仿真设置、模型架构和测试集，确保公平。
  - 多次独立运行报告标准差，统计严谨。
  - 消融实验明确验证了残差策略和数据增强的贡献。
  - 额外扩展迭代实验（至第5轮）验证了性能持续提升趋势。
  - 但未在其他机器人平台或更复杂任务（如可变形物体）上验证，覆盖范围有限。

#### 6. 论文的主要结论与发现
- DexFlyWheel从单条演示出发，可生成超过2000条多样化演示（覆盖20种物体、12种环境、8种位姿）。
- 随迭代进行，策略在 \(T_{OEP}\) 上的成功率从迭代1的16.5%提升至迭代3的81.9%，提升近400%。
- 残差策略在物体泛化上平均提升32.1%（\(T_O(i)\)）。
- 与基线相比：DexFlyWheel显著优于Human Demo（平均9.4%~13.4%）和DexMimicGen（31.4%~45.2%）。
- 真实世界部署：双臂Lift成功率78.3%，Handover成功率63.3%，验证了仿真到真实迁移的有效性。
- 数据生成效率高（2.4小时完成500条成功轨迹），且成功率达89.8%。

#### 7. 优点
- **方法创新**：将IL+残差RL与数据增强整合成闭环飞轮，实现自我提升，显著降低人工成本。
- **数据多样性**：通过渐进式扩展物体、环境、空间维度，生成覆盖广、质量高的数据集。
- **实验充分**：多任务、多基线、消融、真实世界验证，统计严谨。
- **可扩展性**：框架设计支持进一步迭代和增加复杂度，具有实际部署潜力。

#### 8. 不足与局限
- **依赖人工奖励设计**：残差RL需要人为设计奖励函数，可能限制在新任务上的快速适应。
- **缺乏触觉反馈**：仿真和策略均未包含触觉传感，对需要精细力控的任务（如易碎物体）鲁棒性不足。
- **假设限制**：“微小调整”观察可能不适用于需要根本性策略改变的任务（如可变形物体操作、精确装配）。
- **仿真到真实迁移**：实际部署仅测试了双臂升举和交接，其他任务的Sim2Real表现未验证；依赖数字孪生和FoundationPose，对感知精度要求高。
- **实验覆盖**：未评估在真实世界杂乱场景或与人类交互等更复杂环境下的表现。

（完）

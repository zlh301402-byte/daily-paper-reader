---
title: "SAM2Act: Integrating Visual Foundation Model with A Memory Architecture for Robotic Manipulation"
title_zh: SAM2Act：集成视觉基础模型与记忆架构的机器人操作
authors: "Haoquan Fang, Markus Grotz, Wilbert Pumacay, Yi Ru Wang, Dieter Fox, Ranjay Krishna, Jiafei Duan"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=anSWDvJm8v"
tags: ["query:drone-arm"]
score: 4.0
evidence: 使用视觉基础模型的机器人操作策略，可适用于机械臂控制
tldr: "现有机器人操作策略在泛化性和记忆任务上存在不足。本工作提出SAM2Act，利用多视图视觉基础模型和记忆架构学习操作策略。在RLBench 18个任务上平均成功率86.8%，展现出强大的泛化能力。该方法为构建通用机器人操作策略提供了可复用的范式。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-answdvjm8v/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1454, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-answdvjm8v/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1326, \"height\": 834, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-answdvjm8v/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1396, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-answdvjm8v/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1249, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-answdvjm8v/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1782, \"height\": 912, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 867, \"height\": 900, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1782, \"height\": 366, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1647, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 134, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 785, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 719, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1423, \"height\": 509, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1778, \"height\": 794, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1767, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1777, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1787, \"height\": 844, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-answdvjm8v/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1780, \"height\": 247, \"label\": \"Table\"}]"
motivation: 现有机器人操作策略难以泛化到新场景并处理记忆依赖任务。
method: 提出多视图机器人transformer策略，利用SAM2视觉基础模型和多分辨率上采样，结合记忆架构。
result: "在RLBench基准18个任务上平均成功率86.8%，显著超越基线。"
conclusion: 集成视觉基础模型与记忆机制是提升机器人操作泛化性和任务完成能力的有效途径。
---

## Abstract
Robotic manipulation systems operating in diverse, dynamic environments must exhibit three critical abilities: multitask interaction, generalization to unseen scenarios, and spatial memory. While significant progress has been made in robotic manipulation, existing approaches often fall short in generalization to complex environmental variations and addressing memory-dependent tasks. To bridge this gap, we introduce **SAM2Act**, a multi-view robotic transformer-based policy that leverages multi-resolution upsampling with visual representations from large-scale foundation model. SAM2Act achieves a state-of-the-art average success rate of **86.8% across 18 tasks** in the RLBench benchmark, and demonstrates robust generalization on *The Colosseum* benchmark, with only a **4.3% performance gap** under diverse environmental perturbations. Building on this foundation, we propose **SAM2Act+**, a memory-based architecture inspired by SAM2, which incorporates a memory bank, an encoder, and an attention mechanism to enhance spatial memory. To address the need for evaluating memory-dependent tasks, we introduce ***MemoryBench***, a novel benchmark designed to assess spatial memory and action recall in robotic manipulation. SAM2Act+ achieves an average success rate of **94.3% on memory-based tasks** in *MemoryBench*, significantly outperforming existing approaches and pushing the boundaries of memory-based robotic systems.
Project page: [sam2act.github.io](https://sam2act.github.io/).

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
机器人操作系统需要在动态、多样的环境中具备三项关键能力：多任务交互、对未见场景的泛化、以及空间记忆。现有方法（如PerAct、RVT、RVT-2）虽然在标准基准上取得了进展，但在复杂环境变化下的泛化能力以及需要记忆的时序任务上表现不足。本文旨在通过融合大规模视觉基础模型（SAM2）与记忆架构，弥补这些短板，提出能够同时提升多任务性能、泛化鲁棒性和空间记忆能力的机器人操作策略。

## 2. 方法论：核心思想与关键技术细节
### 2.1 SAM2Act（基础版本）
- **架构**：基于RVT-2的多视图transformer粗到细（coarse-to-fine）框架，通过点云重建、虚拟相机渲染生成三视图，结合语言指令预测6-DoF动作。
- **关键改进**：
  - 使用预训练的**SAM2图像编码器**，以**LoRA（秩16）** 进行微调，提取多分辨率嵌入（三个分辨率层级）。
  - 提出**多分辨率上采样机制**：通过级联凸上采样器（convex upsampler），将SAM2多分辨率嵌入与上采样特征逐元素相加，经层归一化后逐步精化特征图，生成更精确的平移热图。
  - 公式说明（文字）：设X_l为第l层特征图，E_l为对应SAM2嵌入，上采样操作U将空间维度加倍并减半通道数，更新公式为 `X_{l+1} = LayerNorm( U(X_l) ⊕ E_l )`，其中⊕表示逐元素相加。
- **训练**：在RLBench和Colosseum上以256 batch size、cosine学习率衰减训练90 epoch。

### 2.2 SAM2Act+（记忆增强版本）
- **灵感**：借鉴SAM2的视频目标跟踪记忆机制（Memory Bank、Memory Encoder、Memory Attention）。
- **集成方式**：在SAM2Act粗分支中嵌入三个记忆组件：
  - **Memory Bank**：每个视图维护独立FIFO队列，存储最近N个记忆（投影至64维）。
  - **Memory Encoder**：将预测的平移热图（类比目标掩码）与来自MVT的未条件嵌入逐元素相加，经卷积下采样生成记忆特征。
  - **Memory Attention**：对当前观察嵌入与存储的记忆进行自注意力和交叉注意力（含2D空间RoPE），输出条件嵌入。
- **训练策略**：先预训练SAM2Act，然后冻结SAM2编码器、MVT和细分支，仅微调粗分支中的记忆组件。采用连续关键帧采样（窗口大小取决于任务），总batch size 256-320，训练12.5K步。
- **前向算法**（Algorithm 1）：对每个视图，依次获取MVT嵌入、检索记忆、经过记忆注意力、预测热图、编码新记忆、存入队列（若满则修剪）。

## 3. 实验设计
### 3.1 模拟环境
- **RLBench 18任务**：标准多任务基准，涵盖249个变体（物体放置、颜色、大小、类别等）。每任务100个训练演示，25个测试演示，4次评估取平均和标准差。
- **The Colosseum**：泛化基准，测试13种扰动（物体颜色/纹理/大小、光照、桌面纹理、背景、相机姿态、干扰物等）。在20个任务上训练，与基线对比。
- **MemoryBench**：新提出的记忆基准，包含3个任务（reopen drawer、put block back、rearrange block），故意违反马尔可夫性质以迫使策略依赖空间记忆。单任务训练和测试。

### 3.2 真实世界实验
- **Franka Panda机器人 + Robotiq 2F-85夹爪 + RealSense D455深度相机**。
- 4个任务：(a) 打开台灯 (b) 按顺序按按钮 (c) 叠方块 (d) 按同一个按钮（记忆任务）。
- 每任务10个分布内和10个分布外（含环境扰动）试验。

### 3.3 对比方法
- **基线**：PerAct、RVT、RVT-2、SAM-E、3D Diffuser Actor、3D-LOTUS、ARP+等。
- **消融**：替换SAM2为SAM/DINOv2/Depth Anything V2，移除多分辨率输入，替换为上采样原版。

## 4. 资源与算力
论文明确说明：所有模型在 **32块NVIDIA H100/A100 GPU** 上训练；有时也用16或8块但保持总batch size一致。SAM2Act训练56.25K步（90 epoch），SAM2Act+训练12.5K步（20 epoch）。每任务训练时间未具体给出。

## 5. 实验数量与充分性
- **数量**：模拟实验涵盖18个RLBench任务、Colosseum上的20个任务、MemoryBench的3个任务；真实世界4个任务。每组实验均报告多次评估的均值和标准差。
- **消融**：对SAM2Act进行了3种消融（编码器替换/上采样替换/移除多分辨率输入），对Colosseum也做了相同消融。
- **充分性**：
  - 多任务基准结果完整，与众多SOTA方法（包括非BC方法）对比，表格和排序清晰。
  - 泛化实验覆盖13种扰动，统计了平均下降百分比。
  - 记忆实验使用单任务设置隔离记忆能力，并给出了随机基线。
  - 真实世界实验规模较小（每任务10+10 trials），但涵盖了分布内/分布外测试。
- **客观性**：所有对比基于公开代码和设置，但未提供自身代码是否开源。论文声称“公平比较”但未讨论超参数调优差异。

## 6. 主要结论与发现
1. **SAM2Act在RLBench 18任务上平均成功率86.8%**，超过RVT-2（81.4%）和ARP+（84.9%）等先前最优方法，尤其在需要精度的任务（Insert Peg提升44%，Sort Shape提升29%）上表现突出。
2. **在Colosseum泛化基准上，SAM2Act平均性能仅下降4.3%**，远低于RVT-2（-19.5%）和SAM-E（-20.7%），对光照、桌面颜色、相机姿态等扰动具有鲁棒性。
3. **SAM2Act+在MemoryBench上平均94.3%**，远超无记忆的SAM2Act（55.0%）和RVT-2（54.0%），证明显式记忆建模对空间记忆任务至关重要。
4. **真实世界实验**：SAM2Act在三个任务上的分布内成功率75% vs RVT-2 43%；SAM2Act+在记忆任务上70% vs 40%（随机猜测）。
5. 消融实验表明：SAM2图像编码器、多分辨率上采样和SAM2多分辨率输入均对性能有显著贡献。

## 7. 优点
- **技术创新点清晰**：将SAM2的多分辨率嵌入和记忆机制适配到机器人操作，方法优雅有效。
- **实验全面**：覆盖标准多任务、泛化、记忆和真实世界，对比充分，消融完整。
- **提出新基准MemoryBench**：专门评估记忆能力，填补了空白。
- **泛化表现突出**：在The Colosseum上的平均下降仅4.3%，展示了强鲁棒性。
- **代码和项目页公开**（sam2act.github.io），可复现性较好。

## 8. 不足与局限
- **记忆窗口固定**：SAM2Act+使用固定的FIFO长度，对不同长度的任务需要手动调整，缺乏自适应能力。
- **未扩展到灵巧手连续控制**：论文自身承认无法处理dexterous continuous control。
- **真实世界实验规模小**：每任务仅20次试验，统计可靠性有限；且仅用一个机器人平台。
- **未讨论失败案例分析**：没有详细分析在哪些任务或扰动下仍会失败，以及失败模式。
- **训练计算开销**：使用32块GPU，资源需求较高，可能限制应用普及。
- **消融实验不够深入**：例如未探索记忆组件中不同设计选择（如注意力层数、记忆大小）的影响。

（完）

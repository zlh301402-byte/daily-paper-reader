---
title: "ForceVLA: Enhancing VLA Models with a Force-aware MoE for Contact-rich Manipulation"
title_zh: ForceVLA：通过力感知混合专家模型增强VLA模型的接触丰富操作
authors: "Jiawen Yu, Hairuo Liu, Qiaojun Yu, Jieji Ren, Ce Hao, Haitong Ding, Guangyu Huang, Guofan Huang, Yan Song, Panpan Cai, Wenqiang Zhang, Cewu Lu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=2845H8Ua5D"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 力感知视觉语言动作模型用于接触丰富操作，可应用于物理交互控制
tldr: 提出ForceVLA，将力传感作为第一类模态融入视觉语言动作模型。通过力感知混合专家模块动态整合力反馈与视觉语言嵌入，实现上下文感知路由，在接触丰富操作任务上显著提升了在视觉遮挡和动态不确定下的性能，推动了通用操作中的力感知能力。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1290, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 704, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1379, \"height\": 622, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1376, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1299, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1306, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1369, \"height\": 659, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1222, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1341, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1432, \"height\": 1059, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1431, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1430, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1429, \"height\": 765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1429, \"height\": 765, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1427, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1430, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1428, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1430, \"height\": 824, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-2845h8ua5d/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1430, \"height\": 763, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 705, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1205, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 579, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 722, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 970, \"height\": 339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-2845h8ua5d/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1134, \"height\": 263, \"label\": \"Table\"}]"
motivation: 现有视觉语言动作模型在接触丰富任务中缺乏力感知能力，难以处理视觉遮挡和动态不确定性。
method: 提出力感知混合专家融合模块，将实时六轴力反馈与预训练的视觉语言嵌入动态结合。
result: 在接触丰富操作任务上显著提升了性能和鲁棒性。
conclusion: 将力作为第一类模态引入VLA模型能有效增强接触丰富操作能力。
---

## Abstract
Vision-Language-Action (VLA) models have advanced general-purpose robotic manipulation by leveraging pretrained visual and linguistic representations. However, they struggle with contact-rich tasks that require fine-grained control involving force, especially under visual occlusion or dynamic uncertainty. To address these limitations, we propose \textbf{ForceVLA}, a novel end-to-end manipulation framework that treats external force sensing as a first-class modality within VLA systems. ForceVLA introduces \textbf{FVLMoE}, a force-aware Mixture-of-Experts fusion module that dynamically integrates pretrained visual-language embeddings with real-time 6-axis force feedback during action decoding. This enables context-aware routing across modality-specific experts, enhancing the robot's ability to adapt to subtle contact dynamics. We also introduce \textbf{ForceVLA-Data}, a new dataset comprising synchronized vision, proprioception, and force-torque signals across five contact-rich manipulation tasks. ForceVLA improves average task success by 23.2\% over strong $\pi_0$-based baselines, achieving up to 80\% success in tasks such as plug insertion. Our approach highlights the importance of multimodal integration for dexterous manipulation and sets a new benchmark for physically intelligent robotic control. Code and data will be released at https://sites.google.com/view/forcevla2025/.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题**：现有的视觉-语言-动作（VLA）模型在接触丰富的操作任务（如插拔、组装）中表现不佳，因为这些任务需要精细的力控制和动态适应性，而VLA模型仅依赖视觉和语言线索，缺乏力反馈，尤其当视觉被遮挡或存在动态不确定性时容易失败。
- **动机**：人类在操作中自然整合触觉和本体感觉，因此需要让机器人也能感知和利用接触力。论文提出将外部力传感作为第一类模态正式融入VLA系统，从而提升在接触丰富场景下的物理智能和鲁棒性。

### 2. 论文提出的方法论
- **核心思想**：基于π0框架，设计一个力感知的混合专家（Mixture-of-Experts, MoE）融合模块 **FVLMoE**，在动作解码阶段动态整合预训练的视觉-语言嵌入和实时六轴力反馈，实现上下文感知的路由与动作生成。
- **关键技术细节**：
  - **输入映射**：视觉和语言输入经预训练VLM（PaliGemma/SigLIP）处理产生视觉-语言嵌入；力传感器数据（6DOF力/力矩）经线性投影变成力token；这些token拼接后进入FVLMoE。
  - **FVLMoE结构**：
    - 拼接后的序列先经一个编码层（多头自注意力+FFN）进行共享细化。
    - 然后进入稀疏MoE层，包含4个专家（独立MLP），路由器为每个token选择top-1专家，输出经残差连接后得到融合特征。
    - 最后通过线性投影将融合特征映射到动作专家需要的维度。
  - **注入动作流头**：融合特征中提取后H_action个token，与当前状态及噪声动作轨迹相加，作为条件指导流匹配去噪过程生成动作序列。
- **算法流程**（文字说明）：  
  输入多视角图像、语言指令、本体状态、6轴力数据 → 视觉语言编码生成上下文嵌入 → 力嵌入与VL嵌入拼接 → FVLMoE编码与MoE融合 → 融合特征注入条件流匹配解码器 → 输出连续动作chunk（TCP位姿+夹爪宽度）。

### 3. 实验设计
- **数据集/场景**：自建 **ForceVLA-Data**，包含5类接触丰富任务（瓶泵、插头插入、USB插入、白板擦拭、黄瓜削皮），共244条轨迹，约14万时间步，同步记录视觉、本体和六轴力数据。数据使用Flexiv Rizon 7-DOF机械臂+Dahuan自适应夹爪+两个RealSense摄像头（外部+腕部），通过VR遥操作采集。
- **Benchmark与对比方法**：
  - 基线：π0-base（有/无力直接输入）、π0-fast（有/无力直接输入）。
  - 评估指标：任务成功率（主要），黄瓜削皮额外报告平均削皮长度和最少削皮次数。
  - 泛化测试：5种变体（不同物体几何、高度变化、视觉遮挡、不稳定插座等）。
  - 消融实验：不同融合位置（早期/晚期）、MoE vs 简单拼接、力输入掩码等。

### 4. 资源与算力
- **训练配置**：主要使用8×NVIDIA RTX 4090 GPU（24GB显存），64核CPU，251GB RAM。
- **训练时间**：多任务联合训练（2 GPU）约12小时完成30,000步；单任务训练（1 GPU）约9小时完成10,000步。使用Adam优化（β1=0.9, β2=0.95），峰值学习率2.5e-5，衰减至2.5e-6，bfloat16精度。

### 5. 实验数量与充分性
- **实验数量**：
  - 5个任务上对比4种基线（π0-base/π0-fast各有无力两种），每个任务测试20次（白板10次，黄瓜15次），共约（20*4+10+15）≈ 105次运行。
  - 泛化实验：5种设定，各测试20次，分别对比4种基线。
  - 消融实验：融合位置（3种）、MoE vs 简单拼接、力输入掩码（4个任务）。
  - 路由分析：可视化5个任务的专家利用率。
  - 多任务联合训练：对比4种基线。
- **充分性评价**：实验覆盖了多种任务类型、基线、泛化条件以及架构设计消融，设计较为全面。比较公平（使用相同基础框架π0，严格控制变量）。结果统计明确，但未报告误差棒或统计显著性检验（论文仅报告单次成功率，未注明重复次数内变异），存在一定偏差风险。

### 6. 论文的主要结论与发现
- ForceVLA在5个任务上平均成功率达60.5%，比最优基线π0-base w/o F（37.3%）提升23.2%，比π0-base w/ F（40.2%）也大幅提升。
- 在泛化测试中，ForceVLA在视觉遮挡下达到90%成功率，显著优于基线。
- 消融表明：力应在VLM编码之后引入（保留预训练表示），且MoE融合明显优于简单拼接（ForceVLA 80% vs 拼接60%）。
- 路由分析显示MoE专家在不同任务阶段有选择性激活，说明模块学习了有意义的物理交互表征。

### 7. 优点
- **方法创新**：将力作为第一类模态正式集成进VLA，设计了专用的力感知MoE融合模块，避免破坏预训练VLM的表示，同时实现动态、上下文敏感的路由。
- **数据集贡献**：提供了首个包含同步视觉、本体和6轴力的接触丰富操作数据集，并开源采集工具，降低研究门槛。
- **实验设计**：包含多种任务、泛化挑战和架构消融，验证了力融合的有效性和设计选择的重要性，结论可信。
- **实用性能**：在真实机器人上取得了明显改进，展示了物理交互中的适应性行为（如自动重试、姿态调整）。

### 8. 不足与局限
- **传感器精度**：使用估计的外部力而非高保真直接测量，极端敏感场景下可能不足。
- **平台成本**：实验基于集成力传感器的昂贵机器人平台（Flexiv Rizon），限制了可复现性和部署范围。
- **缺乏仿真**：论文有意识地采用“现实优先”方法，但未使用仿真进行大规模数据扩充，可能限制了任务泛化规模。
- **统计可靠性**：未报告多次实验的误差范围或置信区间，某些任务成功率波动较大（如USB插入仅25%），结论的稳健性有待进一步验证。
- **被试偏差**：数据由5名人类操作员通过VR遥操作采集，可能存在操作风格偏差。

（完）

---
title: "DiffusionVLA: Scaling Robot Foundation Models via Unified Diffusion and Autoregression"
title_zh: DiffusionVLA：通过统一扩散与自回归扩展机器人基础模型
authors: "Junjie Wen, Yichen Zhu, Minjie Zhu, Zhibin Tang, Jinming Li, Zhongyi Zhou, Xiaoyu Liu, Chaomin Shen, Yaxin Peng, Feifei Feng"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=VdwdU81Uzy"
tags: ["query:drone-arm"]
score: 6.0
evidence: 融合推理的扩散策略用于机器人动作生成，可应用于机械臂控制
tldr: 针对自回归视觉-语言-动作模型动作生成不精确以及纯扩散策略缺乏推理能力的局限，提出DiffusionVLA框架。该框架利用预训练视觉语言模型进行任务分解与解释，并通过推理注入模块引导扩散动作策略，实现了精准鲁棒的机器人控制。实验表明该方法在多种操作任务上表现优异，为机械臂控制提供了通用框架。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1597, \"height\": 1235, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1754, \"height\": 780, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1569, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 769, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 861, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 858, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 853, \"height\": 451, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 844, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 858, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1747, \"height\": 897, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1759, \"height\": 890, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vdwdu81uzy/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 860, \"height\": 375, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1779, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 724, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 815, \"height\": 204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1778, \"height\": 798, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 126, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 727, \"height\": 138, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 810, \"height\": 128, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 809, \"height\": 163, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 861, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 838, \"height\": 182, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vdwdu81uzy/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 894, \"height\": 561, \"label\": \"Table\"}]"
motivation: 现有机器人基础模型在动作生成精度与推理能力上存在不足。
method: 提出DiffusionVLA，将自回归推理与扩散策略结合，并引入推理注入模块。
result: 在仿真和真实机器人任务中，该方法在成功率和动作精度上均优于现有方法。
conclusion: 融合推理与扩散能有效提升机器人动作生成的质量和鲁棒性。
---

## Abstract
In this paper, we present DiffusionVLA, a novel framework that integrates autoregressive reasoning with diffusion policies to address the limitations of existing methods: while autoregressive Vision-Language-Action (VLA) models lack precise and robust action generation, diffusion-based policies inherently lack reasoning capabilities. Central to our approach is autoregressive reasoning — a task decomposition and explanation process enabled by a pre-trained VLM — to guide diffusion-based action policies. To tightly couple reasoning with action generation, we introduce a reasoning injection module that directly embeds self-generated reasoning phrases into the policy learning process. The framework is simple, flexible, and efficient, enabling seamless deployment across diverse robotic platforms.

We conduct extensive experiments using multiple real robots to validate the effectiveness of DiVLA. Our tests include a challenging factory sorting task, where DiVLA successfully categorizes objects, including those not seen during training. The reasoning injection module enhances interpretability, enabling explicit failure diagnosis by visualizing the model’s decision process. Additionally, we test DiVLA on a zero-shot bin-picking task, achieving \textbf{63.7\% accuracy on 102 previously unseen objects}. Our method demonstrates robustness to visual changes, such as distractors and new backgrounds, and easily adapts to new embodiments. Furthermore, DiVLA can follow novel instructions and retain conversational ability. Notably, DiVLA is data-efficient and fast at inference; our smallest DiVLA-2B runs 82Hz on a single A6000 GPU. Finally, we scale the model from 2B to 72B parameters, showcasing improved generalization capabilities with increased model size.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：当前机器人基础模型主要分为两类：自回归视觉-语言-动作（VLA）模型（如RT-2、OpenVLA）和扩散策略模型（如Diffusion Policy）。前者尽管具备语言推理能力，但将连续动作离散化为固定词元会破坏动作的连贯性和精度，且推理速度慢；后者在动作生成上鲁棒且多模态，但缺乏必要的推理能力。如何将两者的优势（推理能力 + 高频率鲁棒动作生成）统一到一个框架中，是本文的核心问题。
- **整体含义**：本文提出的DiffusionVLA（DiVLA）旨在构建一个既能“思考”又能“行动”的端到端机器人策略，通过自回归推理指导扩散动作生成，实现精确、可解释且通用的机器人控制，为机器人基础模型提供新的规模化范式。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将自回归语言模型（用于推理）与扩散模型（用于动作生成）融合，并通过“推理注入模块”将自生成的推理短语直接嵌入到动作策略学习中，从而紧密耦合推理与动作生成。
- **关键技术细节**：
  - **整体架构**：基于预训练视觉语言模型（VLM，采用Qwen2-VL系列，2B/8B/72B）作为骨干，视觉编码器使用SigLIP。多视角图像通过共享编码器后拼接视觉词元，VLM输出文本推理词元。
  - **动作生成**：在VLM最后一层之后，生成固定数量的动作词元，通过两层MLP投影模块映射到扩散模型（标准Diffusion Policy架构）的输入维度。扩散模型输出通过一个MLP层预测机器人关节空间。
  - **推理注入模块**：将VLM推理阶段的最终嵌入，通过特征线性调制（FiLM）直接注入到策略网络的各层中，实现推理信号对动作生成的条件化，无需递归式输入。这不仅提高效率，还增强了策略的可解释性。
  - **训练目标**：总损失为扩散损失与下一词元预测损失的加权和：\( L = L_{\text{diff}} + \alpha L_{\text{ntp}} \)，其中 \(\alpha=10\) 以平衡量级。预训练阶段使用Droid数据集（2B/7B）或Droid+OXE（72B），并利用GPT-4o自动为数据添加推理标注。微调阶段使用LoRA对VLM进行低秩适应，其他部分冻结。
  - **多本体适应**：通过为新本体初始化一个新的MLP层，无需复制整个动作解码器，实现快速迁移。

### 3. 实验设计：数据集/场景、基准方法

- **数据集与场景**：
  - **预训练**：Droid数据集（约97万条轨迹），OXE数据集（用于72B模型）。
  - **微调与评估**：在真实机器人上设置四类任务：工厂分拣（Franka，500条轨迹）、多任务学习（Franka，580条轨迹，包含5个任务）、零样本拣选（Franka，无训练数据，102个未见物体）、餐桌清理（双臂AgileX机器人，400条轨迹，包含已见和未见物体）。此外还包括视觉泛化测试（干扰物、背景变化、彩色光照）和视角泛化测试。
- **基准方法**：对比Diffusion Policy（DP）、TinyVLA、Octo、OpenVLA（均为7B级别，Octo和OpenVLA使用OXE预训练，数据量是DiVLA的25倍）。对于框架公平性，将OpenVLA扩展为三视角输入。
- **评估指标**：成功率（多次试次平均值），对于分拣任务还细分为已见/未见/杂乱等子场景。

### 4. 资源与算力

- **算力信息**：论文在正文中未明确说明训练所使用的GPU型号、数量和训练时长。仅在推理部分提到：使用单张**NVIDIA A6000 GPU**，DiVLA-2B达到**82Hz**，DiVLA-7B达到**42Hz**（利用vLLM框架加速）。预训练和微调阶段的具体硬件开销未披露。这是一个不足，但符合很多机器人论文的惯例。

### 5. 实验数量与充分性

- **实验数量**：论文进行了大量真实机器人实验，涵盖：
  - 多任务学习（5个任务 × 2种设置：分布内和视觉泛化，共约77+45=122次试次）
  - 工厂分拣（4种场景：已见/混合/杂乱已见/杂乱混合，共80+80+65+65=290次试次）
  - 零样本拣选（102个未见物体，每个方法一次试次？但文中报告成功率，应含多次试次，具体试次数未说明）
  - 双臂餐桌清理（已见/混合，各48次试次）
  - 视角泛化（各5次试次）
  - 新指令跟随（少量试次）
  - 消融实验（推理注入模块、多视角对比、模型规模2B/7B/72B）
  - VQA能力示例
- **充分性与公平性**：
  - 实验设计较为全面，覆盖了分布内、分布外（视觉变化、未见物体、新本体、新指令）多种挑战，且对比了多类主流方法，控制了预训练数据量差异（DiVLA预训练数据远小于Octo/OpenVLA）。
  - 但部分实验试次数较少（例如视角泛化仅5次，新指令跟随仅3次），统计显著性不足。另外，未与同为扩散+推理的π0（2024）在实验中直接对比，只在相关工作中提及。
  - 消融实验仅针对推理注入模块，缺少对投影层设计、FiLM替代方案、扩散模型结构等的消融。整体上实验强度合理，但仍有提升空间。

### 6. 论文的主要结论与发现

- **核心结论**：融合自回归推理与扩散策略可以有效提升机器人动作生成的精度、鲁棒性和泛化能力。推理注入模块是关键，不仅提高了性能（全任务平均成功率高出第二名OpenVLA约20.9%），还带来了可解释性。
- **关键发现**：
  - DiVLA在零样本拣选（63.7% vs 28.4%）、工厂分拣（66.2% vs 45.3%）、双臂餐桌清理（72.9% vs 45.8%）等任务上显著优于现有方法。
  - 推理能力使模型能对未见物体进行类比（如将螺丝刀归类为六角扳手），并能动态调整动作（如抓取中途更换目标时的推理重定向）。
  - 模型具有良好的规模扩展性：从2B增至72B，工厂分拣成功率从66.2%提升至82.4%，零样本拣选从63.7%提升至75.9%。
  - 推理模块提供了可解释性，可进行故障分析和行为理解。
  - 推理速度极快，DiVLA-2B达82Hz，为实时控制提供可能。

### 7. 优点：方法或实验设计上的亮点

- **方法论优点**：
  - 巧妙地将自回归推理与扩散动作生成融合，并在策略学习阶段直接注入推理信号（FiLM），无需额外推理步骤，是高效且简洁的设计。
  - 采用LoRA微调VLM，冻结大部分参数，训练高效，数据需求量小（仅需500-580条轨迹微调即可达到优异效果）。
  - 具有本体可迁移性：为新机器人只需新增一个MLP层，快速适应，体现了模型的灵活性。
  - 提出“推理注入模块”，不仅提升泛化能力，还赋予模型可解释性，有利于故障分析。
- **实验设计优点**：
  - 在真实机器人上进行细粒度的多场景评估（已见/未见、杂乱、视觉变化、视角变化、新指令、VQA等），验证了模型在实际部署中的鲁棒性。
  - 对比了多种主流基线，并公平处理了多视角输入问题（为OpenVLA也扩展为三视角）。
  - 展示了模型扩展性（2B→72B），符合缩放定律。

### 8. 不足与局限

- **实验覆盖的局限**：
  - 多数实验在单一机器人平台（Franka和AgileX双臂）上完成，未在更多本体（如轮式、四足）上验证，泛化性结论需谨慎。
  - 部分场景试次过少（如视角泛化仅5次），缺乏统计学意义。
  - 零样本拣选任务中，虽然成功率高出基线很多，但绝对数值仍只有63.7%，存在大量失败场景未被分析。
  - 未与最新的扩散+推理模型π0进行直接对比，仅在相关工作中提及。
- **方法与设计局限**：
  - 推理注入模块依赖于预训练VLM的推理能力，对于简单任务可能引入额外计算，且推理质量可能影响动作生成。
  - 训练目标中两损失权重的选择（\(\alpha=10\)）仅基于经验观察，未进行系统调参。
  - 模型对低比特量化敏感（文中提到8bit/4bit推理性能下降），不利于边缘部署。
- **资源与可重复性**：
  - 训练算力未公开，复现成本较高；虽然开源了部分数据（网站链接），但完整的训练代码和预训练权重是否完全开放尚不明确（文中提及开源网站但未提供具体仓库）。
- **其他**：论文未讨论失败案例的详细分析，所述“推理可解释性”仅给出定性例子，缺乏定量评估。

（完）

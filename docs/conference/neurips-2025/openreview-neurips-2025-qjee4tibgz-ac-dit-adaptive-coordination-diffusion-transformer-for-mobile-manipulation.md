---
title: "AC-DiT: Adaptive Coordination Diffusion Transformer for Mobile Manipulation"
title_zh: AC-DiT：用于移动操控的自适应协调扩散Transformer
authors: "Sixiang Chen, Jiaming Liu, Siyuan Qian, Han Jiang, Zhuoyang Liu, Chenyang Gu, Xiaoqi Li, Chengkai Hou, Pengwei Wang, Zhongyuan Wang, Renrui Zhang, Shanghang Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=qjee4tiBGZ"
tags: ["query:aerial-arm"]
score: 6.0
evidence: 移动操控中基座与机械臂的自适应协调，与空中机械臂协调问题类似
tldr: 移动操控面临基座与机械臂协调难题，现有方法未显式建模基座对机械臂的影响，且忽视不同阶段的多模态感知需求。本文提出自适应协调扩散Transformer（AC-DiT），通过扩散模型显式协调两者，并在不同阶段自适应切换视觉模态。实验验证了该方法在多种移动操控任务中的有效性，提升了长距离操控精度。该工作为移动机器人协调控制提供了新框架。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1436, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 1062, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 802, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1346, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 873, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1307, \"height\": 1260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1347, \"height\": 1035, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1450, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjee4tibgz/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1152, \"height\": 1305, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 184, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 901, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 452, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 424, \"height\": 399, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 620, \"height\": 143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 514, \"height\": 143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjee4tibgz/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1344, \"height\": 804, \"label\": \"Table\"}]"
motivation: 现有移动操控方法忽略了基座对机械臂的影响，且未分阶段利用不同视觉模态。
method: 提出自适应协调扩散Transformer，显式建模基座影响并自适应切换视觉观测模态。
result: 在移动操控任务中提升了协调性和操控精度。
conclusion: AC-DiT为移动基座与机械臂的协调控制提供了有效方案。
---

## Abstract
Recently, mobile manipulation has attracted increasing attention for enabling language-conditioned robotic control in household tasks.
However, existing methods still face challenges in coordinating mobile base and manipulator, primarily due to two limitations.
On the one hand, they fail to explicitly model the influence of the mobile base on manipulator control, which easily leads to error accumulation under high degrees of freedom.
On the other hand, they treat the entire mobile manipulation process with the same visual observation modality (e.g., either all 2D or all 3D), overlooking the distinct multimodal perception requirements at different stages during mobile manipulation.
To address this, we propose the Adaptive Coordination Diffusion Transformer (AC-DiT), which enhances mobile base and manipulator coordination for end-to-end mobile manipulation.
First, since the motion of the mobile base directly influences the manipulator's actions, we introduce a mobility-to-body conditioning mechanism that guides the model to first extract base motion representations, which are then used as context prior for predicting whole-body actions. 
This enables whole-body control that accounts for the potential impact of the mobile base’s motion.
Second, to meet the perception requirements at different stages of mobile manipulation, we design a perception-aware multimodal conditioning strategy that dynamically adjusts the fusion weights between various 2D visual images and 3D point clouds, yielding visual features tailored to the current perceptual needs.
This allows the model to, for example, adaptively rely more on 2D inputs when semantic information is crucial for action prediction, while placing greater emphasis on 3D geometric information when precise spatial understanding is required.
We empirically validate AC-DiT through extensive experiments on both simulated and real-world mobile manipulation tasks, demonstrating superior performance compared to existing methods.

---

## 论文详细总结（自动生成）

# 论文总结：AC-DiT: Adaptive Coordination Diffusion Transformer for Mobile Manipulation

## 1. 核心问题与研究动机

移动操控（mobile manipulation）需要机器人同时协调移动基座（mobile base）与机械臂（manipulator）完成复杂家庭任务。现有方法主要存在两个关键局限性：

- **缺乏显式协调建模**：基座运动直接影响机械臂控制，但现有方法未显式建模这种影响，导致高自由度下误差累积严重。
- **单一视觉模态不足**：整个移动操控过程使用相同的视觉观测模态（全2D或全3D），忽略了不同阶段对多模态感知的不同需求。例如，定位阶段需要语义丰富的2D图像，交互阶段需要几何精确的3D点云。

因此，论文提出**自适应协调扩散Transformer（AC-DiT）**，旨在通过端到端方式增强基座与机械臂的协调，并自适应满足不同阶段的感知需求。

## 2. 方法论

### 核心思想
AC-DiT基于扩散Transformer（DiT）架构，引入两个核心机制：
- **移动体到身体的条件机制（Mobility-to-Body Conditioning）**：先提取基座运动潜在特征作为先验，再用于预测全身动作。
- **感知感知多模态自适应机制（Perception-aware Multimodal Adaptation）**：动态调整2D图像与3D点云的融合权重，生成感知适应的视觉特征。

### 关键技术细节
- **整体架构**：使用SigLIP作为图像、点云和文本的编码器（图像编码器冻结，3D编码器加LoRA微调）。点云处理采用Lift3D策略，将点云转换为与2D基础模型兼容的token序列。
- **Mobility-to-Body Conditioning**：先预训练轻量级移动动作头（DiT块+MLP，约170M参数）预测基座动作，提取其最后一个DiT块的输出token作为潜在移动特征。该特征与多模态特征拼接后，通过交叉注意力注入到移动操控动作头（约1.2B参数）中，用于预测全身动作。
- **Perception-aware Multimodal Adaptation**：将2D特征（三个视角）、3D特征和语言特征通过MLP投影到共享空间，计算每个视觉模态与语言特征的余弦相似度，归一化后作为权重，对原始特征进行加权，得到感知适应的视觉特征。
- **训练目标**：预训练阶段仅优化3D编码器的LoRA和轻量移动头，使用去噪MSE损失；全模型训练阶段优化除预训练SigLIP外的所有可训练模块。

### 算法流程（文字说明）
1. 输入：历史观测（多视角2D图像、3D点云、机器人状态）和语言指令。
2. 特征提取：图像编码器提取2D特征，3D编码器提取3D特征，文本编码器提取语言特征。
3. 预训练阶段：轻量移动头预测基座动作，提取潜在移动特征。
4. 全模型阶段：将潜在移动特征、语言特征和感知加权后的视觉特征输入移动操控动作头，通过DiT块和交叉注意力预测基座和机械臂的联合动作序列。

## 3. 实验设计

### 仿真实验
- **数据集/场景**：
  - **Maniskill-Hab（MSHab）**：基于Sapien模拟器，包含ReplicaCAD场景和YCB物体，7个任务：pick_apple、place_apple、pick_bowl、place_bowl、open_fridge、open_kitchen_counter、close_kitchen_counter。使用RL代理（PPO和SAC）收集1000个成功轨迹。
  - **RoboTwin**：双机械臂仿真，6个任务：block_handover、container_place、dual_bottles_pick_easy、dual_bottles_pick_hard、empty_cup_place、pick_apple_messy。使用GPT-4生成关键姿态，自动生成1000个轨迹。
- **对比方法**：ACT、Diffusion Policy (DP)、3D Diffusion Policy (3DP)、Robotics Diffusion Transformer (RDT)、EquiBot、π0。所有方法使用相同的观测和动作空间。
- **评价指标**：每个任务100个episode，重复3次，计算平均成功率及其标准差。

### 真实世界实验
- **平台**：Agilex Cobot Magic（四个Piper机械臂 + Tracer移动基座），配备三台Orbbec Dabai相机和一台RealSense L515深度相机。
- **任务**：4个长周期任务：Cucumber in Basket、Store Breads、Hang Towel、Clean Table，每个任务包含至少4个子任务。每任务收集100条轨迹。
- **模型训练**：单个模型训练所有任务，评估17次（不同初始物体位置）。
- **对比方法**：ACT和π0。

### 消融实验
在MSHab上评估不同组件贡献：仅2D输入、2D+3D、2D+3D+移动-身体条件、完整模型（+感知多模态自适应）。

## 4. 资源与算力

- **GPU**：8块NVIDIA A100（80GB）。
- **训练阶段**：
  - 预训练（Stage 1）：20,000迭代。
  - 全模型训练（Stage 2）：30,000迭代。
- **模型参数量**：轻量移动头170M，完整AC-DiT 1.2B，总计可训练参数约1.37B，总模型约2.7B（含冻结基础模型）。
- **显存**：训练时batch size为16，使用约60GB GPU内存；推理时约20GB。
- **推理速度**：5Hz（单张RTX 4090），结合动作分块，机器人控制频率30Hz（单步总处理时间0.2s，其中模型推理0.16s）。

## 5. 实验数量与充分性

- **仿真实验**：7个MSHab任务 + 6个RoboTwin任务，共13个任务，每个任务3次重复，对比6种基线方法。
- **真实实验**：4个长周期任务，每个任务17次试验，对比2种基线。
- **消融实验**：4组（逐步添加组件），在MSHab上报告平均成功率。
- **额外消融**：探究条件注入方式（交叉注意力 vs 交替注入）和条件关系建立方式（移动特征 vs 机械臂特征）。
- **评估**：实验覆盖了不同任务类型（拾取、放置、开门、双机械臂协作等），包括仿真和真实场景。基线方法均使用相同观测/动作空间，确保公平。但真实实验仅2种基线，仿真基线丰富。

整体实验较充分，但真实世界基线较少，且消融仅在单一仿真环境中进行。

## 6. 主要结论与发现

- AC-DiT在所有仿真任务（MSHab平均55.6% vs 次优RDT 42.9%）和所有真实任务（各子任务成功率显著领先ACT和π0）中均取得最佳性能。
- Mobility-to-Body Conditioning机制显著提升协调性，减少误差累积（消融实验+9.5%增益）。
- Perception-aware Multimodal Adaptation机制自适应调整模态权重，提升感知适应性（+11.5%总增益）。
- 在双机械臂任务（RoboTwin）中，将Mobility-to-Body机制适配为双机械臂条件机制，同样取得最优结果，证明了方法的可扩展性。
- 可视化表明，模型在抓取阶段增加3D点云和腕部相机权重，在移动阶段增加外部相机权重，验证了自适应机制的有效性。

## 7. 优点

- **创新性**：首次在端到端移动操控中显式建模基座对机械臂的影响，并提出动态多模态感知融合。
- **完备性**：在仿真和真实世界多种任务上验证，包括单臂和双臂场景。
- **可扩展性**：方法可推广至双机械臂任务。
- **可解释性**：通过可视化自适应权重变化，展示了模型在不同阶段如何权衡模态。
- **性能提升**：在多个任务上显著超越现有SOTA方法（如MSHab平均55.6% vs 次优42.9%）。

## 8. 不足与局限

- **依赖模仿学习**：性能受数据数量和质量影响，可能继承次优或有偏的演示。
- **真实实验基线较少**：仅对比ACT和π0，缺乏更多SOTA方法（如RDT、3DP）的真实场景比较。
- **消融实验仅在单一仿真环境**：未在RoboTwin或真实场景中进一步验证各组件贡献。
- **计算开销**：1.2B参数量级，训练需8卡A100，推理需RTX 4090，部署成本较高。
- **失败模式**：包括双机械臂协调错误、运动控制累计误差、因运动终止不佳导致操控失败等，表明在复杂动态环境中鲁棒性仍有提升空间。
- **未讨论泛化性**：未测试未见过的物体或场景，语言指令变化等。
- **代码未开源**：论文声明接受后释放，目前无法复现。

（完）

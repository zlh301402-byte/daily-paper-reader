---
title: "ReinboT: Amplifying Robot Visual-Language Manipulation with Reinforcement Learning"
title_zh: ReinboT：利用强化学习增强机器人视觉语言操作
authors: "Hongyin Zhang, Zifeng Zhuang, Han Zhao, Pengxiang Ding, Hongchao Lu, Donglin Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Mzz4BhdIFb"
tags: ["query:drone-arm"]
score: 8.0
evidence: 强化学习增强的机器人视觉语言操作
tldr: 本文针对机器人操作中模仿学习数据质量不一的问题，提出ReinboT模型，将离线强化学习原理融入视觉-语言-动作模型，通过预测密集回报来理解数据质量分布，生成更鲁棒的操作决策，在多个基准任务上显著提升成功率。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1413, \"height\": 644, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 804, \"height\": 778, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 882, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1421, \"height\": 238, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 575, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 828, \"height\": 560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 869, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1244, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1614, \"height\": 1120, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1249, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1613, \"height\": 1121, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1249, \"height\": 416, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1611, \"height\": 1116, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1249, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1609, \"height\": 1114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-mzz4bhdifb/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1577, \"height\": 952, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-mzz4bhdifb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1237, \"height\": 631, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzz4bhdifb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1210, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzz4bhdifb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1234, \"height\": 561, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-mzz4bhdifb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1270, \"height\": 561, \"label\": \"Table\"}]"
motivation: 视觉-语言-动作模型受限于训练数据质量，而离线RL可从混合质量数据学习鲁棒策略。
method: 提出端到端VLA模型ReinboT，融入RL的累积奖励最大化原则，预测密集回报。
result: "在机器人操作任务上，ReinboT比基线方法成功率提升超过20%。"
conclusion: RL与VLA结合可有效处理数据质量差异，提升机器人操作性能。
---

## Abstract
Vision-Language-Action (VLA) models have shown great potential in general robotic decision-making tasks via imitation learning. However, the variable quality of training data often constrains the performance of these models. On the other hand, offline Reinforcement Learning (RL) excels at learning robust policy models from mixed-quality data. In this paper, we introduce Reinforced robot GPT (ReinboT), a novel end-to-end VLA model that integrates the RL principle of maximizing cumulative reward. ReinboT achieves a deeper understanding of the data quality distribution by predicting dense returns that capture the nuances of manipulation tasks. The dense return prediction capability enables the robot to generate more robust decision-making actions, oriented towards maximizing future benefits. Extensive experiments show that ReinboT achieves state-of-the-art performance on the CALVIN mixed-quality dataset and exhibits superior few-shot learning and out-of-distribution generalization capabilities in real-world tasks.

---

## 论文详细总结（自动生成）

# ReinboT: Amplifying Robot Visual-Language Manipulation with Reinforcement Learning — 中文总结

## 1. 核心问题与研究动机

- **背景**：视觉-语言-动作（VLA）模型通过模仿学习在通用机器人决策中展现了巨大潜力，但训练数据质量参差不齐（即使全部来自成功演示数据，质量分布也不均匀），限制了模型性能。
- **问题**：现有模仿学习范式难以区分数据质量差异并充分利用混合质量数据；离线强化学习（RL）擅长从混合质量数据中学习鲁棒策略，但如何将RL的累积奖励最大化原则有效内化到VLA模型中，特别是设计通用的密集奖励函数以及实现端到端的最大化回报预测，尚未得到充分探索。
- **目标**：提出一种新的端到端VLA模型——ReinboT，将RL的回报最大化原理与VLA结合，通过预测动态密集回报来捕捉操作任务的细微差别，从而提高机器人长时程操作任务的鲁棒性和泛化能力。

## 2. 方法论：核心思想与技术细节

### 2.1 核心思想
- 将**ReturnToGo（RTG）** 视为一种新的模态数据，在Transformer框架中联合建模语言指令、图像状态、本体感受、动作和RTG。
- 利用**预期回归（expectile regression）** 预测在当前条件和历史信息下可实现的最大回报，从而引导生成更优的动作。
- 采用**密集奖励设计**，将长时程任务分解为多个子目标，并基于子目标达成、任务进度、行为平滑度、任务完成度四个维度构造通用密集奖励。

### 2.2 关键技术细节

#### 奖励密集化方法
- 首先通过启发式方法（关节速度接近零、夹爪状态变化）将长时程演示轨迹分割成包含单一子目标的片段。
- 定义四个奖励分量：
  - **子目标达成 r1**：基于MSE、SSIM、ORB特征匹配衡量当前状态与子目标状态的相似度。
  - **任务进度 r2**：反映当前所在子目标序列与最终目标的距离。
  - **行为平滑度 r3**：惩罚关节速度/加速度过大以及动作突变。
  - **任务完成 r4**：轨迹成功指示符。
- 总密集奖励：\( r = \sum w_i r_i \)，其中权重 \( w_i \) 确保各分量量级可比。

#### 网络架构
- 使用**GPT风格Transformer**作为主干网络，集成CLIP（语言编码）、ViT+Perceiver Resampler（图像编码）、MLP（本体感受编码）。
- 引入三个预测Token Embedding：**[RTG]**、**[ACTION]**、**[IMAGE]**，分别用于预测最大ReturnToGo、机器臂动作（平滑L1损失）、夹爪动作（交叉熵损失）和未来图像（像素级MSE）。
- **模块化设计**：
  1. 主干网络提取RTG特征 \( h^{RTG} \) 和动作特征 \( h^{action} \)。
  2. RTG解码器 \( P_\phi \) 输出隐藏特征 \( \hat{g}^{hidden} \)。
  3. 将 \( \hat{g}^{hidden} \) 与 \( h^{action} \) 拼接，输入动作解码器 \( P_\omega \) 预测动作。
- 训练损失：\( \mathcal{L} = \lambda \mathcal{L}_{RTG} + \mathcal{L}_{arm} + 0.01 \mathcal{L}_{gripper} + 0.1 \mathcal{L}_{image} \)，其中 \( \mathcal{L}_{RTG} \) 采用预期回归损失。

#### 推理流程
- 不需要手动指定初始ReturnToGo值，也不需要环境提供即时奖励。
- 单次模型推理即可获得动作，相比Reinformer更高效。

### 2.3 算法/方法优势
- 通过返回最大化，模型能区分数据质量，倾向于选择未来收益更高的动作。
- 避免引入额外的Q函数或RL特定损失函数，降低Transformer学习难度。

## 3. 实验设计

### 3.1 数据集与场景

#### 模拟实验：CALVIN混合质量数据集
- 基于CALVIN benchmark，构建混合质量数据集：
  - **少量带语言标注数据**：约50条轨迹/任务。
  - **大量无语言指令的自主数据**：
    - 原始CALVIN ABC数据（人工遥操作，>20,000条轨迹）。
    - 失败数据（RoboFlamingo策略与环境交互生成，>10,000条轨迹），并添加不同程度的高斯噪声（0.05, 0.1, 0.15）以增加多样性。
- 训练方式：先在混合质量数据上训练，再用少量带标注数据微调，最后在CALVIN D环境上测试泛化性能。

#### 真实世界任务：UR5机械臂
- 任务是杯子、碗、毛绒玩具的抓取和放置。
- 收集约530条成功轨迹。
- **少样本学习评估**：三个任务（每种30条成功轨迹）微调。
- **分布外泛化评估**：未见指令、背景、干扰物、操作对象四种场景。

### 3.2 对比方法
- **模仿学习类**：RoboFlamingo、GR-1、PIDM（仅在带标注数据上训练）、GR-MG（层次化模仿学习）。
- **离线RL类**：RWR（Reward-Weighted Regression），使用不同奖励设计方案（稀疏、子目标稀疏、密集单维标量）。
- 奖励设计变体：Sparse、Sub-goal sparse、Dense single（一维标量回报）、Dense full（向量回报包含各分量）。

### 3.3 评估指标
- 链式指令的成功率（1到5条指令）及平均完成任务长度（AL）。

## 4. 资源与算力

- 论文未明确说明GPU型号、数量及训练时长。
- 附录中给出了训练超参数（batch size=32, learning rate=0.001, epochs=50等）和网络结构参数（GPT2架构，12层，12注意力头等），但缺乏硬件细节。

## 5. 实验数量与充分性

- **主要实验**：在CALVIN混合质量数据集上进行了完整的泛化性能对比（不同奖励设计、不同基线）。
- **消融实验**：
  - 奖励分量消融（缺失ReturnToGo模态，缺失各奖励分量r1/r2/r3/r4）。
  - 超参数λ（ReturnToGo损失权重）和m（预期回归参数）的影响。
  - 回报分布与最大化回报预测特性分析（图3）。
- **真实世界实验**：少样本学习（3个任务）和OOD泛化（4个场景）的定量和定性对比。
- **总体评价**：实验较为充分，覆盖了模拟和真实场景，对比了多个代表性方法，并进行了详细的消融分析。但仅使用单一模拟基准（CALVIN）和有限真实任务，可能缺乏跨数据集或更复杂任务的验证。

## 6. 主要结论与发现

1. **ReinboT在混合质量数据上显著优于所有基线**：在CALVIN D测试中，平均完成任务长度（AL）达到2.26，比最好的模仿学习基线PIDM（AL=1.73）和离线RL基线RWR（Dense single, AL=1.82）提升至少24%。
2. **密集奖励和全组件回报预测是性能的关键**：使用完整的密集四分量回报（Dense full）相比稀疏奖励或仅用单维标量回报大幅提升性能；缺失任意奖励分量都会导致性能下降（最严重的是任务进度r2缺失下降20.8%）。
3. **返回最大化必须适度**：预期回归参数m=0.9时最优；m过大（0.99）会导致过于乐观的高估，反而降低性能。
4. **真实世界场景下**：ReinboT在少样本学习和OOD泛化上均优于GR-1和RWR，表明其能有效利用成功的混合质量数据（即使全部成功，其回报分布也不均匀）。

## 7. 优点

- **方法创新**：将离线RL中最大回报预测思想有机融入VLA端到端架构，无需显式Q函数，避免Transformer在RL训练中的不稳定性。
- **奖励设计通用性强**：提出的子目标分解与四维奖励（子目标达成、进度、平滑、完成）适用于多种操作任务，且计算高效。
- **实验设计全面**：既包含标准模拟基准（CALVIN混合质量），又包含真实机器人场景的少样本和OOD测试；对比基线涵盖模仿学习和离线RL主流方法，消融实验细致。
- **推理高效**：单次前向即可完成动作预测，无需手动设置初始ReturnToGo和环境奖励，便于实际部署。
- **开源透明**：在OpenReview公开论文，包含详细附录（可视化子目标划分、奖励分布、超参数配置等）。

## 8. 不足与局限

- **奖励设计依赖手动子目标划分**：基于关节速度接近零和夹爪状态变化的启发式方法可能不适用于所有任务（如连续动作、无夹爪的飞行器操作），且忽略子目标之间的动态关系。
- **实验覆盖有限**：
  - 仅使用了CALVIN一个模拟基准，缺乏其他复杂操作任务（如开门、拾取放置等）的验证。
  - 真实世界任务只有三种物体，且场景相对简单，未见复杂遮挡、动态环境等挑战。
- **算力资源未报告**：难以评估方法和训练的可复现性及资源成本。
- **超参数敏感**：预期回归参数m和损失权重λ需要手动调优，对非专业用户不友好。
- **未与其他带RL的VLA模型（如Q-Transformer、PARL）直接对比**：论文中未包含这些近期工作，可能削弱对比的公平性。
- **仅支持单机器人臂**：未涉及双机械臂协作或多机器人协同任务。

（完）

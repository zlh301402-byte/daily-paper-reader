---
title: "Video-Enhanced Offline Reinforcement Learning: A Model-Based Approach"
title_zh: 视频增强的离线强化学习：一种基于模型的方法
authors: "Minting Pan, Yitao Zheng, Jiajian Li, Yunbo Wang, Xiaokang Yang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=uDTyhcOd9l"
tags: ["query:drone-arm"]
score: 8.0
evidence: 使用视频世界模型的离线强化学习用于机器人操作
tldr: "本文针对离线强化学习在机器人操作中价值估计不准确的问题，提出VeoRL方法，从大量无标签视频数据构建交互式世界模型，通过基于模型的指导将自然视频中的物理动态常识迁移到目标领域，在多个视觉控制任务上实现超过100%的性能提升。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
motivation: 离线RL缺乏环境交互导致次优行为和值估计偏差，而大量无标签视频包含丰富的动态信息。
method: 提出VeoRL，利用在线视频构建世界模型，通过模型指导将动态知识迁移到离线RL智能体。
result: "在机器人操作视觉控制任务上，VeoRL性能提升超过100%。"
conclusion: 视频数据可有效弥补离线RL的环境交互缺失，提升机器人学习效率。
---

## Abstract
Offline reinforcement learning (RL) enables policy optimization using static datasets, avoiding the risks and costs of extensive real-world exploration. However, it struggles with suboptimal offline behaviors and inaccurate value estimation due to the lack of environmental interaction. We present Video-Enhanced Offline RL (VeoRL), a model-based method that constructs an interactive world model from diverse, unlabeled video data readily available online. Leveraging model-based behavior guidance, our approach transfers commonsense knowledge of control policy and physical dynamics from natural videos to the RL agent within the target domain. VeoRL achieves substantial performance gains (over 100% in some cases) across visual control tasks in robotic manipulation, autonomous driving, and open-world video games. Project page: https://panmt.github.io/VeoRL.github.io.

---

## 论文详细总结（自动生成）

# 视频增强的离线强化学习：一种基于模型的方法（VeoRL）详细中文总结

## 1. 论文的核心问题与整体含义

- **研究动机**：离线强化学习（Offline RL）仅依赖静态数据集进行策略学习，避免了真实环境探索的高成本和风险，但面临两大挑战：一是数据集中行为次优（suboptimal），二是缺乏环境交互导致价值估计不准确（overestimation bias）。  
- **核心思想**：借鉴人类学习方式——先观看教学视频获得抽象理解，再动手实践。VeoRL 利用大量易获取的无标签在线视频（如 YouTube、BridgeData、NuScenes、Minecraft 玩家视频）来增强离线 RL 智能体的常识知识和物理动态理解，从而提升策略学习效果。  
- **整体含义**：将视频数据作为“行为先验”引入模型，弥补离线数据集的不完整性，显著提高在机器人操作、自动驾驶、开放世界游戏等视觉控制任务上的性能（部分任务提升超过 100%）。

## 2. 论文提出的方法论

### 核心思想
VeoRL 是一种基于模型的离线 RL 方法，通过构建“双流世界模型”整合来自视频的潜在行为抽象与来自离线数据集的真实动作，从而引导策略优化。

### 关键技术细节

1. **潜在行为抽象（Latent Behavior Abstraction）**  
   - 使用行为抽象网络（BAN）从连续帧中提取离散潜在行为。  
   - 采用向量量化（VQ-VAE）思想，将相邻帧的编码差映射到固定大小的码本（codebook）中的一个向量，作为该时间步的潜在行为 \( \bar{a}_{t-1} \)。  
   - 训练过程中结合最大均值差异（MMD）损失，对齐源域视频与目标域图像编码特征，实现域自适应。

2. **双流世界模型（Two-Stream World Model）**  
   - **Trunk Net**：基于真实动作 \( a_t \) 预测短期状态转移和奖励。  
   - **Plan Net**：基于潜在行为 \( \bar{a}_t \) 预测长期状态转移，学习从视频中提取的“行为捷径”（当潜在行为发生变化时的转移点）。  
   - 两者共享图像编码器和解码器，但各自拥有独立的循环状态空间模型（RSSM）参数。

3. **基于模型的策略学习**  
   - 策略网络 \( \pi_{\phi}(a_t | s_t, \bar{a}_t) \) 和价值网络 \( v_{\psi}(s_t, \bar{a}_t) \) 同时接收真实状态和潜在行为。  
   - 引入内在奖励 \( \bar{r}_t = -\| s_t, \bar{s}_t \|_2 \)，衡量 Trunk Net 的短期状态与 Plan Net 的长期状态之间的差异，鼓励短程轨迹向长程目标靠拢。  
   - 价值目标 \( V^{\lambda}_t \) 结合外在奖励与内在奖励，通过 TD(λ) 计算。  
   - 策略优化使用直通梯度（straight-through gradients）和 REINFORCE（离散动作任务）。

### 算法流程（文字描述）
1. **阶段一**：在目标域和源域数据上训练 BAN，学习潜在行为码本。  
2. **阶段二**：分别训练 Trunk Net（仅目标域）和 Plan Net（目标域+源域），后者在关键行为变化点处进行长时预测。  
3. **阶段三**：在想象轨迹上训练策略和价值网络，利用内在奖励对齐两个分支的状态。

## 3. 实验设计

### 数据集与场景
- **Meta-World（机器人操作）**：6 个任务（Drawer Open, Handle Press, Handle Pull, Plate Slide, Coffee Push, Button Press）。辅助视频：BridgeData-V2（60,096 条真实机器人操作轨迹）。  
- **CARLA（自动驾驶）**：天气/路况变化的城市驾驶。辅助视频：NuScenes（1,000 个真实驾驶场景，850 个可用序列）。  
- **MineDojo（开放世界游戏）**：3 个任务（Harvest log in plains, Harvest water with bucket, Harvest sand）。辅助视频：人类 Minecraft 玩家视频（5,000 个片段）。

### 离线数据集构建
使用部分训练的 DreamerV2 智能体收集“中等质量”轨迹（类似 D4RL），每个任务约 200 条（Meta-World）或 1,000 条（CARLA）。

### 对比方法
- **模型无关**：DrQ + CQL（价值保守）、LOMPO（模型基+奖励惩罚）。  
- **纯模型基**：DreamerV2（基线）、DreamerV3（额外对比）。  
- **视频增强方法**：APV（动作无关预训练）、VIP（值函数预训练）、VPT（仅用于 MineDojo，需逆动力学模型标注）。

### 评估指标
- Meta-World：成功率和回合回报（50 个评估回合，3 个随机种子）。  
- CARLA：平均回合回报。  
- MineDojo：任务成功率。

## 4. 资源与算力

论文中未明确说明使用的 GPU 型号、数量、训练时长等具体算力资源。仅在附录中提供超参数表（例如学习率、想象长度等），但未提及计算环境。因此资源与算力信息缺失。

## 5. 实验数量与充分性

- **主实验**：三个基准（Meta-World × 6 任务，CARLA × 1 任务，MineDojo × 3 任务），共 10 个任务场景，每个任务 3 个随机种子。  
- **消融实验**：在 Meta-World（Handle Press）、CARLA、MineDojo 上分别消去了（1）潜在行为输入（2）视频数据（3）内在奖励，验证各组件贡献。  
- **额外实验**：  
  - 与 DreamerV3 对比（2 个任务）。  
  - 离线到在线微调（3 个新任务：Meta-World Soccer、CARLA Night、MineDojo Cobblestone）。  
  - 潜在行为数量影响（5/20/50/100）。  
  - 源视频数量影响（1/4, 1/2, 全部）。  
  - 目标域数据质量影响（中等 vs 随机）。  
  - 潜在行为跨任务迁移性（2 组）。  
  - MMD 损失消融（PCA 可视化）。  
- **充分性评价**：实验覆盖全面，包括不同领域、不同基线、关键组件消融、超参数敏感性、域适应、迁移能力，结论可信度高。但部分任务（如 CARLA）仅有一个驾驶任务，多样性稍弱；MineDojo 仅 3 个任务。

## 6. 论文的主要结论与发现

1. VeoRL 在所有三个基准上显著超越现有方法（DreamerV2 提升可达 350%，部分任务提升超 100%）。  
2. 潜在行为抽象能够从无标签视频中提取与真实动作语义对齐的高层技能（如“推”、“拉”、“抓握”），并通过 t-SNE 可视化验证。  
3. 双流世界模型中的内在奖励有效引导短程轨迹向视频知识引导的长程目标靠拢。  
4. 视频数据量的增加直接提升性能，表明方法具有良好的可扩展性。  
5. 潜在行为具有良好的跨任务迁移能力，减少下游任务对辅助视频重新训练的需求。  
6. MMD 对齐显著缩小域差异，提升 33% 的成功率。  
7. 在离线到在线微调场景中，VeoRL 比 DreamerV2 具有更高的训练效率和最终性能。

## 7. 优点

- **创新性**：首次将无标签视频中提取的离散潜在行为作为“行为先验”引入离线 RL 世界模型，提出双流结构与内在奖励机制。  
- **通用性**：在机器人操作、自动驾驶、开放世界游戏三个差异极大的平台上均表现优异，无需任务特定设计。  
- **实用性**：利用互联网上大量免费视频，无需人工标注动作或奖励，大幅降低数据成本。  
- **实验严谨**：消融实验分别验证每个技术组件；超参数分析、域适应分析、迁移性分析、数据质量分析等覆盖全面。  
- **可视化**：t-SNE 展示了潜在行为与真实动作轨迹的对应关系，直观可信。  
- **性能提升巨大**：部分任务成功率从 0.04 提升至 0.30，回报从 203 提升至 1365，具有实际意义。

## 8. 不足与局限

- **计算开销**：双流世界模型训练需要同时维护两个 RSSM 分支，且涉及向量量化、MMD 损失等，作者坦言“计算复杂度增加”，但未量化具体开销（如训练时间、GPU 内存需求），也没有与单流模型进行显式效率对比。  
- **环境依赖**：辅助视频需要与目标域有一定语义关联（如 BridgeData 用于机器人、NuScenes 用于驾驶），若视频完全无关可能导致负迁移。论文仅测试了相关领域，未探讨跨领域差距更大的情况。  
- **任务覆盖**：CARLA 只使用了一个驾驶任务（无不同难度或天气对比），MineDojo 只有 3 个简单收集类任务，缺乏更复杂的逻辑任务（如建筑、战斗）验证。  
- **可扩展性挑战**：潜在行为码本大小（实验中设为 50）需手动调节；对视频数据量的依赖实验仅用了缩减倍数，未给出数据量下限的标尺。  
- **理论分析缺失**：论文主要依赖经验实验，未提供关于性能提升的定理或收敛性分析，对内在奖励设计的解释较直觉化。  
- **代码与复现**：虽提供项目页面，但论文未在正文中明确开源计划，可能影响可复现性。

（完）

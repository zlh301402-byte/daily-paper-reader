---
title: "$\\textit{Hyper-GoalNet}$: Goal-Conditioned Manipulation Policy Learning with HyperNetworks"
title_zh: 超目标网络：基于超网络的目标条件操作策略学习
authors: "Pei Zhou, Wanting Yao, Qian Luo, Xunzhe Zhou, Yanchao Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=aWWRPyGMie"
tags: ["query:aerial-arm"]
score: 7.0
evidence: 基于超网络的目标条件机械臂操作策略学习
tldr: 提出Hyper-GoalNet框架，利用超网络从目标规格生成任务特定的策略网络参数，将目标解释与状态处理分离。通过前向动力学模型和隐空间对比约束增强表征质量，在多种机械臂操作任务上展现了优于常规条件策略的泛化性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1331, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 686, \"height\": 335, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 881, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1361, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1397, \"height\": 304, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1393, \"height\": 792, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1449, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1411, \"height\": 1772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-awwrpygmie/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1415, \"height\": 1766, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 689, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1446, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 692, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 749, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 750, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 734, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1010, \"height\": 375, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1067, \"height\": 178, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1273, \"height\": 139, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-awwrpygmie/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 837, \"height\": 206, \"label\": \"Table\"}]"
motivation: 目标条件策略学习在多样化目标和环境间保持性能存在挑战。
method: 使用超网络从目标规格生成策略参数，分离目标解释与状态处理，并引入前向动力学和隐空间约束。
result: 在多种机器人操作任务上实现了优于常规条件策略的泛化性能。
conclusion: 超网络生成策略参数能有效提升目标条件操作策略的泛化能力。
---

## Abstract
Goal-conditioned policy learning for robotic manipulation presents significant challenges in maintaining performance across diverse objectives and environments. We introduce *Hyper-GoalNet*, a framework that generates task-specific policy network parameters from goal specifications using hypernetworks. Unlike conventional methods that simply condition fixed networks on goal-state pairs, our approach separates goal interpretation from state processing -- the former determines network parameters while the latter applies these parameters to current observations. To enhance representation quality for effective policy generation, we implement two complementary constraints on the latent space: (1) a forward dynamics model that promotes state transition predictability, and (2) a distance-based constraint ensuring monotonic progression toward goal states. We evaluate our method on a comprehensive suite of manipulation tasks with varying environmental randomization. 
Results demonstrate significant performance improvements over state-of-the-art methods, particularly in high-variability conditions. Real-world robotic experiments further validate our method's robustness to sensor noise and physical uncertainties. Our code and trained models will be made publicly available.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：目标条件策略学习（Goal-conditioned policy learning）在机器人操作中面临挑战：当目标任务和环境变化幅度较大时，常规方法难以保持稳定的性能。传统的做法是将当前状态与目标状态拼接后输入固定参数网络，这导致网络必须用同一套权重处理所有可能的目标‑状态组合，混淆了“处理什么”（当前状态）与“如何处理”（目标驱动的策略）。这种设计限制了泛化能力，尤其在接触复杂、高精度操作任务中表现不佳。
- **整体含义**：作者提出应将目标视为“如何加工当前观察”的规范（specification），而非额外输入特征。受生物认知启发（前额叶皮层根据目标动态调节感觉运动回路），作者利用超网络（Hypernetwork）根据目标图像动态生成策略网络参数，使目标解释与状态处理分离，从而提升对不同目标的适应性和鲁棒性。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：将目标条件策略学习重新定义为参数生成任务——给定当前观测和一组目标观测，超网络H生成目标策略π(·;θ)的权重θ。生成的策略随后仅根据当前观测（RGB图像+本体感知）输出动作，无需再次访问目标信息。
- **关键技术细节**：
  - **超网络架构**：采用优化启发式结构（源自HyperGen [40]），通过K次迭代更新生成权重：θₖ = θₖ₋₁ + λₖ(θₖ₋₁,α)·ψₖ(θₖ₋₁,α)，其中α = φ(o_c, o_g)是当前与目标观测的联合嵌入。这种类似优化迭代的机制增强了生成参数的泛化性。
  - **隐空间塑造（Latent Space Shaping）**：为使超网络更有效，对图像编码器E的隐空间施加两个约束：
    1. **前向动力学模型**：训练一个预测器Φ: Z×A→Z，使Φ(z_t, a_t) ≈ z_{t+1}，损失L_pred = E[ℓ(Φ(z_t, a_t), z_{t+1})]。该约束让隐空间编码可预测的状态转移信息。
    2. **距离单调性约束**：对每个成功轨迹，要求当前状态到目标的欧氏距离单调递减：d(z_{j+1}, z_g) ≤ d(z_j, z_g) − β，损失L_dist = E[Σ max(0, β + d(z_{j+1}, z_g) – d(z_j, z_g))]。β=0即可。这保证隐空间反映物理进展。
  - **训练目标**：总损失L = L_policy + λ_pred L_pred + λ_dist L_dist，其中L_policy是行为克隆的MSE损失（对演示动作进行回归）。超网络（包含编码器、预测器）端到端训练。编码器初始20轮冻结R3M预训练权重，之后联合微调。
  - **推理流程（Algorithm 1）**：给定初始观测I₀和目标图像I_g，反复生成策略权重→采样动作→执行环境步→检查隐空间距离d(E(I_t),E(I_g))是否小于阈值ε，若满足则任务成功。支持自主检测目标完成。

## 3. 实验设计

- **仿真环境**：使用Robosuite（基于MimicGen [31]数据集），包含6类接触丰富任务（咖啡、杯子清理、三件组装、穿线、螺母组装）和2类长时任务（咖啡准备、厨房）。每个任务按环境随机化程度分三个难度级别（d0,d1,d2），难度越高物体位姿变化越大。训练集950条演示，每条包含128×128 RGB图像、9维本体感知、连续动作。
- **对比基线**：GCBC（目标条件行为克隆）、Play-LMP（潜计划模型）、MimicPlay（双阶段分层模仿学习）、C-BeT（条件行为Transformer）。所有基线均改为单目标图像设置以公平比较。额外比较了BeT的增强版（加腕部相机、更长上下文）和HyperZero超网络变体。
- **评估指标**：每个任务在50次独立rollout上的成功率（环境提供的终止信号）。最大步长：接触任务600/800步，长时任务1600步。
- **实际机器人实验**：RealMan RMC-DA 7自由度机械臂，4个任务（拾放、堆叠、拉抽屉、清扫），每个任务15次试验。基线包括GCBC、Play-LMP、C-BeT。采用Intel RealSense D435i相机，采集约70-100条人类遥操作演示训练。

## 4. 资源与算力

- **训练设置**：单个NVIDIA RTX 3090或RTX 4090 GPU。总训练500个epoch，batch size 256，学习率5e-4（余弦退火），Adam优化器，无权重衰减。
- **计算时间与内存**：每个epoch约90-104秒（取决于编码器是否冻结）。冻结编码器时显存占用约3-5 GB，解冻编码器时约13-15 GB（参见附录表11）。
- **推理时间**：每个动作步骤平均6.33 ms（Hyper-GoalNet完整版），1.46 ms（仅用目标图像生成一次权重的变体Hyper-GoalNet(G)），显著快于基线（GCBC 15.47 ms，C-BeT 13.61 ms等，见附录表10）。

## 5. 实验数量与充分性

- **模拟实验**：覆盖8类任务（含2类长时），每个任务3个难度等级，共约24个设置。每组50次rollout，总rollout数1200+。对比5种基线，并做了完整消融：
  - 超网络架构对比（优化型 vs HyperZero）
  - 隐空间塑造消融（去掉L_pred、L_dist、使用不同距离度量、距离参考起点而非目标等）
  - C-BeT加入同样塑造后的表现
  - 编码器冻结时机的影响（epoch 0 vs epoch 20）
- **真实实验**：4个任务，每任务15试，共60次试。对比3种基线。
- **充分性与公平性**：实验设计系统全面，难度层次清晰，基线设置一致（均用单目标图像，相同观测长度等）。但未报告误差棒（如标准差），影响统计显著性评估。总体而言实验数量充足，结论具有较强说服力。

## 6. 论文的主要结论与发现

- **超网络生成参数优于固定参数**：在几乎所有任务和难度下，Hyper-GoalNet的成功率显著高于GCBC、Play-LMP、MimicPlay、C-BeT等传统固定参数方法。特别是在高变异性环境（d1, d2）下，基线几乎失效（如GCBC全程为0），而Hyper-GoalNet仍保持较高成功率。
- **隐空间塑造至关重要**：去掉隐空间塑造后，在高难度任务上性能急剧下降（如咖啡d1从0.76降到0.00），验证了可预测性和单调距离约束的价值。
- **自主目标完成检测可行**：基于隐空间距离阈值判断目标完成，在咖啡任务上准确率86.6%、召回率94.3%，与地面实况高度一致。
- **实际机器人实验中鲁棒性强**：Hyper-GoalNet在4个真实任务上成功率均接近100%，而基线（GCBC、Play-LMP、C-BeT）在大部分任务中几乎完全失败，凸显参数自适应方法对噪声和物理不确定性的优势。

## 7. 优点

- **方法创新性**：首次将超网络用于目标条件机器人操作策略生成，将目标视为“加工规范”而非输入特征，思路新颖且符合认知科学原理。
- **隐空间塑造巧妙**：通过前向动力学和单调距离约束，显式构造具有预测性、进展性的表示空间，使超网络生成参数更容易，并为自主任务检测提供天然依据。
- **实验设计全面**：融合仿真（多任务多难度）和真实机器人验证，对比强基线和充分消融，结论可靠。
- **效率优势**：推理速度快（尤其是Hyper-GoalNet(G)变体），显存占用适中，实用性强。
- **实际部署价值**：仅需单目标图像和少量历史观测，无需复杂多帧序列或附加传感器，易于应用。

## 8. 不足与局限

- **依赖高质量隐空间**：塑造过程需要演示数据具有清晰的目标进展（如逐步接近目标）。若任务高度复杂或演示杂乱，可能难以形成有效结构。
- **对未见过目标敏感**：超网络可能为分布外目标生成不稳定策略，缺乏泛化保证。
- **离线训练缺乏安全约束**：当前方法完全基于行为克隆，未集成强化学习或安全过滤机制，在遇到意外状态时可能产生危险动作。
- **实验结果未报告误差棒**：虽然50次rollout对随机初始化有一定统计覆盖，但无标准偏差或置信区间，影响对结果变异性的理解。
- **任务类型有限**：虽然涵盖接触密集和长时任务，但未测试动态环境、移动操作或柔性物体等更具挑战的场景。
- **缺乏多步推理**：当前框架只处理从当前到单个目标的状态，尚未扩展为多目标顺序规划。

（完）

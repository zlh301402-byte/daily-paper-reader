---
title: "STAR: Learning Diverse Robot Skill Abstractions through Rotation-Augmented Vector Quantization"
title_zh: STAR：通过旋转增强向量量化学习多样化机器人技能抽象
authors: "Hao Li, Qi Lv, Rui Shao, Xiang Deng, Yinchuan Li, Jianye HAO, Liqiang Nie"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=n1cqQK4hhC"
tags: ["query:drone-arm"]
score: 5.0
evidence: 学习机器人操作技能抽象，可用于机器人手臂控制
tldr: 本文提出了STAR框架，通过旋转增强残差技能量化（RaRSQ）来学习多样的机器人技能抽象，解决了现有VQ-VAE方法中的码本崩溃和技能因果关系建模问题。该方法在机器人操作任务中展示了良好的技能学习和组合能力，为复杂行为生成提供了有效途径，尤其适用于需要精细操作控制的场景。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 607, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 855, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 853, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 853, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1579, \"height\": 957, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1768, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1765, \"height\": 1170, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1600, \"height\": 1338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n1cqqk4hhc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1741, \"height\": 2155, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-n1cqqk4hhc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1605, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-n1cqqk4hhc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1604, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-n1cqqk4hhc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 644, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-n1cqqk4hhc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 645, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-n1cqqk4hhc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1770, \"height\": 182, \"label\": \"Table\"}]"
motivation: 现有技能抽象方法存在码本崩溃和因果建模不足，限制了复杂机器人操作行为的学习。
method: 提出旋转增强残差技能量化，编码相对角度防止码本崩溃，并改进了技能组合的因果建模。
result: 在多个机器人操作任务上验证了技能多样性和组合性能的提升。
conclusion: STAR为机器人技能学习提供了鲁棒且高效的框架，可扩展到其他控制任务。
---

## Abstract
Transforming complex actions into discrete skill abstractions has demonstrated strong potential for robotic manipulation.Existing approaches mainly leverage latent variable models, e.g., VQ-VAE, to learn skill abstractions through learned vectors (codebooks), while they suffer from codebook collapse and modeling the causal relationship between learned skills. To address these limitations, we present **S**kill **T**raining with **A**ugmented **R**otation (**STAR**), a framework that advances both skill learning and composition to complete complex behaviors. Specifically, to prevent codebook collapse, we devise rotation-augmented residual skill quantization (RaRSQ).It encodes relative angles between encoder outputs into the gradient flow by rotation-based gradient mechanism. Points within the same skill code are forced to be either pushed apart or pulled closer together depending on gradient directions.Further, to capture the casual relationship between skills, we present causal skill transformer (CST) which explicitly models dependencies between skill representations through an autoregressive mechanism for coherent action generation.Extensive experiments demonstrate the superiority of STAR on both LIBERO benchmark and realworld tasks, with around 12% improvement over the baselines.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

- **背景**：机器人操作任务具有多模态动作分布和高度纠缠的动作空间，传统方法难以学习多任务策略。将连续动作分解为离散技能抽象（如VQ-VAE）是一种有效思路。
- **核心问题**：现有离散潜变量方法存在两大限制：
    - **码本崩溃（codebook collapse）**：多数码本向量在训练中未被使用，导致技能多样性严重不足。根源在于直通估计器（STE）将相同梯度分配给同一码本内的所有编码器输出，忽略了向量间的几何关系。
    - **技能间因果关系建模不足**：现有方法难以在长时任务中有效组合技能，缺乏对技能依赖关系的显式建模，导致动作序列不连贯。
- **研究目标**：提出STAR框架，同时解决码本崩溃和技能组合问题，学习多样化、可复用的技能抽象，实现复杂操作行为。

## 2. 方法论：核心思想、关键技术细节、公式/算法流程

### 2.1 总体架构
- **两阶段训练**：第一阶段训练旋转增强残差技能量化（RaRSQ）学习技能抽象；第二阶段固定RaRSQ，训练因果技能变换器（CST）进行技能组合与动作生成。

### 2.2 旋转增强残差技能量化（RaRSQ）
- **目标**：防止码本崩溃，实现层次化技能表示。
- **核心思想**：在残差量化过程中引入旋转变换，使同一码本内不同编码器输出根据几何关系（相对角度）获得差异化梯度更新，而非简单复制梯度。
- **算法流程（Algorithm 1）**：
    1. 输入动作序列 \(a_{t:t+T}\)，经编码器得潜在向量 \(z\)。
    2. 初始化残差 \(r_0 = z\)。
    3. 对每个深度 \(d = 1\ldots D\)：
        - 最近邻查找：\(k_d = \arg\min_k \| r_{d-1} - e^{(d,k)} \|_2^2\)
        - 计算旋转矩阵 \(R_d\)，将 \(r_{d-1}\) 对齐到所选码本向量 \(e^{(d,k_d)}\)。
        - 应用旋转与缩放：\(\tilde{q}_d = \text{sg}\left[ \frac{\| e^{(d,k_d)} \|}{\| r_{d-1} \|} R_d \right] r_{d-1}\)（sg表示停止梯度）
        - 更新残差：\(r_d = r_{d-1} - \tilde{q}_d\)
    4. 最终量化表示：\(\hat{z} = \sum_{d=1}^D \tilde{q}_d\)，再经解码器得重建动作 \(\hat{a}\)。
- **训练损失**：重建损失 \(L_{\text{recon}}\) + 承诺损失 \(L_{\text{commit}}\)，其中承诺损失鼓励残差靠近旋转缩放后的码本向量。

### 2.3 因果技能变换器（CST）
- **目标**：显式建模技能间的依赖关系，实现连贯动作生成。
- **输入表示**：多模态观测（视觉、本体、语言指令）经对应编码器融合得上下文特征 \(g_t\)。
- **层次化技能预测**：以自回归方式逐层预测码本索引：
  \[
  P(k_1,\ldots,k_D | o, \tau) = \prod_{d=1}^D P(k_d | k_{<d}, g_t)
  \]
  每个深度 \(d\) 由预测头 \(\zeta_d\) 输出分类分布。
- **动作细化**：引入偏移预测头 \(\zeta_{\text{ref}}\) 输出连续偏移，弥补离散化精度损失：
  \[
  \hat{a}_t = \psi\left( \sum_{d=1}^D R_d e_{d,k_d} \right) + \zeta_{\text{ref}}(g_t)
  \]
- **训练损失**：码本索引交叉熵损失 + 动作回归L1损失。

### 2.4 推理过程
- 基于当前观测和指令，通过核采样（nucleus sampling）自回归抽取技能码，再解码为动作序列，以滚动时域方式执行。

## 3. 实验设计

### 3.1 数据集/环境
- **LIBERO基准**：130个任务，分为5个套件（LIBERO-Object, Spatial, Goal, Long, 90），各含10/10/10/10/90个任务，50条专家演示/任务。
- **MetaWorld MT50**：50个不同操作任务，100条演示/任务。
- **真实世界**：使用Cobot Agilex ALOHA双臂机器人，单臂执行两个长时任务（顺序放置物体、抽屉操作），各45条人类遥操作演示。

### 3.2 对比方法
- **离散LVM方法**：VQ-BeT、QueST
- **端到端模仿学习**：ResNet-T、Diffusion Policy、ACT
- **大规模VLA模型**：Octo、OpenVLA

### 3.3 评估指标
- 成功率（Success Rate，SR），每个任务50个回合，3个随机种子。

## 4. 资源与算力
- **文中明确说明**：模型在PyTorch中实现，训练于8块Nvidia RTX L40S 48GB GPU服务器（单个GPU即可容纳）。RaRSQ训练100个epoch，batch size 1024，学习率5.5e-5；CST训练500个epoch，batch size 512，学习率8e-4。采用AdamW优化器，余弦学习率衰减。

## 5. 实验数量与充分性
- **总实验量**：
    - LIBERO：5个套件 × 10（或90）任务，共130任务，每个任务50回合，3种子 → 约19,500次评估。
    - MetaWorld：50任务，类似设置。
    - 真实世界：2个任务各10次试验。
- **消融实验**：去除AR、去除旋转、同时去除，共3组；附录中另包含去除动作细化（Action Refinement）的消融。
- **额外分析**：码本利用率分布、技能层次依赖模式、量化损失曲线等。
- **充分性与公平性**：
    - 对比了多个主流基线，且超参数遵循原论文。
    - 每项实验报告均值与标准差，随机种子。
    - 消融实验覆盖了关键组件，验证了各自贡献。
    - 但未进行跨任务泛化测试或零样本迁移实验。

## 6. 主要结论与发现

- **总体性能**：STAR在LIBERO上总体成功率93.6%，比最优基线QueST（81.5%）提升12.1%；在MetaWorld上达92.7%，优于所有对比方法（最高90.6%）。
- **长时任务优势显著**：在LIBERO-Long上88.5% vs 69.1%（+19.4%），在复杂任务中优势更大。
- **码本利用率**：RaRSQ实现16个码本完全利用（100%），而VQ-VAE仅利用7个（43.8%），且分布更均衡。
- **消融验证**：去除AR使总体下降至89.5%，去除旋转下降至91.0%，两者都去掉降至87.8%，说明两个模块均关键。
- **真实世界**：抽屉操作完整成功率30%（VQ-BeT 10%，QueST 0%）；顺序放置成功率60%（VQ-BeT 30%，QueST 40%）。

## 7. 优点

1. **方法创新性**：将旋转技巧引入残差量化，通过保持几何关系防止码本崩溃，是解决VQ-VAE码本崩溃问题的新颖思路。
2. **层次化技能学习**：残差量化自然产生粗到细的技能层次，与操作任务的层级结构吻合。
3. **因果建模**：CST显式建模技能依赖，配合自回归预测和动作细化，生成连贯动作。
4. **实验全面性**：覆盖模拟和真实环境、多个基准、多种基线，消融充分，分析深入（码本分布、依赖模式、损失曲线）。
5. **性能优势明显**：在几乎所有任务上大幅超越现有方法，包括大规模VLA模型，展示了离散化方法的潜力。

## 8. 不足与局限

1. **手动调参**：码本大小（K=16）和量化深度（D=2）需针对任务域手动设定，未提供自适应机制。
2. **依赖专家数据**：作为模仿学习方法，性能受限于专家演示的质量和多样性，在数据稀缺场景可能受限。
3. **未涉及零样本/域迁移**：实验仅在同分布任务上评估，未检验对新物体、新布局或新任务的泛化能力。
4. **动作精度**：虽然动作细化缓解了离散化损失，但附录显示去除细化后性能下降34.6%，说明离散化仍是瓶颈。此外，偏移预测头依赖于BeT的设计，可能不是最优方案。
5. **计算开销**：两阶段训练需分别训练RaRSQ和CST，总epoch数较大（100+500），但单个GPU即可运行，算力要求尚可。
6. **实验未报告置信区间**：虽提供均值±标准差，但未进行统计显著性检验。真实世界实验仅有10次试验，样本量较小。
7. **局限声明**：作者在论文中已指出上述局限性（需手动调参、依赖演示质量），但未讨论对其他类型控制任务（如移动操作）的适用性。

（完）
